# Hitos_IA_Top20 · Impacto Transformador: Casos de Éxito Reais da IA

**Curso 2026-2027 · Estado del arte a 12 de noviembre de 2026**
Convención de idioma: títulos, subtítulos y categorías en gallego (como las tarjetas actuales); descripciones en español.

---

## 0. Notas de verificación y correcciones sobre la base actual (léelas antes de publicar)

Al contrastar los 9 hitos existentes con fuentes primarias y prensa de referencia aparecen **errores o imprecisiones que conviene corregir**:

| Hito | Dato del prompt | Qué dicen las fuentes |
|---|---|---|
| **3 · Microsoft/PNNL** | «N2116 en 9 meses en vez de 20 años» | Se mezclan dos cifras. **80 h de cómputo** filtraron 32 millones de candidatos hasta 18 (el equipo estimó ~20 años por métodos convencionales). **~9 meses** fue lo que tardó PNNL en validar la prueba de concepto en el laboratorio. «70 % menos de litio» es la cifra de Microsoft para una composición Na-Li (≈70 % sodio); es un resultado de laboratorio, no un producto. |
| **4 · Medicina** | «Insilico completa fases clínicas humanas» | Completó la **fase IIa** (Nature Medicine, 2025). La **fase III arrancó en julio de 2026**; sigue sin estar aprobado. «Viz.ai < 30 s» y los resultados de Cancer Copilot **no los pude verificar**: recomiendo rebajar su peso o quitar la cifra. |
| **5 · Figure + BMW** | «OpenAI + Figure», «turnos de hasta 20 horas» | Los turnos fueron de **10 horas** (L-V), durante **11 meses**. Figure rompió su colaboración con OpenAI en 2025 y usa su propio modelo (Helix). Cifras (Figure/BMW): 1.250+ h, 90.000+ piezas, 30.000+ X3. |
| **6 · o1 / AlphaProof** | «IA hacia los Problemas del Milenio» | **Ningún Problema del Milenio está resuelto**. AlphaProof+AlphaGeometry 2 logró **plata** (28/42) en la IMO 2024; el **oro** (35/42) llegó en 2025 con modelos de lenguaje generales. Ver hito 15 y la sección especial. |
| **8 · Tokamak** | «plasma a 100 millones de grados» | Esa cifra corresponde a reactores grandes; el TCV (EPFL) es un experimento menor. Sugiero «plasma a millones de grados». Hito de 2022: pendiente de actualizar con novedades de 2025-26. |
| **Vídeos** | URL de YouTube | **No pude abrir YouTube desde este entorno**, así que no he podido comprobar las URL actuales (la de Figure 02 me resulta sospechosa). Abajo marco como ✔ solo los ID localizados en fuentes externas con título y canal coincidentes; el resto lleva un enlace de búsqueda. **Comprueba cada enlace a mano antes de publicar.** |

**Transparencia sobre actores:** los hitos 9 y 15 incluyen productos de Anthropic, empresa que desarrolla a Claude, el asistente que ha redactado este documento. Se han contrastado con fuentes de terceros, pero conviene una segunda lectura.

---

## 1. Tabla resumen de los 21 hitos

| # | Hito / Nombre | Categoría | Validación | Entidades / Autores | Año | Impacto clave en 1 línea |
|---|---|---|---|---|---|---|
| 1 | AlphaFold 3 & ESMFold | Bioloxía & Medicina | **Demostrado** | Google DeepMind; Meta AI / EvolutionaryScale; D. Baker | 2020-24 | +200 M de estructuras de proteínas abiertas y Nobel de Química 2024 |
| 2 | Vesuvius Challenge e Nazca | Historia & Humanidades | **Demostrado** | Univ. de Kentucky, Vesuvius Challenge; Univ. Yamagata, IBM, DLR | 2023-26 | Primer rollo cerrado leído íntegro (PHerc. 1667) y 303 geoglifos en Nazca (PNAS) |
| 3 | Baterías sólidas: Microsoft & PNNL | Enerxía & Materiais | **Demostrado** | Microsoft (Azure Quantum Elements), PNNL; DeepMind (GNoME) | 2023 | 32 M de candidatos filtrados en <80 h; electrolito N2116 probado en laboratorio |
| 4 | Rentosertib: fármaco de IA | Bioloxía & Medicina | **Ensaio Clínico** | Insilico Medicine; centros clínicos | 2025-26 | Diana y molécula diseñadas con IA; fase IIa superada y fase III activa |
| 5 | Figure 02 na planta de BMW | Robótica & Embodied AI | **Despregado** | Figure AI, BMW Group | 2024-26 | Humanoide en producción industrial: 30.000+ BMW X3, 1.250+ h |
| 6 | Razoamento formal: AlphaProof | Matemáticas & Ciencias Formais | **Investigación** | Google DeepMind; comunidad Lean | 2024-25 | Plata IMO 2024 y oro IMO 2025; verificación formal sin alucinación |
| 7 | GraphCast e WeatherNext | Ciencias da Terra | **Despregado** | Google DeepMind; ECMWF (AIFS); NHC (EE. UU.) | 2023-26 | Predicción global en 60 s y más de un día extra de antelación en ciclones |
| 8 | Fusión: IA domando o plasma | Física & Espazo | **Demostrado** | DeepMind; Swiss Plasma Center (EPFL) | 2022 | RL controla en tiempo real las bobinas magnéticas del tokamak TCV |
| 9 | Anthropic: Mapping the Mind e Computer Use | Software & Axentes | **Investigación** | Anthropic | 2024 | Conceptos localizados con autoencoders (SAE) y agentes que operan el PC |
| 10 | AlphaEvolve, AlphaTensor e FunSearch | Matemáticas & Ciencias Formais | **Despregado** | Google DeepMind | 2022-26 | Algoritmos nuevos: Strassen batido tras 56 años; 0,7 % de ahorro en Google |
| 11 | AlphaChip: IA que deseña chips | Hardware & Computación | **Despregado** | Google (Brain/DeepMind), MediaTek | 2021-24 | Floorplans en horas, usados en TPUs v5e, v5p, Trillium y Axion |
| 12 | AlphaGenome e OpenCRISPR | Bioloxía & Medicina | **Demostrado** | Google DeepMind; Profluent | 2025-26 | 98 % no codificante del genoma y editores CRISPR generados de novo |
| 13 | Interfaces cerebro-ordenador que falan | Bioloxía & Medicina | **Ensaio Clínico** | UC Davis, BrainGate, Stanford | 2024-26 | ELA: 56 palabras/min en casa durante 2 años de uso continuo |
| 14 | Deep Loop Shaping e ondas gravitacionais | Física & Espazo | **Demostrado** | DeepMind, Caltech/LIGO, GSSI | 2025 | Ruido de control reducido 30-100× en el detector LIGO Livingston |
| 15 | Erdős e a matemática de investigación | Matemáticas & Ciencias Formais | **Investigación** | OpenAI; Google DeepMind; comunidad Lean | 2026 | Conjetura de Erdős de 1946 refutada; 9 problemas abiertos en Lean 4 |
| 16 | Axentes de software: SWE-bench | Software & Axentes | **Investigación** | Anthropic, DeepSeek, OpenAI (Vals.ai, Princeton) | 2023-26 | De ~2 % a >95 % en incidencias GitHub (con cautela por tests y contaminación) |
| 17 | Waymo: conducción sen condutor | Robótica & Embodied AI | **Despregado** | Waymo (Alphabet); Swiss Re; IIHS | 2020-26 | 500.000+ viajes/semana comerciales y −81 a −94 % de choques con lesiones |
| 18 | Titorías de IA na Educación | Educación & Sociedade | **Ensaio Clínico** | Banco Mundial (Nigeria); Harvard | 2024-26 | 6 semanas ≈ 1,5-2 años de escolaridad en ensayo aleatorizado con docentes |
| 19 | Mamografía asistida por IA (MASAI) | Bioloxía & Medicina | **Ensaio Clínico** | Univ. de Lund; ScreenPoint | 2021-26 | Ensayo aleatorizado en 105.000 mujeres: +29 % detección, −44 % carga médica |
| 20 | Antibióticos xerados por IA | Bioloxía & Medicina | **Demostrado** | MIT (Collins), Broad, Wyss; Phare Bio | 2025 | Moléculas NG1 y DN1 eficaces contra gonorrea y SARM en ratones |
| 21 | Claude Mythos e Ciberseguridade | Ciberseguridade & Software | **Investigación** | Anthropic; UK AISI; DARPA (AIxCC); Project Glasswing | 2026 | Detección de zero-days, defensa a velocidad de máquina y dilema de doble uso |

