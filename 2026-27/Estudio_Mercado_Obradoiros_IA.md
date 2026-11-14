# Estudio_Mercado_Obradoiros_IA · Iniciación á IA no Ensino (edición 2026-2027)

**Estado del mercado a 13 de noviembre de 2026.**
Convención de idioma: análisis en español; nombres de obradoiros, categorías y frases síntesis de tarjeta en gallego; prompts de demostración en gallego (listos para el aula).

---

## 0. Avisos de método (léelos antes de usar el informe)

1. **Fuentes.** Mezclo prensa especializada, documentación de fabricantes y comparativas de blogs. Muchas comparativas de 2026 son material SEO con **nomenclaturas contradictorias** (p. ej., Ideogram aparece como 3.0, 4 y 4.5; Flux como 2 y 3; Gemini 4 «Argon/Carbon» solo me consta por agregadores). **Confirma cada número de versión en la web oficial antes de publicar la tarjeta.**
2. **Enlaces.** Los URL de abajo son los dominios oficiales que conozco; **no los he abierto en esta sesión**. Marca «verificado en» la fecha en que los abras tú.
3. **Precios.** Cambian por trimestre. Se citan como orientación (otoño de 2026).
4. **Conflicto de interés declarado.** Claude/Anthropic aparece en varios apartados y yo soy Claude. He intentado contrastar con terceros, pero conviene una segunda lectura de esas fichas.
5. **Cambios de nomenclatura detectados en el prompt** (tu inventario está desfasado en estos puntos):
   - **OpenAI Operator**: retirado en agosto de 2025 y absorbido por *ChatGPT Agent*. **ChatGPT Atlas** (navegador) también se cerró: dejó de funcionar el 9 de agosto de 2026.
   - **OpenAI Sora**: OpenAI anunció su cierre en marzo de 2026; la app cerró el 26 de abril y la API el 24 de septiembre de 2026. **Hay que retirar la tarjeta.**
   - **NotebookLM** pasó a llamarse **Gemini Notebook** (16 de julio de 2026).
   - **Windsurf** pasó a ser **Devin Desktop** (Cognition).
   - **Codex** se integró en la app de escritorio de ChatGPT (9 de julio de 2026), con modos Chat / Work / Codex.
   - **Antigravity 2.0** (19 de mayo de 2026) es ya una app de escritorio independiente.
   - **DALL-E** y **Imagen 3** ya no son la cara visible de OpenAI y Google en imagen (ver Obradoiro 2).
   - Series obsoletas en tus tarjetas: Claude 3.5/3.7, ChatGPT o1/o3, Qwen 2.5, Runway Gen-3.
6. **Afirmaciones a corregir en el texto de las tarjetas:** NotebookLM *no* está «libre de alucinaciones»: ancla las respuestas en tus fuentes y cita, pero puede equivocarse. Y «privacidad offline absoluta» solo es cierta si el modelo se ejecuta en local.

---

## 1. Resumen ejecutivo

### 1.1 Hallazgos clave

- **Los generalistas absorben la «capa de texto, código y análisis»**, y en imagen el líder en votación ciega es hoy un modelo integrado en un chat (GPT Image 2.x en ChatGPT; Nano Banana en Gemini). Quedan **diferenciales reales** en estética (Midjourney), pesos abiertos y control (FLUX), vector (Recraft) y tipografía (Ideogram), aunque estos dos últimos se estrechan: GPT Image 2.6 (4-nov-2026) ya genera SVG y GIF animados.
- **En audio, el «moat» ya no es técnico sino jurídico.** Los sellos pactaron con Suno y Udio (Warner con ambos, Universal con Udio) y Udio **desactivó las descargas** durante la transición; Universal y Sony siguen litigando contra Suno. Para un docente, importan los datos de entrenamiento licenciados y los derechos de uso.
- **En vídeo hay consolidación y fragilidad de proveedor**: la caída de Sora en meses prueba que una tarjeta puede quedar muerta antes de empezar el curso.
- **Nueva capa imprescindible: la IA «con manos»** (escritorio + MCP + agentes + local). Los tres grandes laboratorios tienen ya una app de escritorio agéntica (Claude Desktop, Antigravity, ChatGPT con Codex/Work). La alternativa de privacidad real es **local** (LM Studio, Ollama, Jan, AnythingLLM).
- **Marco legal (importante para Galicia):** la Xunta prepara una **Ley de Educación Digital** (prevista antes de que acabe 2026, aún por confirmar su aprobación) que, según lo anunciado, limitaría a los docentes a **sistemas de IA homologados por la Consellería** (habrá un catálogo) y prohibiría decisiones académicas basadas solo en IA. En la UE, las obligaciones «de alto riesgo» para IA educativa (evaluar resultados de aprendizaje, admisión) pasaron al **2 de diciembre de 2027** (Reglamento 2026/1744, en vigor desde el 27-jul-2026), pero las obligaciones de **transparencia del art. 50** siguen desde el 2-ago-2026. Conviene decirlo en el curso: etiqueta el contenido generado.

