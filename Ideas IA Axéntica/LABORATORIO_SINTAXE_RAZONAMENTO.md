# Laboratorio de sintaxis (4º ESO) · razonamiento y diseño

Documento de trabajo. Recoge el razonamiento de partida, el diseño propuesto y las cuestiones abiertas, para continuar con la compañera de Castellano. Está pensado como proyecto de catálogo («Practicador con verdade fixada») y también como herramienta real para su aula.

---

## 1. El problema

La compañera se queja de que los ejercicios que producen las IA tienen poco nivel. Mi lectura es que hay **dos fallos distintos**, y conviene separarlos porque tienen soluciones distintas:

1. **Fallo de generación.** Las frases son demasiado fáciles («El perro come huesos») y no reproducen las trampas reales de 4º ESO.
2. **Fallo de juicio.** Cuando una IA corrige o analiza, **decide ella** qué es correcto, y puede equivocarse con total seguridad. En sintaxis es especialmente grave porque hay ambigüedad legítima, discrepancias terminológicas y varios errores sutiles.

Una app que resuelva solo el primer fallo seguirá sin satisfacerla, porque lo que más le importa a una docente es que la corrección sea fiable.

## 2. Principio de diseño

> **El LLM construye el instrumento; la verdad la fija la docente; el código verifica.**

Consecuencias directas:

- El LLM **no corrige en tiempo real** las respuestas del alumnado.
- Ninguna frase entra en el banco sin **análisis validado por la docente**.
- La corrección es **determinista**, comparando contra el análisis validado.
- La app funciona sin conexión y sin llamadas a un modelo en tiempo de uso.

Es el mismo patrón que generaliza a otras materias (formulación química, conjugación, cronologías, unidades), y por eso encaja en el curso como lección sobre agentes: delegar la fabricación, no la responsabilidad.

## 3. Arquitectura en cuatro fases

### Fase 1 · Criterios de la docente

Ella define, antes de que el agente toque nada:

- **Esquema terminológico.** Gramática tradicional o NGLE (o el que marque su programación). No se mezclan.
- **Funciones que se piden en 4º ESO.** Sujeto, predicado, CD, CI, CC, atributo, CRég, CAg, predicativo, complemento del nombre, aposición, vocativo, etc.
- **Tipos de oración.** Simple, compuesta (coordinada, yuxtapuesta) y compleja (subordinada sustantiva, adjetiva, adverbial).
- **Qué cuenta como acierto.** Por ejemplo, si se exige o no marcar el núcleo, o si se acepta la doble denominación de alguna construcción.

### Fase 2 · Corpus

- Frases **reales**: de las lecturas del curso, de textos de dominio público o redactadas por ella. No generadas libremente por el LLM.
- **Gradación por nivel (1 a 5).** El nivel 4-5 incluye dos o tres niveles de subordinación, elipsis, construcciones con *se* y estructuras ambiguas.
- **Semilla ideal.** Que traiga unas 20 frases que sus alumnos suelen fallar en exámenes. Ahí está el valor real del proyecto.
- Cada frase lleva su **fuente** (obra, edición) para mantener la trazabilidad.

### Fase 3 · Banco validado

El agente prepara, para cada frase:

- El **análisis en árbol** (formato estructurado, ver §5).
- Las **pruebas diagnósticas** aplicables (sustitución por pronombre, pasivización, concordancia, conmutación).
- Los **errores típicos** esperables y su diagnóstico (ver §6).
- Una **cadena de pistas** de menos a más ayuda.
- Variantes **aceptables** de etiquetado y análisis alternativos si la frase es ambigua.

Después hay dos controles:

1. Un **segundo pase adversarial**: otra instancia (o un prompt distinto) intenta encontrar fallos en el análisis. Las discrepancias se marcan.
2. La **revisión de la docente, frase por frase**. Nada pasa a producción sin su visto bueno. Las frases ambiguas se etiquetan «admite dos análisis»: es una virtud pedagógica, no un defecto.

### Fase 4 · App HTML local

La app lee el banco y corrige de forma determinista. Ver modos de interacción en §7.

## 4. Por qué no dejar al LLM corregir en tiempo real

- Puede aceptar como correcto un análisis erróneo o rechazar uno válido.
- Puede cambiar de criterio entre dos intentos.
- No es reproducible: la docente no puede auditar cada corrección.
- Hace la herramienta dependiente de conexión y coste.

Queda una cuestión abierta (§10): permitir, como ayuda **secundaria y marcada**, una explicación generada a partir del análisis validado.

## 5. Esquema de datos (boceto)