**Orden sugerido de presentación (IDs):** 1 → 12 → 4 → 20 → 19 → 13 → 7 → 17 → 5 → 3 → 8 → 14 → 2 → 6 → 10 → 11 → 15 → 16 → 9 → 21 → 18.
(Salud y ciencias de la vida primero, mundo físico después, matemáticas, software y ciberseguridad, y educación como cierre para el profesorado.)

---

## 2. Fichas detalladas

### ID 1 — AlphaFold 3 & ESMFold
- **Título sugerido:** O mapa de todas as proteínas
- **Subtítulo:** Premio Nobel de Química 2024 e unha base de datos aberta con máis de 200 millóns de estruturas.
- **Categoría:** *Bioloxía & Medicina*
- **Organizaciones:** Google DeepMind; Meta AI (equipo ESM, hoy EvolutionaryScale); Universidad de Washington (David Baker)
- **Descripción:** Durante cinco décadas, deducir la forma 3D de una proteína a partir de su secuencia de aminoácidos exigía meses de cristalografía por cada estructura. AlphaFold 2 (DeepMind, 2020) alcanzó precisión casi experimental en la competición CASP14; su base de datos pública supera ya los 200 millones de estructuras. ESMFold (equipo ESM de Meta) añadió más de 600 millones de proteínas metagenómicas con predicciones en segundos. AlphaFold 3 (Nature, 2024) predice además interacciones con ADN, ARN, iones y ligandos. En 2024, Demis Hassabis y John Jumper compartieron el Nobel de Química con David Baker, pionero del diseño de proteínas nuevas. Impacto: millones de investigadores acceden gratis a estructuras que sirven para diseñar fármacos, enzimas o vacunas. Límite: son predicciones; no sustituyen a la validación experimental.
- **Vídeo recomendado:** Veritasium — «AlphaFold – The Most Useful Thing AI Has Ever Done» (~25 min) → https://www.youtube.com/watch?v=P_fHJIYENdI ✔ *(ID localizado en fuente externa con canal y título coincidentes; no reproducido aquí)*. Alternativa: conferencias Nobel 2024 de Baker, Hassabis y Jumper en el canal Nobel Prize → [buscar](https://www.youtube.com/results?search_query=2024+Nobel+Prize+lectures+chemistry+Baker+Hassabis+Jumper).
- **Tag UI:** `border-emerald-500 text-emerald-300`