### 1.2 Tabla Mantener / Fusionar / Descartar (33 tarjetas actuales)

| Taller | Tarjeta actual | Decisión | Justificación breve |
|---|---|---|---|
| **1 · LLM** | ChatGPT | **Mantener** | Actualizar: familia GPT-6 (despliegue desde el 29-oct-2026), ya no «serie o1/o3». |
| | Claude | **Mantener** | Actualizar: Fable 5.2, Opus 5.5, Sonnet 5.5 (no 3.5/3.7). Desaparece «Computer Use» como argumento central: pasa al Obradoiro 5. |
| | Gemini | **Mantener** | Actualizar a Gemini 4 (Argon, 13-oct-2026 según agregadores; confirmar). |
| | NotebookLM | **Mantener, renombrar** | Ahora «Gemini Notebook»; quitar «libre de alucinaciones». |
| | Perplexity | **Mantener (opcional)** | Su ventaja (búsqueda con citas) la copian los generalistas; sirve como contraste didáctico. No he verificado su estado concreto en 2026. |
| | DeepSeek | **Mantener** | V4 Pro y V4.1 Flash, licencia MIT, contexto 1 M. |
| | Qwen | **Mantener** | Qwen3.8 (Max cerrado; 27B abierto Apache 2.0). |
| | Kimi + GLM | **Fusionar** | Una tarjeta «Otros abiertos chinos»: Kimi K3.1 Pro y GLM-5.3. |
| **2 · Imagen** | Flux | **Mantener** | FLUX.2: pesos abiertos, control y coste. |
| | Midjourney | **Mantener** | V8.x: gusto estético, sin plan gratuito. |
| | Ideogram | **Mantener (ventaja estrecha)** | Tipografía/logos; el texto en imagen ya lo hacen bien los generalistas. |
| | Recraft | **Mantener** | Vector y sistemas de diseño; vigilar la competencia de SVG nativo en ChatGPT. |
| | Imagen 3 | **Fusionar → Nano Banana** | Google lidera ahora con la familia Nano Banana (Gemini Image). |
| | ChatGPT Images / DALL-E | **Fusionar → GPT Image** | DALL-E retirado; GPT Image 2.6 (4-nov-2026). |
| | Freepik Pikaso | **Fusionar (nota)** | Dar acceso a FLUX y otros modelos; mencionar como alternativa europea (empresa española). |
| | Stable Diffusion 3.5 | **Descartar como tarjeta** | La vía local pasa al Obradoiro 5 (FLUX.2/SD en local). |
| **3 · Audio** | Suno | **Mantener** | Canciones completas; v5.5; descargas en planes de pago; litigio abierto con UMG/Sony. |
| | Udio | **Descartar (vigilar)** | Descargas desactivadas, plataforma licenciada aún no abierta en junio de 2026. |
| | ElevenLabs SFX & Voice | **Mantener, ampliar** | Voz, efectos y música con datos licenciados, doblaje. |
| | Stable Audio | **Mantener** | 3.0 (mayo de 2026), entrenado solo con datos licenciados. |
| | MusicFX | **Descartar** | Sustituido por Lyria 3 (Google). |
| | AIVA | **Descartar** | Nicho; sin ventaja que justifique tarjeta (no verificado en 2026). |
| | Beatoven.ai | **Fusionar** | Lo cubren ElevenLabs Music / Stable Audio para fondos sin royalties. |
| | CassetteAI | **Descartar** | Sin evidencia de ventaja frente a Suno/ElevenLabs. |
| | (nuevo) Lyria 3 | **Añadir** | Modelo de Google con marca de agua SynthID obligatoria. |
| **4 · Vídeo** | Kling AI | **Mantener** | Kling 3.0: movimiento humano, valor, labios por personaje. |
| | OpenAI Sora | **Descartar** | Cerrado (app 26-abr-2026; API 24-sep-2026). |
| | Google Veo | **Mantener** | Veo 3.1 con audio nativo, en Gemini/Flow. |
| | Runway | **Mantener** | Gen-4.5: control y edición profesional. |
| | Hailuo / MiniMax | **Fusionar (nota)** | Útil por su capa gratuita; no justifica tarjeta propia. |
| | Luma Dream Machine | **Fusionar (nota)** | Cubierto por Runway/Kling para imagen→vídeo. |
| | HeyGen / Hedra | **Mantener ambos, separados** | HeyGen: avatar realista y doblaje; Hedra: foto + audio expresivo. |
| | ElevenLabs Dubbing | **Fusionar** | Pasa al Obradoiro 3 y se compara con el doblaje de HeyGen. |

