# Taller Intensivo: IA Agéntica con DeepSeek Harness · Catálogo completo

*Documento único. **Parte I:** catálogo base (texto íntegro del documento original, con los niveles de encabezado desplazados un nivel). **Parte II:** comentarios y ampliación de Claude (noviembre de 2026).*

---

# PARTE I · CATÁLOGO BASE (documento original)

## Taller Intensivo: IA Agéntica con DeepSeek Harness (Para Usuarios No Técnicos)

### 1. Estructura General del Curso (6 Horas / 2 Sesiones de 3h)

* **Objetivo:** Desmitificar los agentes locales bajo la fórmula **Modelo + Harness = Agente**, interiorizar protocolos de seguridad (*Read-Only* vs. *Workspace Write*) y desarrollar 1 o 2 proyectos prácticos aplicados al día a día o la docencia.
* **Distribución recomendada:**
  * **Sesión 1 (3h):** Fundamentos, instalación sin terminal (App de escritorio / Web UI), gestión de costes (API/tokens), niveles de seguridad, práctica guiada común (limpieza de carpeta) y elección/arranque del Proyecto 1.
  * **Sesión 2 (3h):** Desarrollo autónomo Proyecto 1 (1h 15m), píldora avanzada de Plugins y MCP (30m), desarrollo Proyecto 2 o evolución avanzada (45m) y puesta en común (30m).

---

### 2. Catálogo Completo de Proyectos (Para Filtrar y Seleccionar)

> **Nota metodológica:** Antes de lanzar cualquier proyecto, los alumnos deben aplicar la **Lista de Comprobación de 7 Puntos** (*Objetivo, Contexto, Entrada, Decisiones, Restricciones, Salida, Verificación*) y exigir al agente que **planifique primero en modo `Read-Only`** antes de autorizar cambios en `Workspace Write`.

---

#### BLOQUE A: Proyectos de Nivel Estándar (Workspace + Archivos Locales + Búsqueda Web)
*Ideales como Proyecto 1. No requieren instalar plugins externos ni configurar servidores MCP; aprovechan las capacidades nativas de lectura, escritura y razonamiento.*

##### 1. El Gestor de Gastos y Facturas Personales
* **Ámbito:** Utilidad Personal / Autónomos / Hogar.
* **Insumos en Workspace:** Carpeta desordenada con 10-15 facturas y tickets en PDF o texto.
* **Misión del Agente:**
  1. Leer todos los documentos en modo `Read-Only` y extraer fecha, proveedor, concepto, base imponible e IVA.
  2. Proponer un plan de renombrado estandarizado (`AAAA-MM-DD_Proveedor_Importe.pdf`).
  3. Ejecutar el renombrado en `Workspace Write` y generar una hoja de cálculo resumen (`resumen_gastos.csv` / `.xlsx`).

##### 2. El Comparador de Presupuestos y Reformas
* **Ámbito:** Utilidad Personal / Toma de decisiones.
* **Insumos en Workspace:** 3 o 4 presupuestos en PDF de una reforma, un viaje o una póliza de seguro, cada uno con formatos y partidas diferentes.
* **Misión del Agente:**
  1. Normalizar conceptos para poder comparar peras con peras.
  2. Detectar qué incluye un proveedor que otro omite ("letra pequeña", impuestos no incluidos o partidas excluidas).
  3. Generar una tabla comparativa en Excel o informe visual en HTML con pros, contras y preguntas para negociar.

##### 3. El Auditor de Contratos, Pólizas o Bases Legales
* **Ámbito:** Utilidad Personal / Gestión Administrativa.
* **Insumos en Workspace:** Contratos de alquiler, condiciones generales de un seguro o bases de una convocatoria/subvención.
* **Misión del Agente:**
  1. Analizar el texto buscando plazos críticos, penalizaciones, cláusulas abusivas o requisitos excluyentes.
  2. Generar un informe ejecutivo en lenguaje claro con una lista de verificación de documentos necesarios y preguntas clave antes de firmar.

##### 4. El Gestor de Actas y Acuerdos de Reunión
* **Ámbito:** Productividad / Departamentos / Asociaciones.
* **Insumos en Workspace:** Carpeta con notas sueltas o transcripciones en bruto de varias reuniones.
* **Misión del Agente:**
  1. Filtrar el ruido conversacional y extraer únicamente **decisiones firmes, responsables asignados y fechas límite**.
  2. Actualizar de forma incremental un documento maestro (`seguimiento_acuerdos.md`) sin borrar el histórico anterior.

