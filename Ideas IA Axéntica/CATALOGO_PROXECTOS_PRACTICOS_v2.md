# Catálogo de proxectos prácticos · versión 2

Curso **«Iniciación á IA Axéntica»**. Cada proxecto debe poder expresarse como:

```text
Finalidade + fontes + accións autorizadas + revisión humana
```

**Lenda de recursos:** 🗂 documentos · 📊 CSV/datos · 🧩 HTML local · 🔎 busca/fontes · 🖼️ imaxe · 🎞️ vídeo local · 🔊 audio · 🗺️ API pública

## Como usar este documento

- A **Parte 1** recolle os proxectos retirados por seren «cuasi-chat»: serven de contraste na aula.
- A **Parte 2** recolle os proxectos mantidos, fusionados e novos, agrupados por afinidade. Cada ficha leva o necesario para recrear unha proba antes de clase.
- A **Parte 3** lista os proxectos orixinais que aínda non pasaron a criba fina.
- A **Parte 4** propón unha orde para probalos.

**Aviso sobre datos externos.** Todas as API, portais e ferramentas que se nomean son puntos de partida, non garantías. Antes de preparar cada práctica hai que verificar: se piden clave, límites de uso, licenza dos datos ou das imaxes, formato e disponibilidade na plataforma do curso.

**Patrón «instantánea» (recomendado para todo o que use datos externos).** O axente descarga os datos á carpeta do proxecto xunto cun rexistro de fonte, data e licenza, e o HTML traballa co ficheiro local. Evita fallos de conexión na aula, fai o resultado reproducible e deixa a trazabilidade que o curso pide.

**«En local» e privacidade.** Cando se di que algo é «en local» significa que se procesa con ferramentas do espazo de proxecto. Hai que confirmar se a plataforma envía imaxes, audios ou vídeos a un modelo externo, e usar só material que se aceptaría subir.

**Protocolo común para probar un proxecto** (vale para todos):

1. Crea un espazo de proxecto limpo e carga só as fontes permitidas.
2. Escribe primeiro a *ficha de deseño*: obxectivo, fontes, accións autorizadas, accións que requiren consulta, criterio de validación e riscos.
3. Pide un **plan antes de executar** e corríxeo.
4. Revisa os produtos intermedios, non só o final.
5. Aplica o punto de verificación da ficha.
6. Anota as incidencias (o que fallou e como o detectaches). Son material para a aula.

---

# Parte 1 · Proxectos «cuasi-chat» (retirados)

## Que é un proxecto cuasi-chat

É un encargo que se presenta como «axente» pero funciona igual pegando un prompt longo nun chat. Non hai fonte que consultar, ferramenta que actúe, estado que se conserve nin resultado que se poida comprobar fóra de «parece razoable». O axente só engade lonxitude.

**Proba de seis preguntas.** Unha tarefa é realmente axéntica cando cumpre polo menos catro:

| # | Pregunta |
| - | -------- |
| 1 | ¿Ten varios pasos encadeados cun obxectivo que persiste? |
| 2 | ¿Consulta fontes ou datos externos ao modelo? |
| 3 | ¿Usa ferramentas que actúan (código, ficheiros, consultas, cálculo)? |
| 4 | ¿Conserva estado entre pasos (ficheiros intermedios, rexistro)? |
| 5 | ¿Hai un punto onde algo pode fallar de verdade e comprobarse de forma obxectiva? |
| 6 | ¿Hai unha decisión humana que cambia o resultado? |

Os proxectos desta parte cumpren un ou ningún.

## Lista de retirados e por que non son axénticos

| Proxecto retirado | Por que é cuasi-chat |
| --- | --- |
| Menú semanal intelixente | Entrada pequena, saída de texto. Non hai fonte nin cálculo que comprobar: só «parece razoable». |
| Xestor de orzamento familiar | Sen datos reais non hai nada que analizar; con datos reais entra en terreo sensible. Sen estado nin cálculo verificable queda en plantilla. |
| Planificador de reforma doméstica | Prezos e prazos que o modelo inventa con aparencia de rigor. Sen fontes autorizadas non pode contrastar nada. |
| Asistente para unha mudanza | Lista de tarefas xenérica, a que daría calquera plantilla. |
| Preparador de eventos familiares | Documentos de saída única, sen ferramentas nin comprobación. |
| Plan de lectura persoal | Recomenda sen acceso a catálogos reais. O risco é propoñer libros que non existen. |
| Arquivo persoal dixital | As regras de nomeado e carpetas caben en dez liñas. Só sería axéntico se actuase sobre ficheiros reais. |
| Caixa de ferramentas para familias | Colección de textos: o valor está na redacción, non no proceso. |
| Club de lectura expandido | Xerar preguntas e actividades é produción de contido sen verificación. |
| Banco de recursos comunitarios | Un directorio que nace obsoleto: sen consulta a fontes vivas é só memoria do modelo. |
| Plan para unha festa ou feira local | Programa e cartelaría: dous chats e un deseño. |
| Caderno de exploración para primaria | Material didáctico de saída única. |
| Biblioteca de xogos de aula | Catálogo que o modelo escribe de memoria, sen fonte nin proba. |
| Xerador de retos fotográficos | Lista de ideas que non toca ningunha foto. |
| Arquivo de receitas familiares | A conversión de cantidades é cálculo trivial; o que importa (as historias) non o pon o axente. |
| Guía cultural dunha cidade | Solapa con Ruta literaria e Itinerario de patrimonio, pero sen datos nin mapa verificados. |
| Fanzine dixital | O traballo é editorial: o axente xera texto e imaxes soltos e o ensamblaxe é humano. |
| Diario de adestramento ou benestar | Ademais de xenérico, invita a introducir datos de saúde. |