Frase de ejemplo: *Los vecinos que viven en la aldea le entregaron las llaves a la alcaldesa.*

```json
{
  "id": "es-0001",
  "lang": "es",
  "level": 3,
  "source": { "work": "...", "edition": "...", "status": "adaptada | literal | propia" },
  "text": "Los vecinos que viven en la aldea le entregaron las llaves a la alcaldesa.",
  "tokens": ["Los","vecinos","que","viven","en","la","aldea","le","entregaron","las","llaves","a","la","alcaldesa","."],
  "analysis": {
    "sentence_type": "compleja",
    "predicate_type": "verbal",
    "nodes": [
      { "fn": "SUJ", "span": [0, 6], "children": [
          { "fn": "NUCLEO", "span": [1, 1] },
          { "fn": "SUB_ADJ", "span": [2, 6], "modifies": [1, 1], "children": [
              { "fn": "SUJ", "span": [2, 2], "note": "relativo" },
              { "fn": "NV",  "span": [3, 3] },
              { "fn": "CC_LUGAR", "span": [4, 6] }
          ]}
      ]},
      { "fn": "CI",  "span": [7, 7], "note": "duplicación pronominal" },
      { "fn": "NV",  "span": [8, 8] },
      { "fn": "CD",  "span": [9, 10] },
      { "fn": "CI",  "span": [11, 13] }
    ]
  },
  "tests": [
    { "target": "CD", "test": "pasivización", "expected": "Las llaves fueron entregadas..." }
  ],
  "common_errors": ["E01", "E05"],
  "alt_analyses": [],
  "validated_by": "docente",
  "validated_on": "AAAA-MM-DD"
}
```

Detalles de diseño:

- Los **intervalos de tokens** permiten corregir por separado el **acotado** («marcaste bien dónde empieza y acaba») y la **etiqueta** («pero la función es otra»). Eso da retroalimentación gradual y crédito parcial.
- Los códigos de función (`SUJ`, `CD`, etc.) se definen en un fichero de esquema por lengua y por tradición terminológica, de modo que el motor sea independiente de la lengua.

## 6. Taxonomía de errores (primer borrador a validar por la docente)

Cada error tiene: identificador, qué contradice (etiqueta del alumno frente a la correcta), prueba diagnóstica y plantilla de mensaje.

| Id | Confusión típica | Prueba diagnóstica que la app propone |
| --- | --- | --- |
| E01 | CD ↔ CI (incluido CD de persona con *a*) | Sustitución por *lo/la* frente a *le*; pasivización |
| E02 | Atributo ↔ predicativo | Sustitución por *lo* (el atributo se sustituye, el predicativo no); tipo de verbo |
| E03 | CRég ↔ CC | Exigencia de preposición por el verbo; sustitución por adverbio |
| E04 | *Se*: pasiva refleja ↔ impersonal | Concordancia con el supuesto sujeto |
| E05 | *Que* relativo ↔ conjunción | Sustitución por *el cual*; función dentro de la subordinada |
| E06 | Subordinada adjetiva ↔ sustantiva | Sustitución por *esto/eso* frente a concordancia con antecedente |
| E07 | Elipsis del verbo en coordinadas | Reponer el verbo elidido |
| E08 | Interrogativa indirecta ↔ otras subordinadas | Sustitución por la pregunta directa |
| E09 | Perífrasis verbal ↔ verbo + complemento | Posibilidad de sustituir por otro verbo o por un pronombre |

**Esta lista debe confirmarla la compañera**: ella sabe cuáles son los errores reales de su alumnado y cuáles faltan. Lo valioso del proyecto es ese conocimiento didáctico, no el código.

## 7. Modos de interacción

1. **Marcar y etiquetar.** El alumno selecciona tramos de texto con el ratón y les asigna una función (equivalente digital de los corchetes y llaves).
2. **Construir el árbol.** Arrastrar y anidar constituyentes.
3. **Prueba antes de etiquetar.** Para ciertas funciones, la app pide **aplicar la prueba** (por ejemplo, sustituir el complemento por *lo/le*) antes de dejar etiquetar.
4. **Depura.** Se muestra un análisis con errores plantados y el alumno debe encontrarlos y justificarlos. Es el modo de nivel más alto.
5. **Juez.** Frase ambigua con dos análisis posibles: ¿cuál defiendes y por qué?
6. **Mapa de debilidades.** Registro de errores por categoría que elige las frases siguientes.

La retroalimentación sale de la taxonomía de §6, no de un modelo. Ejemplo: «Acotaste bien *a la alcaldesa*, pero la etiquetaste como CD. Prueba a sustituirlo por un pronombre: ¿*les entregaron las llaves a ella* o *la entregaron*…?».