##### 5. El Cazador de Bulos y Verificador de Fuentes
* **Ámbito:** Ciudadanía / Periodismo / Aula de Secundaria y Bachillerato.
* **Insumos en Workspace:** Un artículo de opinión, una noticia polémica o una cadena viral guardada en texto/PDF.
* **Misión del Agente:**
  1. Descomponer el texto separando **hechos comprobables** de **opiniones o inferencias**.
  2. Usar la búsqueda web integrada para localizar fuentes primarias que confirmen o desmientan cada dato.
  3. Entregar una tabla de auditoría etiquetando cada afirmación como *Confirmada*, *Matizable*, *No verificable* o *Falsa*, citando enlaces y fecha de consulta.

##### 6. El Diseñador de Situaciones de Aprendizaje y Rúbricas
* **Ámbito:** Docencia (General).
* **Insumos en Workspace:** Un PDF con el currículo oficial de una asignatura o apuntes en bruto de un tema.
* **Misión del Agente:**
  1. Diseñar una secuencia didáctica de 4 sesiones con actividades prácticas y atención a la diversidad.
  2. Redactar una guía de estudio resumida para el alumnado.
  3. Crear una rúbrica de evaluación detallada en formato tabla lista para usar.

---

#### BLOQUE B: Proyectos Avanzados (Creator Mode, Multiagentes, Plugins y MCP)
*Ideales como Proyecto 2 en la Sesión 2, tras la demostración de cómo ampliar DeepSeek Harness.*

##### 7. [PROYECTO ESTRELLA DOCENCIA] El Taller de Crítica y Corrección de Lengua
* **Ámbito:** Docencia (Lengua Castellana y Literatura / Idiomas).
* **Herramientas clave:** `Creator Mode` (arquitectura multiagente con reglas estrictas) + opcionalmente `ModLens` (si se usan fotos de exámenes manuscritos) y `dsh-genui` (para ejercicios interactivos).
* **Por qué supera a un chat tradicional:** Evita que la IA reescriba el texto del alumno o invente criterios. Evalúa calibrándose con ejemplos reales del propio docente.
* **Insumos en Workspace:**
  * `criterios_correccion.pdf`: Rúbrica real del profesor.
  * `muestras_calibradas.docx`: 2 o 3 redacciones ya corregidas y comentadas por el profesor como referencia de nivel.
  * `redacciones_alumnos/`: Carpeta con textos de alumnos (anonimizados).
* **Arquitectura de Subagentes (creada vía *Creator Mode*):**
  1. **Subagente Filólogo:** Analiza exclusivamente normativa, puntuación, cohesión y pobreza léxica citando fragmentos literales. *Restricción:* Prohibido reescribir la redacción.
  2. **Subagente Evaluador:** Cruza los hallazgos con `criterios_correccion.pdf` y `muestras_calibradas.docx` para justificar una calificación por apartados.
  3. **Subagente Tutor:** Genera una ficha individual en Word/Markdown con **3 preguntas guía** y **2 micro-retos de mejora** para el alumno sin darle la solución hecha.
* **Extensión interactiva:** Crear un laboratorio de comentario de texto en HTML o mediante `dsh-genui` donde el alumno identifique figuras retóricas o tesis/argumentos recibiendo feedback basado exclusivamente en los apuntes del profesor.

##### 8. Mi Generador de Juegos y Test Interactivos de Repaso
* **Ámbito:** Docencia / Autoaprendizaje.
* **Herramientas clave:** Plugin `dsh-genui` (interfaces interactivas en el chat) o generación de aplicación web local (`index.html`).
* **Insumos en Workspace:** Apuntes de un tema, un glosario o un capítulo de libro.
* **Misión del Agente:** Transformar el contenido estático en una herramienta interactiva con preguntas tipo test de opción múltiple, tarjetas de memoria (*flashcards*), temporizador y explicación inmediata de cada fallo.

##### 9. Mi Equipo de Investigación y Redacción Automatizada (Multiagente)
* **Ámbito:** Creación de contenido / Investigación / Preparación de ponencias.
* **Herramientas clave:** `Creator Mode` (inspirado en el flujo *Investigador de Nichos*).
* **Misión del Agente:** Crear un *preset* coordinador que orqueste 3 subagentes especialistas:
  1. *Explorador de fuentes* (busca referencias actuales en la web).
  2. *Verificador independiente* (audita datos y descarta afirmaciones sin respaldo).
  3. *Redactor* (estructura el guion, artículo o presentación final).
  * Incluye un archivo de estado (`project-state.md`) y puntos de parada obligatorios para que el usuario valide el rumbo antes de redactar.