## Cinco exemplos con prompt e diagnóstico

### 1. Menú semanal intelixente

```text
Actúa como nutricionista. Fai un menú semanal para dúas persoas, sen gluten
e cun orzamento de 60 €. Inclúe a lista da compra e as receitas.
```

**Por que non é axéntico:** unha soa mensaxe, unha soa resposta. Non consulta prezos reais nin informacións nutricionais, non calcula nada que se poida comprobar e a «revisión» é ler e pensar «vale». O orzamento de 60 € é unha afirmación que ninguén verifica.

### 2. Xestor de orzamento familiar

```text
Son unha familia de catro persoas con ingresos de 2.800 € ao mes.
Fai un plan de aforro e unha táboa de gastos por categorías.
```

**Por que non é axéntico:** non hai datos de entrada reais, así que o resultado é unha plantilla con números inventados. Non hai ficheiro que ler, cálculo que reconcilar nin escenario que simular de verdade.

### 3. Plan de lectura persoal

```text
Gústanme as novelas históricas e a ciencia ficción. Recomenda 12 libros
para este ano e organízaos nun calendario mensual.
```

**Por que non é axéntico:** non consulta ningún catálogo, así que non sabe se os libros existen, se están dispoñibles nin canto dura cada un. Os títulos inventados pasan desapercibidos porque nada os comproba.

### 4. Preparador de eventos familiares

```text
Vou organizar o cumpreanos dos meus pais, 30 persoas, nun xardín.
Fai un guión do día, un orzamento e unha lista de materiais.
```

**Por que non é axéntico:** documento de saída única. Non hai fonte, ferramenta nin estado. Os prezos do orzamento son estimacións do modelo.

### 5. Xerador de retos fotográficos

```text
Dáme un calendario de 30 retos fotográficos para mellorar a miña
composición, con unha rúbrica para avaliar cada foto.
```

**Por que non é axéntico:** nunca ve unha foto. Se o axente analizase as imaxes reais, extraese metadatos e medise algo (proporcións, cor, nitidez) estaríamos noutro proxecto, algo próximo a **Arqueoloxía fotográfica** ou **Paleta dun lugar**.

## Lectura didáctica

Estes proxectos son útiles na aula como **contraste**: o mesmo encargo en versión chat (unha mensaxe, unha resposta) fronte á versión axéntica (fontes, plan, execución, verificación). O que os converte en axénticos non é a complexidade do tema senón engadir **datos reais, unha ferramenta que actúe e un punto de comprobación**.

---

# Parte 2 · Proxectos mantidos, fusionados e novos

Etiquetas: **[Mantido]** reforzado con verificación explícita · **[Fusión]** unión de varios do catálogo orixinal · **[Novo]** proposta nova.

Cada ficha ten: **Idea**, **Fontes**, **O axente fai**, **Verificas ti**, **Alcance mínimo (4 h)** e **Semente do encargo** (un arranque que podes adaptar).

---

## A. Datos, ciencia e decisións

### A1. Visualizador do orzamento público · [Mantido] · 📊 🧩

- **Idea.** Panel cunhas partidas dun orzamento real (concello, Xunta ou Estado), comparación entre anos e explicacións en linguaxe clara.
- **Fontes.** Un CSV descargado dun portal oficial de datos abertos e a súa documentación. Gárdase na carpeta do proxecto con URL e data.
- **O axente fai.** Inspecciona o ficheiro (columnas, unidades, ausencias), propón un plan de visualización, limpa os datos nun ficheiro novo, constrúe o HTML con gráficas e redacta as explicacións.
- **Verificas ti.** Que a suma das partidas cadre co total publicado. Que as unidades (euros ou miles de euros) son as correctas. Que ningunha explicación afirma máis do que mostran os datos.
- **Alcance mínimo.** Unha entidade, dous anos, tres gráficas e un parágrafo por gráfica.
- **Semente.** «Le este CSV e dime que contén antes de facer nada: columnas, unidades e problemas que ves. Despois propón un plan de tres gráficas e agarda a miña aprobación.»

### A2. Decisor con criterios e evidencias · [Fusión] · 🔎 📊 🧩

Fusiona: Comparador de escapadas + Mapa de decisións de compra + Guía de consumo responsable.