**Resultado:** 8 + 6 + 4 + 5 tarjetas en los obradoiros 1-4, más 6 fichas nuevas en el Obradoiro 5 → 29 tarjetas frente a 33 (un 12 % menos) y, sobre todo, ninguna ya muerta.

---

## 2. Tarea A · Radiografía de la canibalización

**Imagen.** Los modelos integrados (GPT Image, Nano Banana) lideran las clasificaciones de preferencia ciega y editan en conversación, de modo que un docente cubre el 80 % de sus casos sin salir del chat. Nota: Claude *no* genera imágenes de mapa de bits de forma nativa (puede producir SVG y código), así que para ese caso hay que usar ChatGPT o Gemini. Quinteto con razón de ser: **GPT Image** (todoterreno y edición), **Nano Banana** (gratuito, rápido, referencias), **Midjourney** (dirección de arte), **Recraft** (vector/diseño) y **FLUX.2** (abierto, local, barato); **Ideogram** queda como sexta opción por tipografía. Un docente no necesita más.

**Audio.** Tiene sentido conservar **Suno** (única línea de canciones con voz comparable en facilidad), **ElevenLabs** (voz, SFX, música licenciada y doblaje) y **Stable Audio 3.0** (instrumental y efectos con datos licenciados). CassetteAI, Beatoven y MusicFX no justifican hoy una tarjeta propia. **Lyria 3** entra por ser el camino de Google y por su marca de agua SynthID. Udio queda fuera mientras no permita exportar.

**Vídeo y avatares.** Para no dispersar al profesorado: **un generador cinemático «de calidad» (Veo 3.1), uno «de valor y movimiento» (Kling 3.0), uno «de control profesional» (Runway Gen-4.5)** y, en avatares, **HeyGen** (realismo, doblaje) y **Hedra** (foto + voz). Seedance 2.x (ByteDance) es muy competitivo, pero llega sobre todo vía plataformas intermedias; lo dejo en observación. Nota pedagógica de seguridad: **no generar avatares ni voces de alumnado menor**, y recordar la etiqueta de contenido sintético.

---

## 3. Tarea B · El nuevo Obradoiro 5: «IA de Escritorio, Entornos Locais e Axentes»

### 3.1 Mapa del ecosistema (cuatro familias)