##### 10. El Digitalizador de Apuntes Manuscritos y Pizarras con Audio
* **Ámbito:** Estudiantes / Docencia / Productividad personal.
* **Herramientas clave:** Plugin `ModLens` (visión y OCR estructurado) + Plugin `dsh-voice-webspeech` (lectura en voz alta sin necesidad de APIs externas).
* **Insumos en Workspace:** Fotografías de apuntes tomados a mano o esquemas de una pizarra de clase.
* **Misión del Agente:** Extraer el texto y la jerarquía visual de las imágenes, limpiar y estructurar los apuntes en Markdown, ampliar definiciones clave y convertir el resumen en audio para repasarlo escuchando.

##### 11. El "Segundo Cerebro" de un Proyecto a Largo Plazo
* **Ámbito:** Opositores / Escritores / Gestión de proyectos continuos.
* **Herramientas clave:** Plugin `dsh-mnemon` (memoria persistente entre sesiones).
* **Misión del Agente:** Mantener un repositorio vivo de decisiones, reglas de estilo, bibliografía y avances entre distintas sesiones de trabajo, permitiendo retomar un proyecto días después sin tener que volver a explicar todo el contexto desde cero.

##### 12. El Asistente de Bandeja de Entrada y Coordinación de Agenda
* **Ámbito:** Gestión Administrativa / Tutorías Docentes / Atención al Cliente.
* **Herramientas clave:** Conexión MCP (vía **Composio** con autenticación OAuth controlada hacia Gmail y Google Calendar).
* **Misión del Agente:**
  1. Revisar correos recientes filtrando solicitudes de reunión o tutoría.
  2. Consultar los huecos libres reales en Google Calendar.
  3. Proponer franjas compatibles y dejar preparados los borradores de respuesta en Gmail para revisión y envío manual por parte del usuario.

---

### 3. Criterios Sugeridos para Filtrar el Catálogo Final

Para dejar el catálogo definitivo en **6 u 8 fichas** manejables en el taller:
1. **Regla del 50/50:** Mantener un equilibrio entre proyectos de **utilidad personal/administrativa** (que sirven a cualquier perfil) y proyectos **docentes** (que aportan alto valor diferencial).
2. **Disponibilidad de insumos:** Preparar previamente una carpeta `.zip` con datos ficticios pero realistas para cada proyecto elegido, de modo que ningún alumno pierda tiempo buscando archivos durante el taller.
3. **Control de riesgo en Sesión 2:** Si se incluyen proyectos con MCP (Proyecto 12), preparar cuentas de prueba o limitar los permisos a lectura y creación de borradores (nunca envío automático de correos).

---

# PARTE II · COMENTARIOS Y AMPLIACIÓN DE CLAUDE

## Comentarios de Claude sobre el catálogo base (Parte I)

*Observaciones de diseño y seguridad; no son hechos verificados sobre el producto, sino puntos a revisar antes del taller.*

| Proyecto | Comentario |
|---|---|
| **1 · Gastos y facturas** | Los PDF escaneados necesitan lectura de imagen (ModLens). Usar siempre facturas **ficticias**: son datos económicos personales y el texto llega al modelo en la nube. |
| **3 · Auditor de contratos** | Añadir al informe la frase fija «análisis orientativo, no asesoramiento jurídico» y exigir cita literal de cada cláusula señalada. |
| **5 · Cazador de bulos** | Es de los más sólidos: la tabla *Confirmada / Matizable / No verificable / Falsa* enseña método. Pedir también la **fecha de la fuente**, no solo la de consulta. |
| **7 · Crítica y corrección de Lengua** | Proyecto estrella, pero con dos cautelas: (1) las redacciones «anonimizadas» siguen siendo datos del alumnado y llegan al modelo; usar **muestras ficticias o con consentimiento**; (2) si se usan fotos de exámenes con ModLens, comprobar a qué servicio de visión se envían. |
| **10 · Apuntes manuscritos** | Misma cautela con ModLens: apuntes propios o materiales sin personas. |
| **11 · Segundo cerebro** | Antes de usar `dsh-mnemon`, comprobar **dónde guarda** la memoria: en el directorio de plugins aparecen opciones de memoria en la nube. |
| **12 · Bandeja de entrada** | Es el único con **OAuth a cuentas reales**. Mantener cuentas de prueba, permisos de lectura y borradores sin envío. Una alternativa sin ese riesgo es la ficha **E2** (calendario a `.ics`). |
| **Visión de conjunto** | El catálogo se inclina a «gestión + texto»: 8 de 12 proyectos producen documentos. Faltan datos públicos vivos, creatividad y un MCP inocuo; de ahí la Parte II. |