- **Idea.** Unha decisión real (electrodoméstico, destino, tarifa, coche…) convertida nun comparador con pesos e evidencias. O toque matemático é a **análise de sensibilidade**: ¿cambia a recomendación se muda a importancia dun criterio?
- **Fontes.** Tres a cinco opcións con datos recollidos nunha folla CSV (fichas técnicas, informes de organismos de consumo), cunha URL por cada dato.
- **O axente fai.** Propón criterios a partir da decisión e pregunta polos pesos. Recolle e estrutura os datos coas súas fontes. Constrúe un HTML con controis deslizantes para os pesos, calcula o ranking e identifica en que punto cambia o primeiro posto.
- **Verificas ti.** Que cada dato ten fonte e abre ao azar tres. Que os criterios non contan dúas veces o mesmo. Que o «gañador» non depende dun peso absurdo.
- **Alcance mínimo.** Catro opcións, cinco criterios, controis de pesos e unha táboa de sensibilidade.
- **Semente.** «Quero decidir entre X, Y e Z. Antes de buscar nada, pregúntame que criterios me importan e en que orde. Despois pídeme confirmación do plan de recollida de datos.»

### A3. Detective da factura da luz · [Fusión] · 🗂 📊 🔎

Fusiona: Calculadora de pegada cotiá + Comparador de consumo enerxético.

- **Idea.** Parte dunha factura (propia ou sintética), reconstrúe o cálculo e simula que pasaría con outra tarifa ou con outros hábitos.
- **Fontes.** A factura **sen datos persoais** (borra nome, enderezo, NIF e IBAN antes de subila ou usa unha sintética). Prezos de fonte oficial. Potencias típicas dos aparellos.
- **O axente fai.** Extrae potencia contratada, consumo, peaxes e impostos; reconstrúe o total con código; simula dous ou tres escenarios; xera un informe e un HTML.
- **Verificas ti.** Que o total reconstruído coincide co da factura. Se non coincide, a diferenza é información, non un erro a esconder. Revisas os supostos dos escenarios.
- **Alcance mínimo.** Unha factura e dous escenarios.
- **Semente.** «Le esta factura e extrae cada concepto nunha táboa. Reconstrúe o total con código e dime se coincide. Non simules nada ata que cadre.»

### A4. Clima da miña aldea, 1940–hoxe · [Novo] · 📊 🗺️ 🧩

- **Idea.** Series históricas de temperatura e precipitación dun punto concreto, separando **tendencia de variabilidade**.
- **Fontes.** Unha API de reanálise climática con arquivo histórico (p. ex. a de Open-Meteo, verificando cobertura e licenza). As coordenadas do lugar.
- **O axente fai.** Descarga a serie (instantánea), calcula medias móbiles, tendencias por décadas e anomalías, fai gráficas en HTML e redacta conclusións con cautelas.
- **Verificas ti.** Que as conclusións distinguen tendencia de ruído anual. Que non se confunde reanálise con medicións dunha estación. Que o axente non extrapola.
- **Alcance mínimo.** Unha localidade, temperatura media anual, unha gráfica de tendencia e un texto de 150 palabras.
- **Semente.** «Descarga a serie diaria de temperatura de este punto desde 1940 e dime que columnas e unidades hai. Propón unha forma de medir a tendencia e dime que limitacións ten.»

### A5. Observatorio do ceo de hoxe · [Novo] · 🗺️ 📊 🧩

- **Idea.** Decidir cando e onde observar o ceo esta semana: nubosidade prevista, fase da Lúa e horas de anoitecer calculadas en local.
- **Fontes.** Unha previsión horaria por API (preferiblemente sen clave) e unha biblioteca de efemérides no entorno de execución. As coordenadas.
- **O axente fai.** Obtén a previsión, calcula Lúa e crepúsculo, puntúa as noites con criterios explícitos, recomenda a mellor ventá e unha alternativa, e xera o panel.
- **Verificas ti.** Contrasta as horas de anoitecer e a fase lunar cunha fonte independente. A previsión é probabilística: o axente debe dicilo.
- **Alcance mínimo.** Cinco noites, puntuación sinxela e un panel.
- **Depende de** que o espazo permita executar código. Verifícao antes.

### A6. Planificador de viaxe ferroviaria · [Mantido] · 🔎 🗺️ 📊

- **Idea.** Itinerario en tren con alternativas e tempos de transbordo reais.
- **Fontes.** Horarios en formato aberto (feed GTFS do operador, se existe e permite o uso) ou unha táboa de horarios descargada.
- **O axente fai.** Le o feed, constrúe un grafo simple de conexións, calcula rutas e transbordos mínimos, e xera itinerario, alternativa e lista de comprobación.
- **Verificas ti.** Contrasta dúas viaxes coa web oficial do operador. Comproba os tempos mínimos de transbordo. Recorda que os horarios cambian.
- **Alcance mínimo.** Unha orixe-destino e dúas alternativas.
- **Semente.** «Estes son os datos de horarios. Antes de calcular, explícame como están organizados e que podes e non podes saber con eles.»

### A7. Laboratorio visual de Matemáticas e Física · [Mantido] · 🧩 📊

