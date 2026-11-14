# Rexistro de Actualización: Presentación «01_Iniciacion_Docente»
**Edición do Curso 2026–2027 · Data de corte: Novembro de 2026 (Nov-26)**

Este documento recolle de forma estruturada todos os cambios, decisións de deseño, taxonomías e fontes aplicadas na modernización integral do curso de iniciación docente en Intelixencia Artificial. O seu propósito é servir de guía de referencia e mantemento para futuras actualizacións en cursos vindeiros.

---

## 1. Convencións Globais e Arquitectura Técnica

1. **Identificador temporal:**
   - Incorporouse o cancelo/distintivo `Nov-26` na portada de `index.html`, na cabeceira de `Introducción.html`, na galería de `Casos_Éxito.html` e nos obradoiros para que o alumnado e profesorado teñan clara a vixencia do estado da arte.
2. **Pautas lingüísticas:**
   - **Galego normativo:** Títulos, subtítulos, categorías, textos expositivos das diapositivas, interface de usuario e etiquetas interactivas.
   - **Castelán:** Documentación técnica de apoio, estudos de mercado, notas de investigación e rexistros de cambios.
3. **Pila tecnolóxica e deseño visual:**
   - Framework de diapositivas: Reveal.js en `index.html`.
   - Vistas modulares interactivas: React 18 (standalone via Babel), Tailwind CSS, Iconas SVG inline, variables de cor CSS (`--bg-dark`, `--card-bg`, `--accent-orange`, `--accent-gold`, etc.).
   - Tipografía oficial: *Open Sans* (300, 400, 600, 800).
   - Política de medios: Imaxes locais en carpetas relativas `./Img/`, formato panorámico/aspect-card.
   - Xestión de vídeos: Apertura directa mediante botón accesible en nova pestana de YouTube (`target="_blank" rel="noopener noreferrer"`) para evitar o **Erro 153** derivado das restricións de inserción de iframes en contornas locais `file:///`.

---

## 2. Módulo 1: Introdución e Fundamentos (`Introducción.html`)

### A. Cambio de Paradigma da Computación
- Mantense o contraste histórico en tres fitos ilustrados co mesmo estilo visual retro-futurista:
  1. **Computación Clásica / Programación:** Regras + Datos = Resultados deterministas.
  2. **Aprendizaxe Automática / IA Clásica:** Datos + Resultados = Modelos estatísticos.
  3. **IA Axéntica (Novo Fito 2026):** Ciclo continuo de Percepción → Razoamento (CoT) → Uso de Ferramentas / MCP → Acción no Mundo Real → Reflexión. Ilustrado co lazo de Moebius e circuítos integrados.

### B. Liña de Tempo Histórica Reordenada
- Corrixiuse a orde cronolóxica dos fitos fundacionais.
- **Engadido clave:** O lanzamento público de **ChatGPT (30 de novembro de 2022)** como o punto de inflexión da IA de consumo e xeralista, abrindo o camiño dende os laboratorios á sociedade e ás aulas.

---

## 3. Módulo 2: Casos de Éxito Reais da IA (`Casos_Éxito.html`)

A sección pasou de 9 fichas a unha **galería completa de 21 fitos históricos verificados**, organizados en 8 áreas temáticas.

### A. Taxonomía de Rigor Científico (Badges de Validación)
Para fomentar o espírito crítico nos docentes e evitar confundir demostracións comerciais con evidencia científica, cada ficha incorpora unha etiqueta visible na cara frontal e no reverso:

| Distintivo | Cor UI | Significado Metodolóxico | Exemplos Implementados |
| :--- | :--- | :--- | :--- |
| **`DESPREGADO EN PRODUCIÓN`** | Esmeralda / Verde | Operativo en contornas reais masivas, industriais ou servizos públicos. | Waymo, Figure 02 en BMW, GraphCast (ECMWF), AlphaChip (Google), Algoritmos en servidores Borg. |
| **`ENSAIO CLÍNICO REAL`** | Rosa / Maxenta | Validado en humanos mediante estudos controlados con publicación de impacto. | MASAI (The Lancet), Rentosertib (Fase IIa/III), Neuropróteses BCI en ELA, Titorías Banco Mundial/Harvard. |
| **`DEMOSTRADO EN LABORATORIO`** | Ámbar / Amarelo | Proba de concepto validada experimentalmente con éxito en contorna científica. | AlphaFold 3, AlphaGenome/OpenCRISPR, Antibióticos MIT, Baterías PNNL, Tokamak EPFL, Vesuvius/Nazca, LIGO. |
| **`INVESTIGACIÓN DE FRONTEIRA`** | Púrpura / Violeta | Avances en razoamento formal, matemáticas, interpretabilidade ou ciberdefensa. | AlphaProof (IMO), Erdős (Lean 4), SWE-bench, Anthropic Computer Use, Claude Mythos. |