---

### II.0. Lo que he entendido del proyecto

- **Fórmula:** Modelo + Harness = Agente. El alumnado aprende a **planificar en `Read-Only` y ejecutar en `Workspace Write`**, con la lista de 7 puntos como disciplina.
- **Perfil:** docentes no técnicos que salen con 1-2 proyectos que **de verdad usarán**, ya sea en el aula o en su vida.
- **Lo que ya cubre tu catálogo:** papeleo y documentos (1-4), verificación (5), diseño didáctico (6-9), digitalización (10), memoria (11) y correo/agenda (12). Está **escorado a «gestión + texto»**.
- **Lo que le falta (y propongo cubrir):** datos públicos vivos (API), creatividad (música, arte, juego, imagen), un MCP **de verdad inocuo**, y proyectos con **resultado tangible y sorprendente** (algo que se escucha, se ve o se imprime).
- **Límites técnicos que condicionan el diseño:**
  - El modelo de DeepSeek es **solo texto**: para ver imágenes necesita el plugin **ModLens**.
  - Harness está en **vista previa para desarrolladores** y los plugins **pueden ejecutar código arbitrario**: solo plugins revisados.
  - **Aunque un MCP o un plugin sean locales, el texto que el agente lee viaja al modelo en la nube.** Ningún proyecto de este catálogo debe incluir datos personales de alumnado.

### II.1. Criterios con los que he seleccionado

1. **Resultado tangible:** un `.html`, un `.mid`, un `.ics`, un PDF imprimible; algo que se enseña o se usa al salir.
2. **Datos reales, no inventados**, y una **verificación humana clara** (qué se comprueba y contra qué).
3. **Cero credenciales:** ninguna API con clave ni OAuth; si hay MCP, es local o público y sin cuenta.
4. **Dos horas bastan:** cada ficha cabe en un bloque de 1 h 15 m o 45 m, con insumos preparados.
5. **Sin «menús semanales»:** nada que ChatGPT haga igual de bien en un chat.

### II.2. La «escalera MCP» segura (para la píldora de 30 min)

| Peldaño | Servidor | Qué enseña | Riesgo |
|---|---|---|---|
| 1 | **Time** (hora y zonas horarias) | Que un agente *llama a una herramienta* en vez de adivinar | Ninguno |
| 2 | **Fetch** o búsqueda web **sin clave** (p. ej., el plugin de You.com o el servidor público de Parallel) | Traer información externa citada | Las consultas salen a Internet: solo temas públicos |
| 3 | **Filesystem acotado** a una única carpeta de taller | Leer y escribir en un espacio acotado | Bajo, si se limita a `Aula_Proba` |
| 4 | **MarkItDown** (convierte PDF/Word/PowerPoint a Markdown, en local) | Pasar de «montón de PDF» a texto procesable | Bajo; sin cuentas |

**Reglas de oro:** sin OAuth, sin correo ni calendario conectado, sin servidores de la comunidad que no se hayan revisado, y **permiso de solo lectura salvo la carpeta del taller**. Mejor servidores oficiales o de referencia y leer la configuración antes de activarlos.

---

### II.3. Fichas

#### BLOQUE C · Datos públicos vivos (API abiertas sin clave)

*Todas funcionan con el `web_fetch` nativo; no hace falta plugin. **Plan B obligatorio:** guardar en el `.zip` una copia de los datos, porque 25 personas con la misma IP pueden agotar el límite de una API gratuita.*

##### C1. ¿Ya no nieva como antes? (el clima de mi localidad en 30 años)
- **Ámbito:** Docencia (Matemáticas, Ciencias, Geografía) / Curiosidad.
- **Datos:** Open-Meteo (histórico y previsión; sin clave).
- **Misión:**
  1. Descargar series diarias de temperatura y precipitación de 1995 a 2025 para una localidad.
  2. Calcular medias por década, días de helada y tendencias; separar *tiempo* de *clima*.
  3. Generar un informe HTML con gráficos y una sección «lo que esto NO demuestra».