- **Idea.** Simulación ou explicador interactivo dun fenómeno (tiro parabólico, péndulo, probabilidade, afinación…).
- **Fontes.** O modelo matemático escrito por ti (non pola IA) e, opcionalmente, datos experimentais.
- **O axente fai.** Traduce o modelo a HTML con controis, explica as variables, propón casos límite.
- **Verificas ti.** Compara a saída coa solución analítica en tres casos coñecidos. Revisa unidades e casos límite (ángulo de 0° e 90°, valores cero).
- **Alcance mínimo.** Un fenómeno e dous ou tres controis.
- **Semente.** «Aquí tes a fórmula e as variables. Constrúe unha simulación HTML. Despois dime tres casos nos que o resultado debería ser un valor que eu poida comprobar a man.»

---

## B. Territorio, patrimonio e memoria

### B1. Ruta literaria local · [Mantido] · 🧩 🗺️ 🔎

- **Idea.** Ruta con autores, lugares e textos dunha comarca, con mapa e fichas.
- **Fontes.** Wikidata e OpenStreetMap para lugares e coordenadas. Textos de dominio público ou propios, citados con autor, obra e edición.
- **O axente fai.** Propón candidatos de autores e lugares, valida coordenadas, ordena unha ruta e xera mapa HTML e fichas.
- **Verificas ti.** Que **cada texto citado existe** e está ben atribuído (consulta a edición; este é o risco máis alto). Que a ruta é practicable.
- **Alcance mínimo.** Seis paradas.
- **Semente.** «Só podes citar textos que estean nos documentos do proxecto. Se non tes o texto, di "sen fonte".»

### B2. Toponimia viva · [Novo] · 🗺️ 📊 🧩

- **Idea.** Analizar os topónimos dun concello: terminacións, raíces e patróns, cun mapa interactivo.
- **Fontes.** Nomes de lugar de OpenStreetMap (consulta Overpass, verificando límites) ou un nomenclátor oficial. Bibliografía lingüística autorizada para as etimoloxías.
- **O axente fai.** Descarga e limpa os nomes, clasifica por terminación con regras explícitas, conta, mapea. Para cada grupo propón unha hipótese de orixe **marcada como hipótese**.
- **Verificas ti.** Revisa unha mostra de 20 topónimos clasificados. Non aceptes etimoloxías sen fonte. Consulta cunha persoa do departamento de Galego.
- **Alcance mínimo.** Un concello e tres ou catro terminacións.
- **Semente.** «Clasifica estes topónimos por terminación. Para cada regra, dime cantos casos recolle e mostra cinco exemplos. Non expliques ningunha orixe sen fonte do proxecto.»

### B3. Biodiversidade do meu camiño · [Novo] · 🗺️ 🔎 🧩

- **Idea.** Guía de campo persoal: especies observadas arredor dunha ruta habitual, con tempada e imaxes.
- **Fontes.** Unha base aberta de observacións (GBIF ou iNaturalist), verificando a licenza de cada imaxe e filtrando por calidade da observación.
- **O axente fai.** Define a área arredor da ruta, descarga observacións, agrupa por tipo e mes, xera a guía HTML con créditos.
- **Verificas ti.** Usa só observacións de calidade investigadora. Revisa os nomes científicos. Non publiques localizacións exactas de especies sensibles.
- **Alcance mínimo.** 30 a 50 especies e unha ficha por grupo.
- **Semente.** «Descarga só observacións con calidade verificada nun radio de 500 m desta ruta. Antes de xerar nada, dime cantas hai e como se distribúen por mes.»

### B4. Guía de accesibilidade do barrio · [Mantido] · 🗺️ 🧩

- **Idea.** Mapa e fichas de lugares, barreiras e melloras dun percorrido.
- **Fontes.** OpenStreetMap (rampas, beirarrúas, escaleiras) e unha visita propia con fotos e notas.
- **O axente fai.** Extrae os elementos relevantes, detecta ocos de datos, xera unha guía de visita para recoller información, integra as notas e produce mapa e fichas.
- **Verificas ti.** Visita polo menos cinco puntos no terreo. Os datos de accesibilidade non se dan por certos só polo mapa. Sen persoas identificables nas fotos.
- **Alcance mínimo.** Un percorrido dun quilómetro.
- **Semente.** «Lista o que o mapa di sobre accesibilidade neste percorrido e marca todo o que falta. Fai unha folla para que eu recolla datos no terreo.»

### B5. Arquivo de memoria oral · [Mantido] · 🔊 🗂 🗺️

- **Idea.** Protocolo de entrevista, fichas, transcrición e mapa dunha memoria local.
- **Fontes.** Unha gravación propia con consentimento por escrito, ou unha entrevista sintética.
- **O axente fai.** Transcribe (se a plataforma ofrece ferramenta; se non, parte dunha transcrición feita), marca os fragmentos dubidosos, extrae lugares, datas e persoas, e xera fichas e mapa.
- **Verificas ti.** Escoita os fragmentos marcados. Confirma nomes propios. Define consentimento e uso antes de gravar.
- **Alcance mínimo.** Unha entrevista de 5 a 10 minutos.
- **Semente.** «Transcribe e marca con [?] todo o que non estea claro. Non completes nomes nin datas que non se oian.»