## 8. Multilengua

- El motor es independiente de la lengua si el **esquema de etiquetas** es configurable (fichero por lengua y tradición).
- Para gallego y castellano existen **corpus anotados de Universal Dependencies** de licencia abierta (hay que verificarlo caso por caso). Pueden servir como **fuente de frases con un análisis propuesto**, no como verdad.
- **Mapeo a términos escolares.** Se haría con un script determinista (por ejemplo sujeto → SUJ, objeto directo → CD, objeto indirecto → CI). Es imperfecto: algunas etiquetas de dependencias no distinguen entre CC y CRég, o entre atributo y predicativo, y hay que **desambiguar a mano**.
- **Valor añadido.** Un **modo contrastivo gallego-castellano** con la misma frase en ambas lenguas (pronombres átonos, CI con *-lle*, interferencias).
- **Inglés y francés.** Es más honesto limitarlo a tipos de oración y cláusulas, porque el análisis por funciones no es tradición escolar en esas materias. Habría que consultar a esos departamentos antes de prometer nada.

## 9. Lo que no hay que hacer

- Pedir al LLM que evalúe respuestas del alumnado en tiempo real.
- Generar frases con un LLM y usarlas sin validar.
- Aceptar el análisis del LLM como «solución» sin firma de la docente.
- Mezclar esquema tradicional y NGLE en el mismo banco.
- Prometer cobertura de todos los fenómenos: es preferible un banco pequeño y fiable.

## 10. Cuestiones abiertas

1. ¿Qué esquema terminológico usa exactamente la compañera, y qué opciones admite como correctas?
2. ¿Quiere que la app exija **justificación** (pruebas) o solo etiquetado?
3. ¿Cuál es el tamaño realista del banco inicial (¿30 frases de nivel alto bien validadas?)?
4. ¿Se permite una **ayuda generada por LLM** (explicación a partir de la solución validada), claramente marcada como secundaria?
5. ¿Cómo se registran los resultados del alumnado? ¿Local en el navegador, exportable, o sin registro?
6. ¿Qué lengua va primero: castellano o gallego? ¿Hay colega de Galego que quiera validar?
7. ¿Cómo se tratan las frases con más de un análisis válido?
8. Licencia y fuente de cada frase del corpus (obras de lectura, dominio público, redacción propia).
9. Alcance de la versión para el curso: ¿se enseña el proyecto completo o solo el patrón con diez frases?

## 11. Hoja de ruta

| Versión | Contenido | Para qué sirve |
| --- | --- | --- |
| v0 | Diez frases validadas, un modo (marcar y etiquetar), corrección determinista | Que la compañera lo pruebe y lo critique |
| v1 | Taxonomía de errores con pruebas diagnósticas, modo «Depura», mapa de debilidades | Calidad pedagógica |
| v2 | Banco de 100 frases con niveles, versión en gallego | Uso real en aula |
| v3 | Modo contrastivo gallego-castellano, importación desde corpus anotados | Ampliación |

**Prueba de fuego para v0.** Mezclar análisis hechos por la compañera con otros generados por el agente y ver si ella detecta los suyos y cuántos errores encuentra en los del agente. Si encuentra errores, hay base para decir que el control de calidad es necesario y funciona.

## 12. Semilla para recrear la v0

Para probarlo antes de clase, un encargo posible (ajustar a la plataforma):

```text
Proyecto: practicador de análisis sintáctico (4º ESO, castellano).
Reglas:
- No inventes análisis. Solo trabajas con las frases y los análisis que yo te doy.
- Antes de programar, define el formato de datos (JSON) y enséñamelo.
- La app debe corregir de forma determinista contra mi análisis, sin llamar a ningún modelo.
- Diferencia en la corrección entre "bien acotado" y "bien etiquetado".
- Plan antes de ejecutar; no escribas fuera de la carpeta de entregables.
Material: adjunto 10 frases con su análisis en el formato acordado.
Entrega: un HTML local con un modo (marcar y etiquetar) y una lista de casos de prueba
que yo pueda comprobar a mano.
```

Cómo comprobarlo: introduce a propósito tres respuestas erróneas y mira si el mensaje que devuelve es el que tú darías. Si no lo es, el fallo está en la taxonomía o en los datos, no en el modelo.

## 13. Una nota sobre el aprendizaje de fondo

Este proyecto resume bien la tesis del curso. El docente no **programa** ni **cede la corrección** a la IA. Define un buen encargo, fija las fuentes de verdad, delega la fabricación y valida el resultado. Cualquier materia con respuestas verificables puede seguir el mismo patrón.