1. **Apps de escritorio de los laboratorios:** Claude Desktop (Chat/Cowork/Code), ChatGPT para escritorio (Chat/Work/Codex), Google Antigravity 2.0.
2. **IDE y extensiones agénticas:** Cursor, Devin Desktop (ex-Windsurf), Zed, Cline/Roo Code (extensiones de código abierto con «trae tu clave»). *GitHub Copilot Workspace*: no he podido verificar su estado actual; sí existe el agente de codificación de Copilot.
3. **IA local y privada:** LM Studio, Ollama + Open WebUI, Jan, AnythingLLM (todos sobre llama.cpp o MLX).
4. **Agentes de navegador:** Claude in Chrome, Gemini in Chrome, Perplexity Comet, ChatGPT Agent. **Aviso:** una investigación presentada en un taller de ICLR 2026 probó que, en *ChatGPT Atlas* (modo agente), una web maliciosa podía extraer datos entre pestañas; para Gemini in Chrome, Claude for Chrome y Comet se daban las mismas precondiciones del ataque, aunque no se rompió ninguno. OpenAI admite que la inyección de instrucciones «no se puede parchear del todo». **Recomendación:** usar solo en cuentas de demostración, sin sesiones abiertas de plataformas del centro (Abalar/ABALAR, correo, etc.) y sin datos de alumnado.

*(MCP —Model Context Protocol— es el estándar de conexión de herramientas; lo comparten Claude, Codex, Antigravity, Cursor y los clientes locales. Está gobernado hoy por la Linux Foundation, según mi información; confirmar.)*

### 3.2 Fichas técnicas (6)

#### Ficha 5.1 · Claude Desktop (con Cowork y MCP)
- **Empresa:** Anthropic.
- **Tipo:** cliente de escritorio con tres modos (Chat, **Cowork** —trabajo de conocimiento para no programadores— y Code), compatible con MCP, habilidades y *hooks*.
- **Costes y privacidad:** planes de pago de Claude (Pro, Max, Team/Enterprise); **no es local**: el contenido que le des acceso se envía al modelo. En Team/Enterprise hay controles de datos; para alumnado, nada identificable.
- **Relevancia docente:** ordenar y renombrar carpetas de aula, convertir apuntes en fichas, preparar rúbricas, conectar correo y calendario por MCP, generar pequeñas apps didácticas (HTML) sin escribir código.
- **Pros:** curva de entrada suave (Cowork); comparte configuración con Code; muy sólido en escritura y razonamiento largo.
- **Contras:** coste; permisos amplios sobre el equipo (la prensa ha recogido el recelo de dar acceso total a un agente); no cumple por sí solo el «datos no salen del centro».
- **Enlace:** https://claude.com/download
- **Transparencia:** producto del desarrollador de este asistente.

#### Ficha 5.2 · ChatGPT para escritorio (Chat / Work / Codex)
- **Empresa:** OpenAI.
- **Tipo:** cliente de escritorio; **Codex** se integró en la app el 9-jul-2026 y convive con los modos Chat y Work; *ChatGPT Agent* sustituye a Operator.
- **Costes y privacidad:** Codex llega a todos los planes de ChatGPT, incluido el gratuito (límites); ejecución en nube o en local según el modo; datos procesados por OpenAI.
- **Relevancia docente:** análisis de ventanas y capturas, tareas repetitivas, creación de materiales con código, automatizaciones programadas.
- **Pros:** acceso inmediato, enorme base de usuarios, buen ecosistema de conectores.
- **Contras:** sin modo «solo local»; el agente de navegador tiene el riesgo de inyección descrito arriba; la marca cambia a menudo (Operator, Atlas ya cerrados).
- **Enlace:** https://chatgpt.com/features/desktop (verificar la ruta exacta; dominio oficial https://chatgpt.com)

#### Ficha 5.3 · Google Antigravity 2.0
- **Empresa:** Google.
- **Tipo:** entorno agéntico de escritorio (app independiente + CLI + SDK desde el 19-may-2026): subagentes, *skills*, MCP, tareas programadas y un subagente de navegador que prueba lo que construye.
- **Costes y privacidad:** plan individual gratuito en vista previa; niveles Google AI Pro/Ultra; modelos Gemini (y Claude/GPT-OSS según fuentes). Las fuentes **discrepan** sobre si los agentes corren en local o en la nube: comprobar antes de prometer privacidad.
- **Relevancia docente:** crear webs de aula o recursos interactivos con agentes en paralelo; probar el resultado automáticamente.
- **Pros:** gratis para empezar; fuerte en trabajo con navegador.
- **Contras:** lanzamiento accidentado, gobernanza de seguridad aún por demostrar; orientado a quien ya piensa como desarrollador.
- **Enlace:** https://antigravity.google