### B6. Arqueólogo familiar · [Novo] · 🗂 🖼️

- **Idea.** Cartas, fotos e documentos escaneados → liña do tempo e árbore, con grao de certeza en cada dato.
- **Fontes.** Material propio ou de persoas falecidas ou con permiso. Traballa sempre con copias.
- **O axente fai.** Le ou transcribe, extrae datas, persoas e lugares, constrúe a liña do tempo. Cada dato leva «certo / probable / hipótese» e de onde sae.
- **Verificas ti.** Contrasta coa memoria familiar. Revisa as lecturas de caligrafía. Non aceptes parentescos non documentados.
- **Alcance mínimo.** Dez documentos.
- **Límite.** Datos de terceiros: só de persoas falecidas ou co seu consentimento.

### B7. Xogo de pistas histórico-literario · [Mantido, con personaxes integrados] · 🧩 🗂

- **Idea.** Escape room ou procura do tesouro en HTML con enigmas baseados en datos e textos reais. Se usa personaxes, levan unha ficha coherente.
- **Fontes.** Textos e datos históricos de dominio público ou propios.
- **O axente fai.** Deseña o grafo de pistas (que pista desbloquea cal), escribe os enigmas, programa o HTML e proba camiños.
- **Verificas ti.** Xoga ata o final buscando camiños imposibles ou atallos. Revisa os datos históricos.
- **Alcance mínimo.** Cinco enigmas.
- **Semente.** «Antes de escribir un enigma, debuxa o grafo de dependencias entre pistas e axúdame a comprobar que non hai camiños mortos.»

---

## C. Imaxe e vídeo en local

### C1. Arqueoloxía fotográfica · [Novo] · 🖼️ 🗺️ 🧩

- **Idea.** Pór orde nunha fototeca sen tocar os orixinais: cronoloxía, mapa, duplicados e álbums.
- **Fontes.** Unha **copia** de varios centos de fotos (non toda a biblioteca) e os seus metadatos EXIF. Mellor paisaxes e viaxes ca persoas.
- **O axente fai.** Le metadatos, detecta duplicados, propón cronoloxía e agrupacións por lugar ou evento, xera unha páxina HTML e propón nomes. Non move nin borra nada sen aprobación: escribe só na carpeta de saída.
- **Verificas ti.** Revisa 20 fotos agrupadas. Confirma os duplicados antes de eliminar nada. Mira o que pasa coas fotos sen EXIF.
- **Alcance mínimo.** 200 fotos e unha cronoloxía.
- **Depende de** que o espazo poida ler imaxes e metadatos. Verifica onde se procesan.

### C2. Taller de vídeo local · [Novo] · 🎞️ 🔊

- **Idea.** Montaxe dunha curtametraxe, un time-lapse ou un stop-motion con clips propios.
- **Fontes.** Clips propios e música con licenza clara.
- **O axente fai.** Pide un plan de montaxe (planos, duración, ritmo), executa cortes, concatenación e subtítulos con ferramentas de vídeo do entorno (p. ex. ffmpeg, se está instalado) e renderiza unha previa en baixa resolución.
- **Verificas ti.** Ves a previa. Aprobas o plan **antes** do render final. Comprobas a licenza da música.
- **Alcance mínimo.** Un a dous minutos, entre seis e dez planos.
- **Depende de** que as ferramentas de vídeo estean dispoñibles no espazo do curso.

### C3. Do píxel ao fío · [Novo] · 🖼️ 🧩

- **Idea.** Converter unha imaxe nun patrón de punto de cruz, ganchillo ou mosaico, con lista de fíos.
- **Fontes.** Unha imaxe propia e unha carta de cores de fíos que ti proporciones.
- **O axente fai.** Reduce a imaxe a unha cuadrícula e unha paleta limitada, asocia cada cor ao fío máis próximo, e xera un patrón imprimible con cantidades.
- **Verificas ti.** Proba un cadrado de 10×10 con fío real. Revisa que as cores da carta existen. Axusta a paleta.
- **Alcance mínimo.** Unha imaxe de 40×40 e unha paleta de dez cores.
- **Semente.** «Reduce esta imaxe a 40×40 con só 10 cores da miña carta. Antes de xerar o patrón mostra a vista previa e dime que detalles se perden.»

### C4. Paleta dun lugar · [Novo] · 🖼️ 🧩

- **Idea.** Extraer a paleta dunha serie de fotos ou cadros dun lugar e compoñer un estudo de cor.
- **Fontes.** Fotos propias ou imaxes de dominio público.
- **O axente fai.** Calcula as cores dominantes por imaxe, agrúpaas, xera unha paleta HTML con códigos, simula combinacións e explica o contraste.
- **Verificas ti.** Axuízaa a ollo: ¿representa o lugar? Comproba o contraste texto/fondo con criterios de accesibilidade.
- **Alcance mínimo.** Dez imaxes e unha paleta de seis cores.

---

## D. Música e son

### D1. Do asubío á partitura · [Novo] · 🔊 🧩