### ID 2 — Vesuvius Challenge e arqueoloxía con ML
- **Título sugerido:** Ler o que o lume converteu en carbón
- **Subtítulo:** Un rollo pechado de Herculano lido de principio a fin sen abrilo, e 303 novos xeoglifos en Nazca.
- **Categoría:** *Historia & Humanidades*
- **Validación:** `Demostrado en Laboratorio`
- **Organizaciones:** Univ. de Kentucky y Vesuvius Challenge; Univ. de Yamagata, IBM y DLR (Nazca); Google DeepMind (Ithaca/Aeneas)
- **Descripción:** La erupción del Vesubio (79 d. C.) carbonizó la biblioteca de la Villa de los Papiros: rollos que se deshacen si se intenta abrirlos. El Vesuvius Challenge publicó escáneres de rayos X en 3D y convocó a la comunidad: la visión por computador «desenrolla» virtualmente las capas y detecta la densidad de la tinta invisible. En junio de 2026 se anunció la primera lectura completa, de extremo a extremo, del rollo cerrado PHerc. 1667 (más de 20 columnas de griego antiguo). En paralelo, modelos de visión artificial aplicados a fotografías aéreas aceleraron la identificación de 303 nuevos geoglifos figurativos en Nazca (estudio publicado en PNAS en 2024 por la Univ. de Yamagata, IBM y DLR). La IA no descubre sola el pasado, pero amplifica de forma exponencial la labor de arqueólogos e historiadores.
- **Vídeo recomendado:** canal oficial Vesuvius Challenge / Univ. de Kentucky sobre la primera lectura completa (2026) → [buscar](https://www.youtube.com/results?search_query=Vesuvius+Challenge+first+scroll+read+PHerc+1667) ⚠ ID sin verificar.
- **Tag UI:** `border-amber-500 text-amber-300`

### ID 3 — Microsoft & PNNL: baterías sólidas
- **Título sugerido:** 32 millóns de materiais en 80 horas
- **Subtítulo:** Un electrólito novo con ~70 % menos de litio, da pantalla ao laboratorio.
- **Categoría:** *Enerxía & Materiais*
- **Validación:** `Demostrado en Laboratorio`
- **Organizaciones:** Microsoft (Azure Quantum Elements); Pacific Northwest National Laboratory (PNNL); Google DeepMind (GNoME)
- **Descripción:** Los electrolitos sólidos prometen baterías más seguras y densas, pero hallar un material estable y buen conductor entre millones de combinaciones químicas es inviable por ensayo y error. En 2023, Microsoft combinó IA y computación de alto rendimiento para filtrar 32 millones de candidatos: unos 500.000 materiales estables, 800 y finalmente 18 candidatos en menos de 80 horas de cómputo en la nube (el equipo lo estimó en ~20 años por métodos convencionales). PNNL sintetizó y validó en unos nueve meses un electrolito de sodio-litio-itrio-cloro (≈70 % de sodio, de ahí el ahorro de litio; «N2116» en la prensa). Es una prueba de concepto: faltan estabilidad y ciclos. Complemento: GNoME (DeepMind, Nature 2023) predijo 2,2 millones de cristales estables nuevos.
- **Vídeo recomendado:** el artículo de Microsoft «Discoveries in weeks, not years» incluye un vídeo oficial incrustado; localiza su enlace en la página de Microsoft Source o busca en el canal de Microsoft → [buscar](https://www.youtube.com/results?search_query=Microsoft+Azure+Quantum+Elements+PNNL+battery+material+AI) ⚠ ID sin verificar. (Sustituye a la URL de fusión nuclear repetida.)
- **Tag UI:** `border-yellow-500 text-yellow-300`

### ID 4 — Rentosertib: primer fármaco de IA en fase III
- **Título sugerido:** Un fármaco ideado de principio a fin por IA
- **Subtítulo:** Da diana á molécula: xa en fase III contra a fibrose pulmonar (xullo 2026).
- **Categoría:** *Bioloxía & Medicina*
- **Validación:** `Ensaio Clínico`
- **Organizaciones:** Insilico Medicine; centros clínicos hospitalarios
- **Descripción:** Desarrollar un fármaco suele costar más de una década. Insilico usó IA en toda la cadena: PandaOmics propuso la diana (TNIK) para la fibrosis pulmonar idiopática y Chemistry42 diseñó la molécula (rentosertib, antes ISM001-055). En la fase IIa (71 pacientes, 22 centros en China; Nature Medicine, 2025) la dosis de 60 mg diarios mejoró la capacidad vital forzada en +98,4 mL a las 12 semanas, frente a −20,3 mL con placebo. En julio de 2026 arrancó la fase III (320 pacientes, 47 centros, 52 semanas). Importante: sigue siendo experimental, no está aprobado y la fase III puede fallar.
- **Vídeo recomendado:** Insilico Medicine, canal oficial, sobre rentosertib / Pharma.AI → [buscar](https://www.youtube.com/results?search_query=Insilico+Medicine+rentosertib+Pharma.AI) ⚠ ID sin verificar (la URL actual no pude comprobarla).
- **Tag UI:** `border-emerald-500 text-emerald-300`

### ID 5 — Figure 02 na planta de BMW
- **Título sugerido:** Humanoides na cadea de montaxe
- **Subtítulo:** 11 meses, 1.250 horas e máis de 30.000 BMW X3.
- **Categoría:** *Robótica & Embodied AI*
- **Validación:** `Despregado en Produción`
- **Organizaciones:** Figure AI; BMW Group (planta de Spartanburg, EE. UU.)
- **Descripción:** La robótica humanoide llevaba años en vídeos de demostración. En BMW Spartanburg, el humanoide Figure 02 trabajó once meses en carrocería: cogía chapas y las colocaba con precisión milimétrica en los útiles de soldadura. Cifras publicadas por Figure y BMW: turnos de 10 horas de lunes a viernes, más de 1.250 horas de funcionamiento, más de 90.000 piezas cargadas y contribución a más de 30.000 BMW X3. Es el primer despliegue de humanoides a escala de producción documentado en automoción. Matices: Figure rompió con OpenAI en 2025 y usa su propio modelo visión-lenguaje-acción (Helix); las cifras proceden de las propias empresas; y el robot se retiró tras el piloto, con Figure 03 evaluándose ya en logística.
- **Vídeo recomendado:** Figure AI (canal oficial) — resumen del despliegue en BMW → [buscar](https://www.youtube.com/results?search_query=Figure+02+BMW+Spartanburg+30000+X3) ⚠ ID sin verificar (la URL actual me parece sospechosa).
- **Tag UI:** `border-orange-500 text-orange-300`

### ID 6 — Razoamento formal: AlphaProof, o1 e as Olimpíadas
- **Título sugerido:** Pensar antes de responder
- **Subtítulo:** Da prata (2024) ao ouro (2025) na Olimpíada Internacional de Matemáticas.
- **Categoría:** *Matemáticas & Ciencias Formais*
- **Validación:** `Investigación de Fronteira`
- **Organizaciones:** Google DeepMind; OpenAI; comunidad Lean
- **Descripción:** Los modelos de lenguaje clásicos «contestan» de una pasada; los modelos de razonamiento gastan cómputo al responder (cadena de pensamiento, búsqueda y verificación). OpenAI o1 (2024) y o3 elevaron los resultados en ciencia y matemáticas. DeepMind unió IA y demostración formal: AlphaProof (refuerzo sobre Lean 4) y AlphaGeometry 2 resolvieron 4 de 6 problemas de la IMO 2024 (28/42, plata) con pruebas verificadas mecánicamente por el compilador, alcanzando puntuaciones equivalentes a medalla de oro en 2025. **Advertencia didáctica fundamental:** la IA NO ha resuelto ningún Problema del Milenio (Navier-Stokes de OpenAI sigue en controversia y no ha sido aceptado por el Clay Institute; Riemann y P vs NP siguen totalmente abiertos). El salto cualitativo real es la eliminación de alucinaciones deductivas mediante compiladores formales.
- **Vídeo recomendado:** Two Minute Papers — «DeepMind's New AI Looked At 100,000,000 Examples!» (~5 min, sobre AlphaProof/AlphaGeometry 2) → https://www.youtube.com/watch?v=QJtNQNgGLdM ✔ *(ID localizado en fuente externa con canal y título coincidentes)*.
- **Tag UI:** `border-purple-500 text-purple-300`

### ID 7 — GraphCast e WeatherNext
- **Título sugerido:** O tempo, calculado por unha rede neuronal
- **Subtítulo:** Máis dun día de antelación en furacáns, e modelos abertos para todos.
- **Categoría:** *Ciencias da Terra*
- **Organizaciones:** Google DeepMind y Google Research; ECMWF (AIFS); Centro Nacional de Huracanes de EE. UU. (NHC); Met Office
- **Descripción:** La predicción numérica clásica resuelve ecuaciones de física en superordenadores. GraphCast (DeepMind, Science, 2023), una red neuronal sobre grafos entrenada con décadas de reanálisis, predice 10 días de tiempo global en menos de un minuto con un solo TPU y superó al modelo operativo HRES del ECMWF en la mayoría de variables evaluadas. El ECMWF puso en operación su modelo AIFS en 2025. En agosto de 2026, DeepMind publicó en Nature WeatherNext (Cyclones), desarrollado con el NHC: gana más de un día de antelación en trayectoria, intensidad y vientos de ciclones (≈ una década de progreso) y se liberó en abierto (código y pesos). En 2025 ayudó al NHC a anticipar la intensificación rápida del huracán Melissa. Límite: los modelos de IA complementan, no sustituyen, a los meteorólogos ni a los avisos oficiales.
- **Vídeo recomendado:** Google DeepMind (canal oficial) — presentación de GraphCast / WeatherNext → [buscar](https://www.youtube.com/results?search_query=Google+DeepMind+GraphCast+WeatherNext+weather+forecasting) ⚠ ID sin verificar.
- **Tag UI:** `border-sky-500 text-sky-300`

### ID 8 — Fusión: IA domando o plasma
- **Título sugerido:** Aprender a controlar un sol en miniatura
- **Subtítulo:** Aprendizaxe por reforzo en tempo real dentro dun tokamak.
- **Categoría:** *Física & Espazo*
- **Organizaciones:** Google DeepMind; Swiss Plasma Center (EPFL)
- **Descripción:** Para que la fusión sea viable hay que confinar un plasma sobrecalentado con campos magnéticos que deben ajustarse miles de veces por segundo; un fallo provoca «disrupciones» que dañan el reactor. En 2022 (Nature), DeepMind y el Swiss Plasma Center entrenaron en simulación una política de aprendizaje por refuerzo profundo que controló en tiempo real las bobinas del tokamak TCV y creó formas de plasma —incluida una configuración con dos «gotas» simultáneas— que antes exigían diseños de control específicos y meses de trabajo. Es una demostración de control en un experimento, no de producción de energía neta. Impacto: acorta el desarrollo de controladores y apunta a futuros reactores como ITER. Nota para la interfaz: la cifra de «100 millones de grados» corresponde a reactores grandes, no al TCV. *Pendiente de actualizar con novedades 2025-26.*
- **Vídeo recomendado:** Google DeepMind (canal oficial) — «Accelerating fusion science through learned plasma control» o similar → [buscar](https://www.youtube.com/results?search_query=DeepMind+EPFL+tokamak+plasma+control+reinforcement+learning) ⚠ ID sin verificar.
- **Tag UI:** `border-indigo-500 text-indigo-300`

### ID 9 — Anthropic: Mapping the Mind e Computer Use
- **Título sugerido:** Abrir a caixa negra e darlle mans á IA
- **Subtítulo:** Millóns de conceptos localizados dentro do modelo; Claude manexando rato e teclado.
- **Categoría:** *Software & Axentes*
- **Organizaciones:** Anthropic
- **Descripción:** Dos avances de 2024 con efecto en cadena. (1) Interpretabilidad mecanicista: en «Mapping the Mind of a Large Language Model» (mayo de 2024), Anthropic usó autoencoders dispersos (SAE) para extraer millones de «características» interpretables (hasta ~34 millones en Claude 3 Sonnet), como la del puente Golden Gate: al amplificarla surgió «Golden Gate Claude». Mostró por primera vez que se pueden localizar y manipular conceptos dentro de un modelo comercial. (2) Computer Use (octubre de 2024): Claude interpreta capturas de pantalla y controla ratón y teclado, germen de los agentes que hoy operan navegadores, hojas de cálculo y entornos de desarrollo. Impacto: auditoría y seguridad (saber por qué un modelo responde lo que responde) y automatización de tareas de oficina. Transparencia: producto de la empresa que desarrolla a Claude.
- **Vídeo recomendado:** canal de Anthropic — «Mapping the Mind» / demostración de Computer Use → [buscar](https://www.youtube.com/results?search_query=Anthropic+computer+use+Claude+demo) ⚠ ID sin verificar (la URL actual no pude comprobarla).
- **Tag UI:** `border-blue-500 text-blue-300`

### ID 10 — AlphaEvolve, AlphaTensor e FunSearch
- **Título sugerido:** Algoritmos que a IA inventou
- **Subtítulo:** Rompeu un récord de 56 anos en multiplicación de matrices e aforra cómputo a Google.
- **Categoría:** *Matemáticas & Ciencias Formais*
- **Organizaciones:** Google DeepMind
- **Descripción:** Descubrir algoritmos nuevos era territorio exclusivo de matemáticos e ingenieros. AlphaTensor (Nature, 2022) usó refuerzo para hallar métodos de multiplicación de matrices más rápidos, y FunSearch (Nature, 2023) encontró un «cap set» de tamaño 512 en dimensión 8, mayor que el récord previo (496). AlphaEvolve (mayo de 2025) combina Gemini con búsqueda evolutiva: halló un algoritmo para multiplicar matrices complejas 4×4 con 48 multiplicaciones, el primer avance sobre Strassen (49) en 56 años para ese caso, y en ~50 problemas abiertos igualó el mejor resultado conocido en la mayoría y lo mejoró en torno a un 20 %. En producción: recuperó de media el 0,7 % del cómputo mundial de Google (planificador Borg) y aceleró un 23 % un núcleo de entrenamiento de Gemini (−1 % del tiempo total). En 2026 se ofrece a empresas vía Google Cloud.
- **Vídeo recomendado:** Two Minute Papers — «DeepMind's AlphaEvolve AI: History In The Making!» (~7,5 min) → https://www.youtube.com/watch?v=T0eWBlFhFzc ✔ *(ID localizado en fuente externa con canal y título coincidentes)*.
- **Tag UI:** `border-purple-500 text-purple-300`

### ID 11 — AlphaChip: IA que deseña chips
- **Título sugerido:** Chips deseñados como se fose un xogo
- **Subtítulo:** Plantas de circuíto en horas, usadas en tres xeracións de TPU… e cunha polémica científica.
- **Categoría:** *Hardware & Computación*
- **Organizaciones:** Google (Brain y DeepMind); MediaTek
- **Descripción:** Colocar los bloques de un chip (floorplanning) es un rompecabezas combinatorio que la ingeniería llevaba más de seis décadas intentando automatizar. En 2021 (Nature), investigadores de Google propusieron tratarlo como un juego y entrenar un agente de aprendizaje por refuerzo (después llamado AlphaChip) que genera plantillas en menos de seis horas, frente a semanas de trabajo humano. Google informa de su uso en las tres últimas generaciones de TPU (v5e, v5p, Trillium) y en CPU Axion; MediaTek lo adaptó a sus chips. Controversia (útil en clase): grupos académicos (Cheng, Kahng, Markov) cuestionan las comparaciones y la reproducibilidad; Nature publicó en 2024 una adenda y Google defiende sus resultados. Lección: un hito puede ser real en la industria y seguir en disputa científica.
- **Vídeo recomendado:** Google DeepMind (canal oficial) — AlphaChip → [buscar](https://www.youtube.com/results?search_query=Google+DeepMind+AlphaChip+chip+design+reinforcement+learning) ⚠ ID sin verificar.
- **Tag UI:** `border-slate-400 text-slate-300`

### ID 12 — AlphaGenome e OpenCRISPR
- **Título sugerido:** Ler e escribir o xenoma con IA
- **Subtítulo:** Predicir o efecto de mutacións no 98 % «escuro» do ADN e editores xenéticos que a natureza non inventou.
- **Categoría:** *Bioloxía & Medicina*
- **Organizaciones:** Google DeepMind; Profluent
- **Descripción:** El 98 % del genoma humano no codifica proteínas, pero contiene interruptores que regulan los genes y muchas variantes asociadas a enfermedad. AlphaGenome (DeepMind; Nature, 28 de enero de 2026) recibe hasta 1 millón de pares de bases y predice miles de propiedades moleculares (expresión, accesibilidad de la cromatina, empalme, contactos 3D) con resolución de base; igualó o superó a los mejores modelos externos en 25 de 26 evaluaciones de efecto de variantes. Unos 3.000 científicos de 160 países lo probaron en su vista previa. En paralelo, Profluent (Nature, 2025) usó modelos de lenguaje para generar editores CRISPR inexistentes en la naturaleza: OpenCRISPR-1 edita ADN humano con actividad comparable a SpCas9 y mayor especificidad, y se licencia abiertamente. Son herramientas de investigación; su uso clínico exigirá ensayos.
- **Vídeo recomendado:** Google DeepMind (canal oficial) — AlphaGenome → [buscar](https://www.youtube.com/results?search_query=Google+DeepMind+AlphaGenome) ⚠ ID sin verificar.
- **Tag UI:** `border-emerald-500 text-emerald-300`

### ID 13 — Interfaces cerebro-ordenador que falan
- **Título sugerido:** Devolver a voz
- **Subtítulo:** Case dous anos de uso diario, na casa, dunha neuropróstese de fala nun paciente con ELA.
- **Categoría:** *Bioloxía & Medicina*
- **Organizaciones:** UC Davis Health (Brandman, Stavisky), consorcio BrainGate, Stanford
- **Descripción:** Las personas con ELA pueden perder el habla conservando la intención de hablar. Los equipos de BrainGate y UC Davis implantan electrodos en la corteza motora del habla y decodifican la actividad neuronal con redes neuronales y modelos de lenguaje. En 2024 (NEJM) un participante alcanzó ~97 % de precisión con un vocabulario de 125.000 palabras; en 2025 (Nature), un sistema «cerebro-voz» sintetizó voz con un retardo de ~1/40 de segundo y entonación; en junio de 2026 (Nature Medicine) el mismo participante usó la interfaz en casa casi dos años: más de 3.800 horas, ~183.000 frases y casi 2 millones de palabras, a 56 palabras por minuto de media, y la utiliza para trabajar. Límites: pocos participantes, cirugía y mantenimiento técnico. Su responsable recibió el Premio Chen Institute–Science 2026.
- **Vídeo recomendado:** UC Davis Health (canal oficial) — neuroprótesis de habla en ELA → [buscar](https://www.youtube.com/results?search_query=UC+Davis+Health+brain-computer+interface+ALS+speech+Casey+Harrell) ⚠ ID sin verificar.
- **Tag UI:** `border-emerald-500 text-emerald-300`

### ID 14 — Deep Loop Shaping e ondas gravitacionais
- **Título sugerido:** Aquietar o universo para escoitalo
- **Subtítulo:** Ruído de control reducido entre 30 e 100 veces nun detector LIGO real.
- **Categoría:** *Física & Espazo*
- **Organizaciones:** Google DeepMind; Caltech/LIGO; Gran Sasso Science Institute (GSSI)
- **Descripción:** Los detectores de ondas gravitacionales miden variaciones de una fracción del tamaño de un protón; cualquier vibración, incluso olas a 160 km, arruina la medida. Un obstáculo clave es el ruido que inyecta el propio sistema de control que estabiliza los espejos. Deep Loop Shaping (Science, septiembre de 2025) usa aprendizaje por refuerzo con recompensas en el dominio de la frecuencia y, en pruebas reales en LIGO Livingston, redujo entre 30 y 100 veces el ruido de control en el bucle más difícil, por debajo del límite cuántico. Es una prueba de concepto con una hora de datos; aplicada a todos los bucles, podría permitir detectar cientos de fusiones más al año, y sirve también en aeroespacial y robótica. Complemento: PRIMO (2023) reconstruyó con IA la imagen del agujero negro M87* del Event Horizon Telescope.
- **Vídeo recomendado:** Google DeepMind (canal oficial) — «Using AI to perceive the universe in greater depth» → [buscar](https://www.youtube.com/results?search_query=DeepMind+Deep+Loop+Shaping+LIGO) ⚠ ID sin verificar.
- **Tag UI:** `border-indigo-500 text-indigo-300`

### ID 15 — Erdős e a matemática de investigación
- **Título sugerido:** A IA entra na matemática de investigación
- **Subtítulo:** Unha conxectura de Erdős de 1946 refutada e nove problemas abertos resoltos con proba formal.
- **Categoría:** *Matemáticas & Ciencias Formais*
- **Organizaciones:** OpenAI; Google DeepMind (AlphaProof Nexus); Lean/Mathlib; comunidad (T. Tao, T. Bloom, W. Sawin)
- **Descripción:** Hasta 2025, la IA brillaba en olimpiadas, no en problemas de investigación. En 2026 cambió el panorama. (1) Mayo: un modelo de razonamiento general de OpenAI refutó la conjetura de la distancia unitaria de Erdős (1946): construyó familias de n puntos del plano con ≈ n^(1+δ) pares a distancia 1 mediante teoría algebraica de números, con δ ≈ 0,014 refinado por Will Sawin (Princeton). Tim Gowers (Medalla Fields) lo calificó de hito y lo aceptaría en una revista de primer nivel. (2) AlphaProof Nexus (DeepMind; arXiv en mayo, Science en octubre): Gemini 3.1 Pro + Lean resolvió 9 de 353 problemas de Erdős abiertos y formalizados (dos de 1970) y 44 de 492 conjeturas de la OEIS, con pruebas verificadas por Lean. Matiz: parte de los resultados de IA sigue sin revisión por pares y hay disputas de crédito.
- **Vídeo recomendado:** conferencia/entrevista de Tim Gowers o Terence Tao sobre IA y matemáticas, o canal Quanta Magazine / Numberphile → [buscar](https://www.youtube.com/results?search_query=Gowers+AI+Erd%C5%91s+unit+distance+conjecture) ⚠ ID sin verificar.
- **Tag UI:** `border-purple-500 text-purple-300`

### ID 16 — Axentes de software: SWE-bench
- **Título sugerido:** Da autocompletación a delegar o traballo
- **Subtítulo:** De ~2 % a >95 % en incidencias reais de GitHub (con rigor metodolóxico ante auditorías).
- **Categoría:** *Software & Axentes*
- **Validación:** `Investigación de Fronteira`
- **Organizaciones:** Anthropic, DeepSeek, OpenAI, Google (ranking de terceros: Vals.ai); autores de SWE-bench (Princeton)
- **Descripción:** SWE-bench (2023) pide a un modelo que resuelva incidencias reales de repositorios abiertos de Python (Django, scikit-learn…) de modo que pasen las baterías de tests. En 2023, el mejor sistema resolvía alrededor del 2 %. En 2026, los agentes con herramientas (editar archivos, ejecutar tests, iterar) superan el 95 % en el subconjunto verificado de 500 tareas. **Cautela metodológica esencial:** en febrero de 2026 OpenAI publicó una auditoría detallada de SWE-bench Verified y recomendó prudencia, señalando tests defectuosos en el benchmark y posible contaminación o exposición de soluciones en los datos de entrenamiento. En evaluaciones profesionales más blindadas (SWE-bench Pro), los agentes rondan el 80 %. El hito no debe enseñarse como «autonomía absoluta sin ingenieros», sino como un cambio de paradigma hacia la delegación de tareas completas bajo supervisión humana.
- **Vídeo recomendado:** charla/presentación de los autores de SWE-bench o análisis de un canal técnico (p. ej., Computerphile, AI Explained) → [buscar](https://www.youtube.com/results?search_query=SWE-bench+explained+AI+coding+agents) ⚠ ID sin verificar.
- **Tag UI:** `border-blue-500 text-blue-300`

### ID 17 — Waymo: conducción sen condutor
- **Título sugerido:** O taxi que non ten condutor
- **Subtítulo:** Máis de 500.000 viaxes de pago por semana e moitos menos choques con lesións.
- **Categoría:** *Robótica & Embodied AI*
- **Organizaciones:** Waymo (Alphabet); Swiss Re; Insurance Institute for Highway Safety (IIHS)
- **Descripción:** Conducir sin conductor llevaba años en «casi listo». Waymo opera robotaxis sin nadie al volante: en 2026 supera los 500.000 viajes de pago por semana en unas diez ciudades de EE. UU., con 220 millones de millas sin conductor hasta marzo de 2026 y ~4 millones de millas semanales. Según Waymo, sus vehículos tuvieron un 94 % menos de choques con lesiones graves o mortales que conductores humanos en las mismas zonas; el estudio independiente del IIHS halló un 81 % menos de choques con lesiones, y el análisis con la reaseguradora Swiss Re, un 88 % menos de reclamaciones por daños materiales y un 92 % menos por lesiones corporales. Matices: operan en áreas delimitadas y buena parte de los datos los publica la propia empresa; el objetivo de 1 millón de viajes semanales a fin de 2026 no está confirmado.
- **Vídeo recomendado:** Gustavo Entrala — «Los ROBOTAXIS ROBAN ya el 27% del mercado a UBER en San Francisco» → https://www.youtube.com/watch?v=8Szm56z58EM ✔ *(ID verificado)*.
- **Tag UI:** `border-orange-500 text-orange-300`

### ID 18 — Titorías de IA que melloran a aprendizaxe
- **Título sugerido:** Un titor para cada estudante
- **Subtítulo:** Seis semanas con IA ≈ 1,5-2 anos de escolaridade (ensaio aleatorizado en Nigeria), se hai boa pedagoxía.
- **Categoría:** *Educación & Sociedade*
- **Organizaciones:** Banco Mundial (De Simone et al.); Harvard (Kestin et al.); Univ. de Pensilvania (Bastani et al.)
- **Descripción:** Las tutorías individuales son una de las intervenciones educativas más eficaces (≈0,29 desviaciones típicas en 89 ensayos), pero escasas y caras. En el estado de Edo (Nigeria), el Banco Mundial hizo un ensayo aleatorizado en nueve institutos públicos (~800 estudiantes): seis semanas de sesiones extraescolares en parejas con Copilot (GPT-4), con supervisión docente e indicaciones pensadas para razonar, dieron ganancias en inglés equivalentes a 1,5-2 años de escolaridad típica, por encima de ~80 % de las intervenciones comparables. En Harvard, un tutor de IA bien diseñado duplicó el aprendizaje en física frente a una clase de aprendizaje activo (Scientific Reports, 2025). Advertencia: en un ensayo en Türkiye, un chatbot sin pedagogía mejoró el rendimiento mientras se usaba, pero lo empeoró un 17 % al retirarlo. El diseño y el docente son la clave.
- **Vídeo recomendado:** Banco Mundial (canal oficial) — «From Chalkboards to Chatbots» / ensayo de Nigeria → [buscar](https://www.youtube.com/results?search_query=World+Bank+Nigeria+AI+tutoring+Edo+State+Copilot) ⚠ ID sin verificar.
- **Tag UI:** `border-pink-500 text-pink-300`

### ID 19 — Mamografía asistida por IA (MASAI)
- **Título sugerido:** Unha segunda mirada que non se cansa
- **Subtítulo:** Primeiro ensaio aleatorizado de IA nun programa de cribado: máis cancros detectados e menos carga de lectura.
- **Categoría:** *Bioloxía & Medicina*
- **Organizaciones:** Univ. de Lund (Suecia); ScreenPoint Medical (sistema Transpara)
- **Descripción:** El cribado de mama depende de radiólogos que leen miles de mamografías, con falta de personal en muchos países. MASAI es el primer ensayo aleatorizado de IA en un programa de cribado: más de 105.000 mujeres en Suecia, con lectura asistida por IA frente a la doble lectura estándar. Resultados: un 29 % más de cánceres detectados sin más falsos positivos y un 44 % menos de carga de lectura (estudios intermedios), y en enero de 2026 (The Lancet) el resultado principal: 1,55 frente a 1,76 cánceres de intervalo por 1.000 mujeres (−12 %), estadísticamente «no inferior», con menos cánceres de intervalo de características desfavorables. Límites: un solo país, un tipo de equipo y un sistema de IA; falta la mortalidad a largo plazo. Los autores preparan un ensayo en Etiopía con ecografía asistida por IA.
- **Vídeo recomendado:** Univ. de Lund / The Lancet — resumen del ensayo MASAI → [buscar](https://www.youtube.com/results?search_query=MASAI+trial+AI+mammography+screening+Lancet+Lund) ⚠ ID sin verificar.
- **Tag UI:** `border-emerald-500 text-emerald-300`

### ID 20 — Antibióticos xerados por IA
- **Título sugerido:** Deseñar antibióticos que non existían
- **Subtítulo:** Dúas moléculas inéditas eficaces contra gonorrea resistente e SARM en ratos.
- **Categoría:** *Bioloxía & Medicina*
- **Organizaciones:** MIT (James Collins), Broad Institute, Wyss Institute; Phare Bio
- **Descripción:** La resistencia a los antibióticos está asociada a casi 5 millones de muertes al año y llevamos décadas sin clases realmente nuevas. El equipo de Collins (Cell, agosto de 2025) pasó de «cribar» bibliotecas existentes —como halicina (2020) o abaucina (2023)— a «generar» moléculas que no existen: dos algoritmos generativos diseñaron más de 36 millones de compuestos, filtrados por predictores de actividad antibacteriana, toxicidad y novedad. Se sintetizaron los mejores: NG1, contra Neisseria gonorrhoeae resistente, y DN1, contra SARM (MRSA), estructuralmente distintos de los antibióticos conocidos; ambos funcionaron en cultivo y en ratones. Estado: preclínico, aún lejos de los pacientes (Phare Bio trabaja en optimizarlos). Impacto potencial: ampliar el espacio químico explorable frente a una de las mayores amenazas sanitarias.
- **Vídeo recomendado:** MIT / Collins Lab — IA y antibióticos → https://www.youtube.com/watch?v=oxVzNcGP7M8 ✔ *(ID verificado: TED talk Jim Collins)*.
- **Tag UI:** `border-emerald-500 text-emerald-300`

### ID 21 — Claude Mythos e a Ciberseguridade Autónoma
- **Título sugerido:** Ciberdefensa a velocidade de máquina e o dilema do dobre uso
- **Subtítulo:** Detección de vulnerabilidades de día cero e o primeiro modelo con acceso restrinxido por seguridade nacional (2026).
- **Categoría:** *Ciberseguridade & Software*
- **Organizaciones:** Anthropic; UK AI Security Institute (AISI); DARPA (AIxCC); Project Glasswing
- **Descripción:** La ciberseguridad cambió de era con la aparición de modelos de frontera dotados de razonamiento autónomo profundo sobre código binario, ingeniería inversa y protocolos de red. Durante las pruebas de evaluación del UK AI Security Institute (AISI) y competiciones como el AI Cyber Challenge (AIxCC) de DARPA, el modelo Claude Mythos demostró una capacidad inédita para descubrir de forma totalmente autónoma vulnerabilidades desconocidas (*zero-days*) en sistemas operativos y pilas de software crítico, trazando en segundos cadenas complejas de explotación que llevarían semanas a equipos humanos de élite. Ante su carácter de estricto doble uso —capaz de parchear y blindar la infraestructura mundial, pero también de automatizar ciberataques militares a escala masiva—, Anthropic tomó la decisión histórica de retener su lanzamiento público abierto y articular el programa de acceso restringido *Project Glasswing* (abril de 2026), bifurcando sus modelos en dos ramas: Claude Fable (versión pública comercial con filtros estrictos que bloquean cualquier generación de exploits) y Claude Mythos (reservado para auditoría defensiva en entidades gubernamentales e infraestructuras críticas). El hito consagró la necesidad ineludible de la ciberdefensa automatizada continua a velocidad de máquina.
- **Vídeo recomendado:** DEF CON 33 — Winners of DARPA’s AI Cyber Challenge (AIxCC) → https://www.youtube.com/watch?v=touJ5uLlXjQ ✔ *(ID verificado)*.
- **Tag UI:** `border-rose-500 text-rose-300`

---

## 3. Sección especial: A Fronteira Matemática e os Problemas do Milenio

**Para o profesorado — síntese.** Durante moito tempo, a IA foi un recoñecedor estatístico de patróns: un modelo que adiviña a seguinte palabra ou clasifica imaxes sen «saber» por que algo é certo. En matemáticas ese enfoque tiña un límite evidente: unha proba case correcta é unha proba falsa. O cambio chegou ao combinar tres pezas. Primeiro, **modelos de razoamento** que dedican cómputo a pensar paso a paso (o1/o3, Gemini Deep Think). Segundo, **proba formal**: asistentes como **Lean 4** actúan como árbitro incorruptible, porque o seu núcleo comproba cada inferencia; así, a IA pode equivocarse mil veces e só conta a proba que o verificador acepta (AlphaProof, 2024; AlphaProof Nexus, 2026). Terceiro, **busca de construcións** (FunSearch, AlphaEvolve) que propón obxectos matemáticos novos que despois se comproban. O resultado é unha IA que pasou de resolver problemas de olimpíada (plata en 2024, ouro en 2025) a refutar a conxectura da distancia unitaria de Erdős (maio de 2026) e a resolver problemas abertos con certificación formal.

**Que NON está resolto (estado a novembro de 2026).** Ningún Problema do Milenio foi resolto de forma aceptada. O caso máis vistoso é **Navier–Stokes**: en setembro de 2026 OpenAI presentou un manuscrito de 166 páxinas e unha formalización en Lean que establecería explosión en tempo finito, tras un esforzo de ~10.000 axentes durante 88 horas. O **Clay Mathematics Institute non o aceptou** e segue listando o problema como aberto; varios expertos sinalan que a proba parece depender dunha versión con forzamento (distinta do enunciado clásico), un artigo de Bastounis, Circelli e Hansen sostén que o código Lean non se corresponde coa proba en linguaxe natural, e hai unha disputa de prioridade con quen abriu o camiño (Córdoba, Martínez-Zoroa, Buckmaster, Alpöge). Antes, DeepMind e colaboradores (2025) usaron redes neuronais con restricións físicas (PINNs) para descubrir novas familias de singularidades inestables en ecuacións de fluídos: un avance real, pero non unha solución do problema.

**Ideas para a aula.** (1) Que garante unha proba formal e que non (a pregunta «formalizaches o enunciado correcto?» segue a ser humana). (2) Diferenza entre verificar, comprender e atribuír crédito. (3) Por que a revisión por pares importa: DeepMind publicou en *Science*; outros resultados seguen só en repositorios. (4) Comparar «resolver exercicios» con «descubrir», e discutir o rol do matemático (Tao, Gowers, Buzzard) como director e verificador, non como espectador.

---

## 4. Banquillo (candidatos que quedaron fuera del Top 20)

- **DeepSeek-R1 (China, Nature 2025):** razonamiento por refuerzo con pesos abiertos; clave para la diversidad de actores y la democratización.
- **Evo 2 (Arc Institute, Stanford, NVIDIA):** modelo abierto de lenguaje genómico para todos los dominios de la vida.
- **ESM3 (EvolutionaryScale):** modelo generativo de proteínas con una proteína fluorescente nueva diseñada por IA.
- **ICPC/IMO 2025 en lenguaje natural:** ya integrado en el hito 6.
- **Nobel de Física 2024 (Hopfield y Hinton):** base teórica del aprendizaje profundo; contexto histórico más que «caso de éxito».

*Fin del documento. Antes de publicar: verificar los enlaces de vídeo marcados con ⚠ y contrastar las cifras con las fuentes citadas en cada ficha.*