#### Ficha 5.4 · Cursor (y alternativas: Devin Desktop, Cline/Roo Code)
- **Empresa:** Anysphere (Cursor); Cognition (Devin Desktop); proyectos abiertos (Cline/Roo Code).
- **Tipo:** IDE agéntico multimodelo con MCP; Cline/Roo son **extensiones de código abierto** con «trae tu clave» y compatibilidad con modelos locales.
- **Costes y privacidad:** Cursor, plan *Hobby* gratuito y *Pro* en torno a 20 $/mes; datos enviados a los proveedores de modelo (revisar su modo de privacidad). Cline y Roo, gratuitas; coste = tu clave de API, o **0 € con un modelo local**.
- **Relevancia docente:** generar páginas HTML, hojas de ejercicios con scripts y pequeñas aplicaciones sin teclear código; es la vía para «docentes que crean sus propios recursos».
- **Pros:** el patrón más maduro de edición guiada por agentes; Cline permite una vía 100 % local.
- **Contras:** pide cierta cultura técnica (proyectos, diffs, control de versiones); posible deuda técnica en materiales que nadie revisa.
- **Enlaces:** https://cursor.com · https://cline.bot · https://windsurf.com (ahora Devin Desktop; verificar redirección)

#### Ficha 5.5 · LM Studio (y alternativas: Ollama + Open WebUI, Jan)
- **Empresa:** Element Labs (LM Studio); Ollama; Open WebUI; Jan.
- **Tipo:** runtime local con interfaz gráfica (LM Studio y Jan) o servicio local con web propia (Ollama + Open WebUI, para servidor del centro).
- **Costes y privacidad:** LM Studio, gratuito (software cerrado); Ollama, Open WebUI y Jan, **código abierto**; **100 % local y sin conexión** una vez descargado el modelo → encaja con el RGPD y con la futura exigencia de la Consellería (el dato no sale del equipo).
- **Relevancia docente:** corregir y comentar textos de alumnado **sin subir nada a la nube** (previa anonimización), resumir actas, asistente de centro con una sola instalación.
- **Pros:** privacidad real, coste cero, sin dependencia de un proveedor.
- **Contras:** los modelos locales son **más débiles** que los de frontera; exigen memoria (orientativo: 16 GB de RAM para modelos de 7-8 B; 32 GB o una GPU de 16-24 GB para modelos de ~27 B como Qwen3.8-27B, con licencia Apache 2.0). Modelos como DeepSeek V4 o Kimi K3 son demasiado grandes para un portátil.
- **Enlaces:** https://lmstudio.ai · https://ollama.com · https://openwebui.com · https://jan.ai

#### Ficha 5.6 · AnythingLLM
- **Empresa:** Mintplex Labs.
- **Tipo:** aplicación local de **RAG** (chat con tus documentos); incluye su propio motor o se conecta a Ollama/LM Studio.
- **Costes y privacidad:** de código abierto; puede funcionar **100 % en local**.
- **Relevancia docente:** «preguntar» a la programación didáctica, al PEC o a las instrucciones de la Consellería con los PDF en tu ordenador; consultar un banco de exámenes propio.
- **Pros:** la forma más sencilla de tener un asistente documental privado.
- **Contras:** la calidad depende del modelo local y de cómo se trocea el documento; sin comprobación humana puede responder con seguridad cosas que el documento no dice.
- **Enlace:** https://anythingllm.com

---

## 4. Catálogo definitivo de tarjetas (Obradoiros 1-4)

*(Campo sugerido en cada tarjeta: `verificado_en` y `estado`; ver sección 6.)*

### Obradoiro 1 · Modelos Fundacionais e Razoamento (8)