- **Idea.** Gravación propia dunha melodía → alturas e ritmos → MIDI ou partitura.
- **Fontes.** Unha melodía simple, sen acompañamento, cantada, asubiada ou tocada.
- **O axente fai.** Detecta alturas e duracións con ferramenta de análise (se hai), cuantifica ritmos, xera MIDI ou notación textual (p. ex. ABC) e reprodúceo. Marca onde dubida.
- **Verificas ti.** Compara de oído orixinal e transcrición. Revisa os pasos marcados como dubidosos.
- **Alcance mínimo.** Entre 8 e 16 compases.
- **Depende de** que haxa unha biblioteca de análise de audio. Se non, parte dunha lista de notas preparada.

### D2. Contrapunto auditado · [Novo] · 🔊 🧩

- **Idea.** Compoñer cunhas regras explícitas e un **verificador** que as comproba, e iterar ata cumprilas. É o ciclo plan-execución-verificación en estado puro.
- **Fontes.** Unha lista de regras que ti elixes. Versión sen teoría: «só pentatónica, saltos máximos dunha quinta, final na tónica».
- **O axente fai.** Escribe o verificador, xera a peza, verifica, corrixe e informa de cada iteración.
- **Verificas ti.** Reproduce a peza. Proba o verificador con exemplos que **deben fallar** (un verificador malo é peor que ningún).
- **Alcance mínimo.** Unha melodía de 8 compases e cinco regras.
- **Semente.** «Escribe primeiro un verificador destas regras e proba que detecta violacións. Só despois xera a melodía e itera.»

### D3. Por que o piano está «desafinado» · [Novo] · 🧩 🔊 📊

- **Idea.** Laboratorio interactivo de afinación pitagórica, xusta e temperada.
- **Fontes.** As razóns de frecuencias que ti dás (3/2, 2^(7/12)…).
- **O axente fai.** Calcula as escalas, constrúe un HTML con xerador de tons e visualización de batimentos, e explica a coma pitagórica.
- **Verificas ti.** Calcula a man dous intervalos. Escoita os batimentos. Comproba que a coma pitagórica sae preto de 23,5 cents.
- **Alcance mínimo.** Tres sistemas de afinación e un intervalo comparable.

### D4. Mapa sonoro da contorna · [Mantido] · 🔊 🗺️

- **Idea.** Percorrido xeolocalizado de gravacións con fichas.
- **Fontes.** Gravacións propias curtas con data e lugar. Sen conversas identificables.
- **O axente fai.** Organiza metadatos, xera fichas e mapa, e propón categorías (xeofonía, biofonía, antropofonía).
- **Verificas ti.** Etiqueta escoitando e non só por proposta. Revisa localizacións.
- **Alcance mínimo.** Seis puntos.

### D5. Xogo de escoita: instrumentos do mundo · [Fusión] · 🧩 🔊 🗺️

Fusiona: Catálogo de instrumentos do mundo + Xogo musical interactivo.

- **Idea.** Cuestionario de escoita en HTML con clips, mapa de orixe e fichas.
- **Fontes.** Clips con licenza aberta, verificando a licenza e a atribución de cada un.
- **O axente fai.** Selecciona clips que cumpran a licenza, escribe as fichas, fai o mapa de orixe e programa o xogo.
- **Verificas ti.** Licenza e atribución por clip. Orixe e clasificación de cada instrumento.
- **Alcance mínimo.** Dez clips e un cuestionario.

---

## E. Artes, creatividade e afeccións

### E1. Comisario de exposición imposible · [Fusión] · 🔎 🖼️ 🧩

Fusiona: Exposición virtual de patrimonio + Galería de técnicas plásticas.

- **Idea.** Unha exposición virtual sobre un tema propio, con obras de museos que ofrecen colección en acceso aberto.
- **Fontes.** Colecións abertas (p. ex. Met Museum, Art Institute of Chicago ou Europeana, verificando a API e a licenza de cada imaxe). Só imaxes marcadas como dominio público ou CC0.
- **O axente fai.** Dado o tema, consulta a API, filtra por licenza, selecciona entre 10 e 12 pezas, escribe textos de sala e crea un micrositio con liña temporal. Para cada peza rexistra ID, URL e licenza.
- **Verificas ti.** Abre tres URL e confirma peza e autoría. Busca datas ou atribucións inventadas nos textos de sala. Revisa licenzas.
- **Alcance mínimo.** Dez pezas e un micrositio dunha páxina.
- **Semente.** «O tema é "o mar". Só podes usar obras que a API marque como libres de dereitos. Para cada peza garda ID, URL e licenza nun CSV antes de escribir ningún texto.»

### E2. Instrucións á LeWitt · [Novo] · 🧩 🖼️