- **Verificación:** contrastar 2 valores con una fuente oficial; entender que los datos de reanálisis son modelo, no estación.
- **Por qué funciona:** convierte el tópico del «ya no nieva» en estadística real.
- **Nivel:** ⭐⭐ · **Tipo:** Proyecto 1.

##### C2. Observatorio de mi concello (población, precios y empleo)
- **Ámbito:** Docencia (Matemáticas, Ciencias Sociales) / Ciudadanía.
- **Datos:** API JSON del INE (sin clave) y catálogo de datos.gob.es (sin clave).
- **Misión:** elegir 3 indicadores (p. ej., población por edades, IPC, paro), descargar sus series, calcular variaciones y redactar «5 hechos» con su fuente y su fecha.
- **Producto:** panel HTML con 3 gráficos + ficha de fuentes.
- **Aviso:** el INE ofrece datos por municipios solo en algunas tablas; el agente debe **decir cuándo un dato no existe** en vez de rellenarlo.
- **Nivel:** ⭐⭐.

##### C3. Terremotos de la semana y la escala logarítmica
- **Ámbito:** Docencia (Matemáticas, Física).
- **Datos:** API de eventos del USGS (sin clave).
- **Misión:** bajar los sismos de los últimos 30 días, dibujarlos en un mapa y comprobar por qué el número de sismos cae al subir la magnitud (**ley de Gutenberg-Richter**, escalas logarítmicas).
- **Producto:** HTML interactivo con un deslizador de magnitud y una explicación para alumnado.
- **Nivel:** ⭐⭐ · **Gancho:** conecta logaritmos con un fenómeno real.

##### C4. Mi euro de ayer (cultura financiera con datos reales)
- **Ámbito:** Docencia (Cultura Financiera, Matemáticas) / Utilidad personal.
- **Datos:** tipos de cambio del BCE (Frankfurter, sin clave) + IPC del INE.
- **Misión:** construir una calculadora HTML que responda «¿cuánto valen hoy mis 1.000 € de 2010?», compare divisas y muestre el efecto compuesto de la inflación.
- **Verificación:** recalcular a mano un caso con el IPC publicado.
- **Aviso:** no es asesoramiento financiero; el informe debe decirlo.
- **Nivel:** ⭐⭐.

##### C5. Museo a la carta (exposición virtual de dominio público)
- **Ámbito:** Docencia (Arte, Historia, Lengua) / Afición.
- **Datos:** API de acceso abierto del Metropolitan Museum y API del Art Institute of Chicago (sin clave); **solo obras marcadas como dominio público**.
- **Misión:**
  1. Elegir un tema («el mar», «mujeres que leen», «el retrato») y consultar ambas colecciones.
  2. Seleccionar 8-10 obras y escribir una ficha comparativa por pares.
  3. Generar una sala virtual en HTML con las imágenes (enlazadas, no copiadas) y 5 preguntas de mirada atenta.
- **Verificación:** comprobar para cada obra la bandera de dominio público y la atribución.
- **Nivel:** ⭐⭐ · **Por qué:** arte con IA sin generar imágenes.

##### C6. Un clásico gallego anotado (edición didáctica en dominio público)
- **Ámbito:** Docencia (Lengua Gallega y Literatura).
- **Datos:** Wikisource en gallego (API de MediaWiki; sin clave).
- **Misión:** tomar un poema o capítulo de dominio público, añadir **glosario**, notas contextuales y actividades de comprensión, y producir una **edición imprimible**.
- **Restricción clave:** el agente **no modifica el texto original** (como el Filólogo del proyecto 7).
- **Nivel:** ⭐⭐.

##### C7. Radar de convocatorias (BOE)
- **Ámbito:** Docencia / Gestión administrativa.
- **Datos:** API de datos abiertos del BOE (sumario diario; sin clave).
- **Misión:** filtrar el sumario de los últimos 14 días con palabras clave que elija el docente (educación, subvenciones, oposiciones) y emitir un boletín con el **identificador BOE y enlace** de cada ítem.
- **Aviso:** solo el texto publicado en el diario oficial es auténtico; el boletín es un **índice**, no una interpretación legal.
- **Nivel:** ⭐⭐⭐ · **Nota:** comprobar si el DOG ofrece una vía equivalente.