### B. Listaxe dos 21 Fitos Implementados
1. **AlphaFold 3 & ESMFold** *(Bioloxía & Medicina · Demostrado)*: +200M estruturas abertas, Nobel de Química 2024.
2. **AlphaGenome e OpenCRISPR** *(Bioloxía & Medicina · Demostrado)*: Interpretación do 98% non codificante e editores sintéticos.
3. **Rentosertib (Insilico Medicine)** *(Bioloxía & Medicina · Ensaio Clínico)*: Primeiro fármaco deseñado por IA en Fase III.
4. **Antibióticos Xerados por IA** *(Bioloxía & Medicina · Demostrado)*: Moléculas NG1 e DN1 (MIT/Cell 2025) contra gonorrea e SARM.
5. **Mamografía con IA: Estudo MASAI** *(Bioloxía & Medicina · Ensaio Clínico)*: 105.000 mulleres en Suecia (The Lancet), +29% detección.
6. **Neuropróteses de Fala en ELA (BCI)** *(Bioloxía & Medicina · Ensaio Clínico)*: UC Davis/BrainGate, 2 anos de uso domiciliario continuo.
7. **GraphCast e WeatherNext** *(Ciencias da Terra · Despregado)*: Previsión global en 60 s e +1 día de antelación en furacáns.
8. **Waymo: Conducción sen Condutor** *(Robótica · Despregado)*: 500.000 viaxes semanais comerciais, −81% a −94% lesións (IIHS/Swiss Re). Vídeo: Gustavo Entrala en San Francisco.
9. **Figure 02 na Planta de BMW** *(Robótica · Despregado)*: 11 meses en Spartanburg, 1.250 h operativas, 30.000 vehículos X3 montados.
10. **Baterías Sólidas: Microsoft & PNNL** *(Enerxía · Demostrado)*: 32M materiais en 80 h, electrólito N2116 con 70% menos de litio.
11. **Fusión Nuclear: Tokamaks** *(Física · Demostrado)*: Control magnético en tempo real no reactor TCV (EPFL/DeepMind).
12. **Deep Loop Shaping en LIGO** *(Física · Demostrado)*: Ruído de control reducido entre 30 e 100 veces por baixo do límite cuántico.
13. **Vesuvius Challenge e Xeoglifos de Nazca** *(Historia · Demostrado)*: Lectura íntegra do papiro PHerc. 1667 (xuño 2026) e 303 novos xeoglifos en Nazca (PNAS 2024).
14. **Razoamento Formal: AlphaProof e o1** *(Matemáticas · Investigación)*: Prata IMO 2024 e ouro 2025 con Lean 4.
15. **Algoritmos Descubertos por IA** *(Matemáticas · Despregado)*: FunSearch e AlphaEvolve (récord de Strassen batido tras 56 anos, aforro do 0,7% en Google).
16. **AlphaChip: Deseño de Chips** *(Hardware · Despregado)*: Floorplanning en horas en TPUs de Google (v5e, v5p, Trillium) e CPU Axion.
17. **Erdős e a Matemática con Lean 4** *(Matemáticas · Investigación)*: Conxectura da distancia unitaria (1946) refutada e 9 problemas abertos resoltos.
18. **Axentes de Software: SWE-bench** *(Software · Investigación)*: Do 2% ao >95% en GitHub, con aviso crítico pola auditoría de OpenAI de febreiro de 2026 sobre contaminación e tests defectuosos.
19. **Anthropic: Computer Use e Mapeo Mental** *(Software · Investigación)*: Autoencoders esparsos (SAEs) e control de interfaces de escritorio.
20. **Claude Mythos e a Ciberdefensa** *(Ciberseguridade · Investigación)*: Descubrimento de zero-days, Project Glasswing e dilema do dobre uso militar.
21. **Titorías de IA con Pedagoxía** *(Educación · Ensaio Clínico)*: Banco Mundial (Nigeria) e Harvard demostrando ganancia equivalente a 1,5–2 anos de escolaridade con deseño socrático.