- **Idea.** Escribes unha instrución de debuxo ao estilo de Sol LeWitt e o axente a executa como arte xerativa en SVG. Compáranse as interpretacións diverxentes da mesma instrución.
- **Fontes.** As túas instrucións.
- **O axente fai.** Interpreta a instrución literalmente, indica as ambigüidades que atopa **antes** de executar, xera SVG con semente aleatoria e produce varias versións.
- **Verificas ti.** Compara as saídas: onde diverxen, a instrución era ambigua. Reescribe e repite. Opcional: exporta SVG para plóter, serigrafía ou corte.
- **Alcance mínimo.** Tres instrucións e tres versións por instrución.
- **Idea de fondo.** A precisión da instrución determina a precisión do resultado. É o mellor exemplo para explicar un bo encargo.

### E3. Taller de xogos de mesa · [Novo] · 🗂 📊 🧩

- **Idea.** Deseñas un xogo sinxelo e o axente simula milleiros de partidas para detectar desequilibrios (primeiro xogador demasiado favorecido, estratexias dominantes, duración).
- **Fontes.** Regras escritas por ti, curtas e sen ambigüidade.
- **O axente fai.** Converte as regras nun simulador, executa entre 5.000 e 10.000 partidas con estratexias sinxelas, informa de estatísticas e propón axustes.
- **Verificas ti.** Xoga dúas partidas a man seguindo o simulador paso a paso para ver se implementa **as túas regras**. Non aceptes estatísticas se o simulador non cumpre as regras.
- **Alcance mínimo.** Un xogo para dúas persoas con regras dunha páxina.
- **Depende de** que o espazo permita executar código.

### E4. Catalogador dunha colección · [Novo] · 🖼️ 🔎 📊

- **Idea.** Fotos dunha colección (minerais, moedas, discos, cromos…) → fichas catalogadas.
- **Fontes.** Fotos propias e unha referencia que ti elixas (catálogo ou base aberta).
- **O axente fai.** Propón os campos da ficha, identifica cada peza con nivel de confianza, contrasta coa referencia e xera un catálogo HTML ou CSV, destacando as identificacións dubidosas.
- **Verificas ti.** Contrasta as dubidosas coa referencia ou cun experto. Non aceptes valoracións económicas sen fonte.
- **Alcance mínimo.** Entre 15 e 20 pezas.

---

## F. Linguas e pensamento crítico

### F1. Practicador con verdade fixada · [Novo, central] · 🧩 🗂

Ver o documento independente `LABORATORIO_SINTAXE_RAZONAMENTO.md`.

- **Idea.** Unha ferramenta de práctica na que a corrección vén dun banco de elementos validados polo docente, non do modelo. Exemplo principal: análise sintáctica en 4º de ESO. Outros: formulación química, conxugación, cronoloxías, unidades físicas.
- **Fontes.** Un banco de 20 a 30 elementos redactados ou validados polo docente, cos seus erros típicos.
- **O axente fai.** Deseña a estrutura de datos, propón distractores e pistas, escribe a app que corrixe contra o banco e **non xulga por si mesmo**.
- **Verificas ti.** Cada elemento do banco ten a túa sinatura. Proba o feedback con tres erros deliberados.
- **Alcance mínimo.** Dez elementos e un modo de práctica.
- **Lección.** O axente fabrica, a persoa fixa a verdade, o código verifica.

### F2. Oulipo con verificador · [Novo] · 🧩 🗂

- **Idea.** Textos con restricións (lipogramas, palíndromos, acrósticos…) e un verificador en código que comproba se se cumpren.
- **Fontes.** As restricións que ti elixas.
- **O axente fai.** Escribe o verificador, redacta o texto, verifica e corrixe, mostrando o reconto de erros en cada intento.
- **Verificas ti.** Proba o verificador con frases que deben fallar. Le o texto: cumprir a regra non garante calidade literaria.
- **Alcance mínimo.** Tres restricións e un texto curto por restrición.
- **Lección.** Os modelos fallan en tarefas de letra a letra e a ferramenta compensa o fallo.

### F3. Revisor de galego con fontes autorizadas · [Novo] · 🗂 🔎

- **Idea.** Revisión normativa dun texto limitada ás fontes autorizadas do proxecto. O axente só propón cambios que poida citar e marca o resto como «sen fonte».
- **Fontes.** Textos normativos e dicionarios oficiais, ou unha lista de dominios permitidos, verificando condicións de uso.
- **O axente fai.** Le o texto, marca as posibles incidencias, e para cada unha cita a fonte (entrada ou regra) ou escribe «sen fonte».
- **Verificas ti.** Contrasta dez propostas coa fonte. Busca falsos positivos (corrixir o que está ben). A decisión final é humana.
- **Alcance mínimo.** Un texto de 300 palabras.
- **Semente.** «Revisa este texto só con estas fontes. Se non podes citar a regra, non propoñas o cambio.»

### F4. Museo de erros de IA · [Mantido, proxecto estrela] · 🧩 🗂

- **Idea.** Colección comentada de erros reais (alucinacións, sesgos, citas inventadas, aritmética) con unha proba de verificación para cada un.
- **Fontes.** Casos que provocas durante o curso, documentando prompt, resposta e verificación. Nunca con datos persoais.
- **O axente fai.** Axuda a deseñar probas que provoquen erros, cataloga e clasifica, e crea fichas e un museo HTML.
- **Verificas ti.** Cada ficha ten a evidencia (a fonte que desmente). Repite o prompt e anota a variación.
- **Alcance mínimo.** Seis erros ben documentados.