##### C8. Salida de campo con datos (especies, tiempo y mapa)
- **Ámbito:** Docencia (Ciencias Naturales, Geografía) / Excursionismo.
- **Datos:** iNaturalist (lecturas públicas), Open-Meteo y el Nomenclátor del IDEE (sin clave).
- **Misión:** a partir de un punto y un radio, listar las especies observadas, la previsión y 3 puntos de interés cercanos, y producir una **hoja de campo imprimible** con un reto de observación.
- **Aviso:** son observaciones ciudadanas; el agente debe distinguir «verificado por la comunidad» de «sin verificar».
- **Nivel:** ⭐⭐⭐.

---

#### BLOQUE D · Creatividad y medios, sin APIs

##### D1. Arte generativo con matemáticas (sin saber programar)
- **Ámbito:** Docencia (Matemáticas, Plástica) / Afición.
- **Herramientas:** nativas (el agente escribe HTML+JS) y, opcionalmente, `dsh-genui`.
- **Misión:** producir un `index.html` que dibuje teselaciones, espirales de Fibonacci, curvas de Lissajous o rosas polares con **controles** (deslizadores) para cambiar los parámetros, y un botón de descarga SVG/PNG.
- **Verificación:** cada figura debe llevar escrita la **fórmula** que la genera.
- **Nivel:** ⭐ · **Gancho:** se ve; se imprime; se regala.

##### D2. Compositor de bolsillo (música y matemáticas)
- **Ámbito:** Docencia (Matemáticas, Música) / Afición.
- **Misión:**
  1. Pedirle una pieza breve en un estilo y estado de ánimo («nana», «ritmo de gaita»).
  2. El agente genera un `index.html` con **Web Audio** que la reproduce y un archivo **.mid** descargable (abrible con MuseScore).
  3. Explorar ideas con matemáticas: escalas, series armónicas, **ritmos euclidianos**.
- **Verificación:** que la pieza se abra en un programa de partituras y que se pueda explicar cada compás.
- **Nivel:** ⭐⭐ · **Aviso:** nada de «estilo de artista X»; originalidad y licencia clara.

##### D3. Fábrica de juegos de mesa imprimibles
- **Ámbito:** Docencia (cualquier materia) / Ocio.
- **Misión:** a partir de un tema del currículo (o de una afición), diseñar un juego completo: **reglas de una página, tablero en SVG, 30 cartas y fichas**, todo listo para imprimir en A4.
- **Verificación:** una **partida de prueba** de 10 minutos y una lista de los cambios que provocó.
- **Nivel:** ⭐⭐ · **Diferencia con el proyecto 8:** el resultado es físico, no una pantalla.

##### D4. Fanzine o álbum con las imágenes de otros obradoiros (puente)
- **Ámbito:** Docencia (Plástica, Lengua) / Creatividad.
- **Insumos:** imágenes producidas con las herramientas del Obradoiro 2 y textos propios.
- **Misión:** maquetar un **fanzine o cartel** en HTML listo para imprimir a PDF, con retícula, jerarquía tipográfica y pie de crédito de cada imagen.
- **Verificación:** que cada imagen lleve su origen y su herramienta.
- **Nivel:** ⭐⭐ · **Interés:** conecta los cinco obradoiros.

##### D5. Fototeca con texto alternativo (accesibilidad)
- **Ámbito:** Docencia / Centro / Afición.
- **Herramientas:** plugin **ModLens** (visión para un modelo de solo texto).
- **Misión:** leer 20-30 fotos, generar **título, descripción y texto alternativo**, proponer álbumes y producir un catálogo HTML con la ficha de cada imagen.
- **Avisos importantes:** (1) ModLens **no depende de un único servicio de visión**: comprobar a qué servicio envía las imágenes antes del taller; (2) **solo imágenes sin personas ni menores** (paisajes, objetos, obras).
- **Nivel:** ⭐⭐⭐.

##### D6. Corto de 60 segundos con fotos y música libre (vídeo en local)
- **Ámbito:** Docencia / Creatividad.
- **Requisito:** **ffmpeg instalado de antemano** en los equipos del taller.
- **Misión:** a partir de 10-15 imágenes, un guion de 8 líneas y una pista de música libre, el agente escribe las órdenes de ffmpeg para montar el vídeo con títulos, transiciones y banda sonora, y deja una **hoja de créditos**.
- **Verificación:** duración, volumen y créditos.
- **Nivel:** ⭐⭐⭐ · **Aviso:** solo material propio o de licencia libre.