### C. Sección Especial Didáctica: A Fronteira Matemática e os Problemas do Milenio
- Incluído un banner despregable interactivo con tres leccións para a docencia:
  1. *A Tríade do Razoamento Formal:* Por que un compilador formal (Lean 4) elimina a alucinación.
  2. *Estado real dos Problemas do Milenio:* Aclaración taxativa de que **ningún Problema do Milenio está resolto por IA** (o traballo de OpenAI sobre Navier-Stokes segue en controversia polo forzamento matemático; Riemann e P vs NP seguen abertos).
  3. *O Rol Humano:* O matemático actúa como director de orquestra; a IA apoia o descubrimento pero non substitúe a formulación nin a comprensión.

---

## 4. Módulo 3: Obradoiros Prácticos (`Talleres`)

Renovación completa baseada no estudo de mercado comparativo. Pásase de 4 obradoiros con ferramentas que quedaron desfasadas a **5 obradoiros interactivos con 29 tarxetas actualizadas**:

### 1. Taller de LLMs e Razoamento (`Taller_LLM.html` · 8 tarxetas)
- **GPT-6 (OpenAI):** Razoamento Sistema 2 adaptativo e multimodalidade de baixa latencia.
- **Claude 5.5 (Anthropic):** Capacidade analítica profunda, fiabilidade textual e uso de ferramentas.
- **Gemini 4 (Google):** Xigantesca xanela de contexto (millóns de tokens) e integración multimodal nativa.
- **Gemini Notebook (NotebookLM):** Asistente de estudo, podcasts xerativos e síntese documental con citas.
- **Perplexity Pro:** Motor de busca e investigación fundamentada con verificación de fontes primarias.
- **DeepSeek V4:** Razoamento de alta eficiencia e pesos abertos que revolucionou o ecosistema.
- **Qwen 3.8 (Alibaba):** Líder global en código aberto e soporte multilingüe avanzado.
- **Kimi / GLM:** Fronteira en contexto ultra-longo e procesamento integral de documentos complexos.

### 2. Taller de Imaxe e Ilustración (`Taller_Imagen.html` · 6 tarxetas)
- **GPT Image (OpenAI):** Edición semántica e control de texto perfecto dentro da ilustración.
- **Nano Banana:** Ilustración rápida e eficiente de nova xeración integrada en fluxos web.
- **Midjourney v8:** Máxima calidade plástica, cinematográfica e coherencia estilística artística.
- **Ideogram 4:** Excelencia tipográfica, creación de carteis e diagramas educativos lexibles.
- **Recraft v4:** Ilustración vectorial profesional (.SVG), deseño de iconas e paletas cromáticas.
- **FLUX.2 (Black Forest Labs):** Motor de pesos abertos de última xeración con máxima fidelidade anatómica.

### 3. Taller de Música e Audio (`Taller_Musica.html` · 5 tarxetas)
- **Suno (v5.5/v6):** Composición vocal e instrumental completa con letras en galego e arranxos ricos.
- **AIVA (AIVA Technologies):** Composición orquestal, clásica e bandas sonoras con descarga de pistas separadas, arquivos MIDI e partituras editables para docencia musical.
- **ElevenLabs Voice:** Clonación de voz de calidade de estudio, dobraxe emocional e avatares acústicos.
- **Stable Audio 3.0:** Deseño de efectos sonoros ambientais, paisaxes acústicas e texturas instrumentais con licenza limpa.
- **Google Lyria (3.5):** Motor xerativo musical avanzado de DeepMind centrado en acompañamentos interactivos e marcas SynthID.
- *Aviso docente:* Desaconséllase Udio ao desactivar as descargas de audio e stems en 2026; Beatoven e MusicFX fican integrados ou superados.