### F5. Detector de afirmacións dubidosas · [Mantido] · 🔎 🗂

- **Idea.** Protocolo de verificación: dada unha afirmación, descompóñela, busca fontes primarias e fai unha ficha de contraste.
- **Fontes.** Unha lista permitida (organismos oficiais, bases de datos) e tres afirmacións escollidas.
- **O axente fai.** Descompón en afirmacións comprobables, busca, asigna un veredicto con nivel de evidencia e sinala o que non se pode comprobar.
- **Verificas ti.** Abre as fontes citadas. Distingue «falso» de «non verificable».
- **Alcance mínimo.** Tres afirmacións.

---

## G. Inclusión e apoio educativo

### G1. Xerador de historias sociais · [Mantido] · 🗂 🖼️

- **Idea.** Fichas personalizables para situacións cotiás, con pictogramas.
- **Fontes.** Situacións **sintéticas** redactadas por ti (nunca alumnado real), unha guía recoñecida da estrutura das historias sociais e un banco de pictogramas con licenza (p. ex. ARASAAC, verificando condicións).
- **O axente fai.** Adapta a situación, redacta seguindo a guía e asocia pictogramas.
- **Verificas ti.** Lista de comprobación da guía. Revisión por unha persoa de orientación antes de usar con ninguén real.
- **Alcance mínimo.** Tres situacións.

### G2. Tradutor a lectura fácil · [Mantido] · 🗂 🖼️

- **Idea.** Biblioteca de textos adaptados con pictogramas e verificación.
- **Fontes.** Textos administrativos públicos e as pautas de lectura fácil vixentes (verificar a versión).
- **O axente fai.** Aplica as pautas, xera a versión adaptada e un informe de cambios que indica que pauta aplicou en cada punto.
- **Verificas ti.** Contrasta coa lista de pautas. A validación real corresponde a persoas lectoras con dificultades de lectura, non só ao axente.
- **Alcance mínimo.** Un texto dunha páxina.

---

# Parte 3 · Proxectos orixinais pendentes de criba fina

Non entraron na criba anterior. A columna é unha primeira impresión, non unha decisión.

| Proxecto orixinal | Primeira impresión |
| --- | --- |
| Atlas de expresións galegas | Bo se se alimenta dun corpus con fontes; risco de inventar expresións. Solapa con **Revisor de galego**. |
| Adaptador multilingüe | Perigo de cuasi-chat (traducir). Só é axéntico con glosario e verificación por falantes. |
| Observatorio meteorolóxico local | Solapa con **Clima da miña aldea** e **Observatorio do ceo**. Candidato a fusión. |
| Guía de seguridade dixital familiar | Probable cuasi-chat. Reforzar con simulacións de fraude sintéticas. |
| Explorador de datos demográficos | Mesmo patrón que **Visualizador do orzamento público**. Fusionar ou manter como alternativa. |
| Banda sonora para unha historia | Depende de licenzas. Reforzar con verificación de licenza ou ligar con **Taller de vídeo local**. |
| Adestrador de hábitos activos | Cuasi-chat e con risco de datos de saúde. |
| Deseño dunha identidade visual | Xeración de imaxe en chat. Candidato a retirar ou a ligar con **Paleta dun lugar**. |
| Coreografía explicada | Orixinal pero depende de vídeo ou audio. Revisar a viabilidade. |
| Planificador visual de rutinas | Útil. Usar só datos sintéticos. Solapa con **Xerador de historias sociais**. |
| Itinerario de patrimonio industrial | Mesma ficha que **Ruta literaria local** con outras fontes. |
| Observatorio de noticias locais | Solapa con **Detector de afirmacións dubidosas**. |
| Proxecto de horta ou xardín | Interesante se se liga a datos meteorolóxicos reais; se non, cuasi-chat. |
| Plan de acollida para persoas recentemente chegadas | Valioso pero esixe información actualizada e coidado cos datos. Candidato a outra edición. |
| Mapa de rutas seguras a pé ou en bicicleta | Solapa con **Guía de accesibilidade do barrio**. |
| Kit de experimentos reproducibles | Reforzar con rexistro de datos reais e análise. |

---

# Parte 4 · Orde suxerida para probar antes de clase

Escollidos pola súa boa relación entre esforzo e valor demostrativo.

1. **Contrapunto auditado** (D2). Demostra o ciclo de verificación con pouca preparación.
2. **Instrucións á LeWitt** (E2). Mostra que un prompt é unha instrución e que a ambigüidade se paga.
3. **Detective da factura da luz** (A3). Parte dunha factura propia, con cálculo comprobable.
4. **Clima da miña aldea** (A4). Datos externos por API e un tema moi teu (tendencia fronte a ruído).
5. **Practicador con verdade fixada** (F1). O proxecto que máis xeneraliza; ver o documento específico.

Para cada un: escribe a ficha de deseño antes de arrancar, pide o plan, e anota onde fallou o axente. Esas incidencias son o mellor material do curso.