| Tarjeta | Versión más reciente (nov-2026) | Enlace | Frase síntese |
|---|---|---|---|
| **ChatGPT** (OpenAI) | Familia GPT-6 (Sol/Luna; GPT-6 Pro en planes altos); GPT Image 2.6 | https://chatgpt.com | O todoterreo con voz, imaxe e axentes nunha soa conta. |
| **Claude** (Anthropic) | Fable 5.2, Opus 5.5, Sonnet 5.5, Haiku 5.5 | https://claude.ai | Prosa matizada, razoamento longo e traballo con arquivos e ferramentas. |
| **Gemini** (Google) | Gemini 4 (Argon; confirmar) | https://gemini.google.com | Multimodalidade e contexto enorme, integrado en Workspace e Android. |
| **Gemini Notebook** (antes NotebookLM) | Renomeado o 16-xul-2026 | https://notebooklm.google.com | Respostas ancoradas nas túas fontes, con citas e resumos en áudio e vídeo. |
| **Perplexity** (opcional) | Verificar | https://www.perplexity.ai | Buscador con citas: o contraste didáctico co *deep research* dos xeneralistas. |
| **DeepSeek** | V4 Pro (13-ago) e V4.1 Flash (snapshot 17-out); MIT | https://www.deepseek.com | Rendemento de primeiro nivel con custo mínimo e pesos abertos. |
| **Qwen** (Alibaba) | Qwen3.8-Max (nube) e Qwen3.8-27B (aberto, Apache 2.0) | https://chat.qwen.ai | A familia aberta máis versátil, con tamaños que cabe executar en local. |
| **Kimi e GLM** (Moonshot, Z.ai) | Kimi K3.1 Pro (23-out); GLM-5.3 (18-ago) | https://www.kimi.com · https://z.ai | Axentes de contexto longo e enxeñaría, con pesos descargables. |

*Aviso didáctico:* en abril-noviembre de 2026 hay bastante ruido sobre qué modelo «gana»; el docente debe aprender a **elegir por tarea**, no por marca.

### Obradoiro 2 · Creación Visual e Multimodal (6)

| Tarjeta | Versión | Enlace | Frase síntese |
|---|---|---|---|
| **GPT Image** (ChatGPT) | 2.6 (4-nov-2026; SVG y GIF animado) | https://chatgpt.com | Edición conversacional precisa e texto lexible na imaxe. |
| **Nano Banana** (Gemini) | Nano Banana 2 y Pro | https://gemini.google.com | Gratuíto, rápido e con imaxes de referencia consistentes. |
| **Midjourney** | V8.x | https://www.midjourney.com | O mellor gusto estético: dirección de arte e luz. |
| **Ideogram** | Serie 4.x (verificar) | https://ideogram.ai | Tipografía exacta en pósteres, logotipos e cartelería. |
| **Recraft** | V4.x | https://www.recraft.ai | Gráficos vectoriais (SVG) e iconografía de deseño. |
| **FLUX** (Black Forest Labs) | FLUX.2 (FLUX 3 anunciado según algunas fuentes) | https://bfl.ai | Pesos abertos e control: tamén en local. |

### Obradoiro 3 · Audio, Voz e Creación Sonora (4)

| Tarjeta | Versión | Enlace | Frase síntese |
|---|---|---|---|
| **Suno** | v5.5 | https://suno.com | Cancións completas con voz a partir dunha frase. |
| **ElevenLabs** | Voice, Music, SFX, Dubbing | https://elevenlabs.io | Voz, efectos e música con datos licenciados e dobraxe. |
| **Stable Audio** | 3.0 (maio de 2026) | https://stableaudio.com | Instrumentais e efectos con licenza limpa e duración exacta. |
| **Lyria** (Google) | Lyria 3 (feb-2026), marca SynthID | https://deepmind.google/models/lyria | A vía de Google para música xerada con marca de auga. |

*Vigilar:* Udio (descargas desactivadas por su acuerdo con Universal y Warner) y la plataforma licenciada que ambos prometen para 2026.
*Aviso legal:* clonar la voz de una persona exige su consentimiento expreso; no se hará con alumnado.

### Obradoiro 4 · Vídeo Xerativo e Avatares (5)