### 4. Taller de Vídeo e Animación (`Taller_Video.html` · 5 tarxetas)
- **Google Veo 3.1:** Vídeo fotorrealista de alta resolución 1080p con audio integrado nativo e coherencia física ao prompt.
- **Kling AI (4.0):** Dinámica física hiperrealista, control de movemento e tomas continuas de ata 30 segundos.
- **Runway Gen-4.5:** Cámara virtual, dirección de escena e ferramentas de posprodución profesional multicapa.
- **Luma Dream Machine (Ray3.14):** Coherencia visual fotorrealista, xeración nativa a 1080p e control cinemático de transformacións.
- **HeyGen & Hedra:** Avatares docentes con sincronización labial perfecta en +175 linguas (HeyGen) e animación expresiva de calquera personaxe ou retrato histórico dende pistas de voz (Hedra).
- *Aviso histórico:* Retirada definitiva de Sora tras o peche da súa web/app (abril 2026) e da súa API (setembro 2026).

### 5. NOVO Taller 5: IA de Escritorio e Harness Axéntico (`Taller_Escritorio.html` · 6 tarxetas)
Novo taller creado para responder ao desprazamento do traballo dende a pestana do navegador cara á contorna de escritorio e a execución axéntica:
- **Concepto de Harness e MCP:** O modelo non actúa só; o *harness* é o arnés operativo que lle achega ferramentas de sistema, memoria e permisos. O estándar aberto **MCP (Model Context Protocol)** permite conectar cartafoles, bases de datos e ferramentas sen copiar e pegar contexto a man.
- **Claude Desktop:** Axente de escritorio con soporte nativo de servidores MCP.
- **ChatGPT Desktop & Work:** Integración nativa no sistema operativo con captura contextual de ventás e tarefas complexas.
- **Google Antigravity 2.0:** Contorna de axentes autónomos con soporte de ferramentas locais e espazos de traballo.
- **Cursor & IDEs Axénticos:** Asistentes de desenvolvemento que legan proxectos enteiros e execución terminal.
- **LM Studio / Ollama:** Execución 100% local e privada de modelos sen enviar datos a servidores externos.
- **AnythingLLM:** Xestión documental corporativa e RAG privado de escritorio con cifrado local.
- **Compoñentes docentes adicionais:**
  - *Banner dobre didáctico:* Definición de Harness/MCP á esquerda + Alerta de Seguridade e RGPD á dereita.
  - *Tres Misións Prácticas Docentes:* 1) Organización de materiais didácticos; 2) RAG privado con apuntes; 3) Axente de avaliación local sen subida a servidores na nube.
- **Integración na navegación:** Ligazón de acceso directo `#/taller-escritorio` engadida ao menú lateral e ao carrusel Reveal.js en `index.html`.

---

## 5. Arquivos Modificados e Creados Nesta Revisión

- `2026-27/01_Iniciacion_Docente/index.html` (Navegación e slides de Reveal.js actualizados con Nov-26 e Taller 5).
- `2026-27/01_Iniciacion_Docente/Introducción/Introducción.html` (Novo paradigma Moebius + liña de tempo con ChatGPT 2022).
- `2026-27/01_Iniciacion_Docente/Éxitos/Casos_Éxito.html` (21 fichas con badges de rigor científico, banner matemático e ligazóns directas a YouTube).
- `2026-27/01_Iniciacion_Docente/Talleres/Taller_LLM.html` (8 tarxetas actualizadas).
- `2026-27/01_Iniciacion_Docente/Talleres/Taller_Imagen.html` (6 tarxetas actualizadas).
- `2026-27/01_Iniciacion_Docente/Talleres/Taller_Musica.html` (4 tarxetas actualizadas).
- `2026-27/01_Iniciacion_Docente/Talleres/Taller_Video.html` (5 tarxetas actualizadas).
- `2026-27/01_Iniciacion_Docente/Talleres/Taller_Escritorio.html` (Novo taller con 6 tarxetas, alerta RGPD e misións).
- `2026-27/Hitos_IA_Top20.md` (Documento mestre de referencia cos 21 fitos e a investigación validada).
- `2026-27/Estudio_Mercado_Obradoiros_IA.md` (Estudo de mercado completo dos 5 obradoiros).
- `2026-27/01_Iniciacion_Docente/REGISTRO_ACTUALIZACION_2026_27.md` (Este documento).