---

#### BLOQUE E · MCP sencillos y sin riesgo para el usuario

##### E1. Mi biblioteca de PDF: de montón a base consultable
- **Ámbito:** Docencia / Gestión.
- **Herramientas:** **MarkItDown MCP** (conversión local) + **Filesystem MCP** acotado a la carpeta del taller.
- **Misión:**
  1. Convertir 10-20 documentos (programaciones, instrucciones, normativa) a Markdown.
  2. Crear un índice con resúmenes de una línea.
  3. Responder preguntas **citando archivo y apartado**, y decir «no consta» cuando el documento no lo dice.
- **Verificación:** 5 preguntas con respuesta conocida y 2 trampa (sin respuesta en los documentos).
- **Nivel:** ⭐⭐ · **Aviso:** usar documentos públicos o ficticios; el texto llega al modelo en la nube.

##### E2. Calendario del curso a `.ics` (sin tocar tu calendario real)
- **Ámbito:** Docencia / Productividad.
- **Herramientas:** **Time MCP** y, opcionalmente, Fetch.
- **Misión:** a partir del calendario escolar (PDF o texto), calcular festivos, evaluaciones, puentes y entregas, y generar un archivo `.ics` que **la persona importa a mano**.
- **Verificación:** revisar tres fechas y los días de la semana.
- **Nivel:** ⭐ · **Ventaja de seguridad:** es la alternativa al proyecto 12; no hay OAuth ni acceso al correo.

##### E3. Revisor de plugins y conectores (el «semáforo» de seguridad)
- **Ámbito:** Formación / Seguridad.
- **Misión:** en `Read-Only`, leer el README y el código de un plugin real del ecosistema y producir un **informe en semáforo**: qué permisos pide, si accede a red, si ejecuta comandos, qué datos toca y qué preguntas hacer antes de instalar.
- **Verificación:** contrastar 3 afirmaciones del informe con el código.
- **Nivel:** ⭐⭐⭐ · **Por qué:** los plugins pueden ejecutar código arbitrario; es la competencia que más falta.

---

### II.4. Mi selección y combinaciones

**Ocho que añadiría** (mezclan lo docente y lo personal, y cubren lo que falta):

| # | Proyecto | Por qué entra |
|---|---|---|
| C1 | ¿Ya no nieva como antes? | Datos vivos, matemáticas, efecto sorpresa. |
| C5 | Museo a la carta | Arte y API sin generar imágenes. |
| D1 | Arte generativo | Resultado visual inmediato, nivel mínimo. |
| D2 | Compositor de bolsillo | Música y matemáticas; se escucha. |
| D3 | Fábrica de juegos de mesa | Resultado físico. |
| D5 | Fototeca con texto alternativo | Imagen local con ModLens (con las precauciones). |
| E1 | Biblioteca de PDF | MCP útil y seguro. |
| E3 | Revisor de plugins | Competencia clave de seguridad. |

**Parejas Proyecto 1 → Proyecto 2 (por perfil):**
- *Matemáticas:* C1 → D1 o D2.
- *Lengua y letras:* C6 → D4.
- *Gestión:* E2 → E1.
- *Personal / afición:* D3 → D2.

**Sobre el catálogo original:** si preocupa el proyecto 12 (correo con OAuth), **E2** cubre la agenda sin ese riesgo y puede ser el ejemplo de MCP «de entrada».

### II.5. Preparación y riesgos

1. **`.zip` con insumos y con copias de los datos de cada API** (plan B).
2. **Probar cada API antes del taller:** no he podido abrir ni probar las API en esta sesión; los nombres de servicio son los oficiales que conozco, y conviene validar cada URL y sus condiciones.
3. **Límites compartidos:** 25 personas en la misma red pueden agotar una API gratuita.
4. **Privacidad:** nada de datos personales de alumnado; el texto que lee el agente llega al modelo.
5. **Plugins:** solo los revisados (E3 sirve de entrenamiento), siempre desde fuentes conocidas.
6. **Derechos:** solo material de dominio público o de licencia libre; atribución visible en museo (C5), fanzine (D4) y vídeo (D6).
7. **Estado del producto:** Harness está en vista previa y cambia entre versiones; preparar capturas de seguridad por si algo cambia.