| Tarjeta | Versión | Enlace | Frase síntese |
|---|---|---|---|
| **Veo** (Google) | 3.1, en Gemini y Flow | https://labs.google/flow | Calidade cinematográfica con son sincronizado. |
| **Kling AI** (Kuaishou) | 3.0 | https://klingai.com | Movemento humano realista e moito valor por euro. |
| **Runway** | Gen-4.5 | https://runwayml.com | Control de cámara, *motion brush* e edición profesional. |
| **HeyGen** | Avatar V; dobraxe en 175+ idiomas | https://www.heygen.com | O docente virtual máis realista e a dobraxe con labios sincronizados. |
| **Hedra** | Character-3 | https://www.hedra.com | Unha foto e un áudio convértense nun personaxe expresivo. |

*Retirado:* OpenAI Sora (cerrado en 2026). *En observación:* Seedance 2.x (ByteDance), Luma Ray3, Hailuo.

---

## 5. Guía de prompts de demostración (contexto educativo galego)

**Obradoiro 1 · Modelos e razoamento**
> Actúa como asesor pedagóxico. Son profesor/a de 2º de ESO en Galicia e quero unha situación de aprendizaxe de Matemáticas sobre proporcionalidade a partir da factura da luz dunha familia da miña vila. Dame: obxectivo, competencias específicas do currículo galego, secuencia en 4 sesións, unha actividade de investigación con datos reais e unha rúbrica de 4 niveis. Se non estás seguro dun dato legal ou curricular, dímolo e non o inventes. Responde en galego e con listas curtas.

**Obradoiro 2 · Creación visual**
> Crea un cartaz A3 en vertical para o Día das Letras Galegas do noso instituto, con tipografía grande lexible, paleta azul e branca inspirada na bandeira e unha ilustración da ría. O texto debe dicir exactamente: «Día das Letras Galegas · Venres 17 de maio · Biblioteca do IES». Dame tres variantes e versión vectorial (SVG) da mellor.

**Obradoiro 3 · Audio, voz e son**
> Compón un jingle instrumental de 20 segundos, alegre e suave, para a entrada ao aula despois do recreo, sen letra e sen estilo reconocible dun artista. Dame tamén un efecto sonoro curto de campá escolar antiga. Se a ferramenta o permite, indica a licenza de uso en contornas educativas.

**Obradoiro 4 · Vídeo e avatares**
> Plano cinematográfico de 8 segundos: unha clase de ciencias nun instituto rural galego, luz de media mañá, alumnado de espaldas observando un experimento con plantas, sen caras identificables nin texto lexible. Camiño lento cara adiante, ambiente sonoro suave. Crea despois un avatar presentador (non real) que lea en galego un aviso de 15 segundos sobre a saída ao museo e dobra o resultado ao castelán.

**Obradoiro 5 · IA de escritorio, entornos locais e axentes**
> (Con acceso só a unha carpeta de proba chamada «Aula_Proba», sen datos persoais.) Le os 12 documentos da carpeta, clasifícaos por tema e curso, propón unha estrutura de subcarpetas e un índice en Markdown. **Non movas nin borres nada ata que eu confirme a proposta.** Cando eu aprobe, executa os cambios e dáme un rexistro do que fixeches.

*Variante local:* mismo ejercicio con LM Studio y un modelo de ~7-8 B, comparando calidad con la versión en la nube y comprobando que no hay tráfico de salida.

---

## 6. Recomendaciones de diseño web

- Añade a cada tarjeta `verificado_en` (fecha) y `estado` (*vigente / renombrado / retirado*). En doce meses han cerrado Sora, Atlas y Operator, y han cambiado de nombre NotebookLM y Windsurf.
- Evita fijar versiones en el título (usa «GPT» o «Claude» con la versión en un campo editable).
- Crea una etiqueta visible «**Datos: nube / local**» y una insignia «**Homologada por la Consellería**» preparada para cuando exista el catálogo.
- En el Obradoiro 5, muestra una advertencia fija sobre **permisos y datos de alumnado**.

## 7. Pendientes de verificación antes de publicar

1. Versiones exactas de Gemini 4, Ideogram, FLUX, Midjourney y Qwen en sus webs oficiales.
2. Estado de aprobación de la Ley de Educación Digital de Galicia y alcance real del catálogo de IA homologada.
3. Si los agentes de Antigravity 2.0 corren en local o en nube.
4. Estado actual de Perplexity y de GitHub Copilot Workspace.
5. Todos los enlaces de las tablas (abrirlos y anotar la fecha).
