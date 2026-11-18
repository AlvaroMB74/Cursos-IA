# Catálogo de Micro-Aplicaciones Web de Iniciación para Docentes

Este catálogo reúne **20 propuestas de micro-aplicaciones web autocontenidas** diseñadas para funcionar en un único archivo `index.html`. No requieren servidores, bases de datos ni conexiones a internet tras su descarga: pueden ejecutarse directamente desde un pendrive, proyectarse en la pizarra digital o incrustarse en un bloque HTML/iframe de Moodle o Google Sites. 

El eje central de todas las propuestas es el uso de **ilustraciones y animaciones vectoriales SVG integradas** directamente en el código, manipuladas mediante CSS y JavaScript nativo para maximizar el impacto visual y didáctico.

---

## 1. Ciencias y STEM

### 1. El Laboratorio de Engranajes y Transmisiones
- **Área / Temática:** Tecnología, Física (Mecánica básica) y Matemáticas (Proporcionalidad).
- **Tipología de Artefacto:** Simulador físico-visual interactivo con parámetros ajustables.
- **Funcionalidad Principal (Qué hace el usuario):** El docente o el alumnado selecciona el número de dientes de dos o tres ruedas dentadas acopladas y ajusta la velocidad y el sentido de giro del motor principal mediante deslizadores. La aplicación calcula y muestra en tiempo real las revoluciones por minuto (RPM) de salida y la relación de transmisión.
- **Componente Visual / Animación SVG:** Un lienzo `<svg>` genera dinámicamente los perfiles dentados de los engranajes mediante trigonometría en JavaScript. Al activar el motor, cada rueda gira con una velocidad angular proporcional y en sentido inverso a la anterior, mostrando flechas vectoriales dinámicas que indican el par motor y la dirección del movimiento.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3 y JavaScript puro (manipulación del atributo `transform="rotate()"` en nodos SVG y cálculos trigonométricos básicos para dibujar dientes).
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** Toda la física se reduce a una regla de tres inversa ($N_1 \cdot \omega_1 = N_2 \cdot \omega_2$). Una IA genera el algoritmo de dibujo de polígonos SVG y el bucle `requestAnimationFrame` con total precisión sin depender de motores de física externos.

### 2. Ciclo del Agua Vivo y Climático
- **Área / Temática:** Ciencias Naturales, Biología y Geografía.
- **Tipología de Artefacto:** Esquema interactivo animado con control de variables ambientales.
- **Funcionalidad Principal (Qué hace el usuario):** El usuario manipula dos controles: "Temperatura Ambiental" (de $-10^\circ\text{C}$ a $45^\circ\text{C}$) y "Cobertura Forestal" (de deforestado a bosque denso). Según los valores elegidos, el paisaje reacciona mostrando cómo varían la evaporación, la condensación, el tipo de precipitación (lluvia o nieve) y la infiltración subterránea.
- **Componente Visual / Animación SVG:** Una ilustración vectorial panorámica (montaña, río, mar, nubes y acuífero) con múltiples capas `<g>`. Mediante `keyframes` CSS controlados por variables CSS (`--velocidad-evaporacion`), suben flechas onduladas translúcidas desde el mar, las nubes cambian de color y tamaño, y caen gotas o copos de nieve SVG que recargan el nivel azul del acuífero subterráneo.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3 (variables CSS dinámicas + animaciones `stroke-dashoffset`) y JavaScript nativo.
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** Consiste en mostrar, ocultar o cambiar la velocidad de capas SVG predefinidas mediante condicionales `if/else` sencillos, lo que elimina cualquier riesgo de errores de lógica compleja.

### 3. Constructor de Circuitos Eléctricos Seguros
- **Área / Temática:** Física y Tecnología (Electricidad básica).
- **Tipología de Artefacto:** Banco de pruebas virtual y simulador de flujo eléctrico.
- **Funcionalidad Principal (Qué hace el usuario):** El alumnado dispone de una placa base con interruptores, pilas de distinto voltaje, bombillas y resistencias que puede activar o desactivar haciendo clic. El sistema detecta si el circuito está cerrado, abierto o en cortocircuito, calculando la intensidad de corriente mediante la Ley de Ohm.
- **Componente Visual / Animación SVG:** Un diagrama esquemático en `<svg>` donde los cables están dibujados con trazos discontinuos (`stroke-dasharray`). Al cerrar el interruptor, una animación CSS desplaza los puntos a lo largo del cable simulando el flujo de electrones; las bombillas emiten un halo radial amarillo (`<radialGradient>`) cuya opacidad depende de la potencia, y si hay cortocircuito, la pila vibra y muestra chispas vectoriales.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3, JavaScript puro y Web Audio API (para emitir un leve zumbido eléctrico o un sonido de chispa/alerta en caso de sobrecarga).
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** El estado del circuito se modela con simples variables booleanas (`interruptor1 = true`). La IA estructura fácilmente el grafo visual en SVG sin requerir librerías matemáticas pesadas.

### 4. El Pulso del Corazón y la Circulación Sanguínea
- **Área / Temática:** Biología y Anatomía Humana (Educación Primaria y Secundaria).
- **Tipología de Artefacto:** Infografía anatómica animada con modo exploración y simulador de ritmo cardíaco.
- **Funcionalidad Principal (Qué hace el usuario):** El usuario puede alternar entre estados físicos ("Reposo", "Caminando", "Sprint") para observar cómo cambian las pulsaciones por minuto (BPM), además de hacer clic sobre aurículas, ventrículos y arterias para desplegar tarjetas explicativas sobre la sangre oxigenada y desoxigenada.
- **Componente Visual / Animación SVG:** Un corazón vectorial estilizado en `<svg>` con cuatro cavidades diferenciadas por colores (rojo brillante y azul violáceo) y válvulas que se abren y cierran. Mediante escalado rítmico en CSS (`scale()`), las aurículas y ventrículos se contraen de forma secuencial (sístole y diástole) mientras pequeños círculos SVG viajan por los conductos pulmonares y sistémicos.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3, JavaScript nativo y Web Audio API (sintetizador de onda sinusoidal grave para reproducir el sonido *lub-dub* sincronizado con cada latido visual).
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** La sincronización entre un temporizador `setInterval` en JS, un pulso visual SVG y un tono de Web Audio API requiere menos de 150 líneas de código limpias y autoexplicativas.

### 5. Balanza Algebraica de Ecuaciones
- **Área / Temática:** Matemáticas (Iniciación al Álgebra y Ecuaciones de primer grado).
- **Tipología de Artefacto:** Manipulativo virtual interactivo para resolver incógnitas.
- **Funcionalidad Principal (Qué hace el usuario):** Se presenta una ecuación visual (ej. $2x + 3 = 9$) representada con pesas etiquetadas como "$X$" y unidades de "$1$" en ambos platillos de una balanza. El estudiante debe aplicar la misma operación en ambos lados (añadir o quitar unidades, o dividir por la mitad) hasta dejar una sola "$X$" aislada en equilibrio.
- **Componente Visual / Animación SVG:** Una balanza clásica dibujada en `<svg>` cuyo brazo superior pivota (`transform: rotate()`) con transición suave (`cubic-bezier`) según la diferencia de peso real entre el platillo izquierdo y el derecho. Cuando ambos lados vuelven a igualarse, el fiel central se alinea con una marca verde y emite un destello vectorial.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3, JavaScript nativo y `canvas-confetti` (opcional vía CDN o simulado con partículas SVG) al resolver la ecuación.
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** La lógica matemática detrás es aritmética elemental (sumas y divisiones enteras) y el movimiento del brazo SVG depende únicamente de restar el valor total de un platillo frente al otro.

---

## 2. Letras y Humanidades

### 6. Máquina de Análisis Morfosintáctico "Caja de Cristal"
- **Área / Temática:** Lengua Castellana y Literatura / Sintaxis.
- **Tipología de Artefacto:** Analizador visual interactivo por bloques encajables.
- **Funcionalidad Principal (Qué hace el usuario):** El docente carga una batería de oraciones predefinidas (o escribe una nueva en un cuadro de texto) y el alumno selecciona palabras consecutivas para agruparlas en sintagmas (SN, SV, SPrep) y asignarles su función (Sujeto, Predicado, CD, CI, CC) mediante botones de colores.
- **Componente Visual / Animación SVG:** En lugar de tablas rígidas, la aplicación genera dinámicamente llaves vectoriales `<svg>` (`<path>` con curvas de Bézier) y cajas anidadas con bordes redondeados debajo de cada grupo de palabras. Al agrupar palabras, las llaves se dibujan con una animación fluida de trazo (`stroke-dashoffset`) y se colorean según la jerarquía sintáctica.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3 y JavaScript puro (cálculo de coordenadas `getBoundingClientRect()` de cada palabra para trazar las llaves SVG exactas debajo).
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** No requiere procesamiento de lenguaje natural (NLP) complejo, ya que es una herramienta de manipulación y etiquetado visual guiado por el usuario o validado contra respuestas preconfiguradas en un objeto JSON local.

### 7. Cronología Visual de Civilizaciones e Historia
- **Área / Temática:** Historia, Geografía e Historia del Arte.
- **Tipología de Artefacto:** Línea del tiempo interactiva con zoom y filtros temáticos.
- **Funcionalidad Principal (Qué hace el usuario):** El usuario navega horizontalmente por una línea temporal (por ejemplo, de la Prehistoria a la Edad Contemporánea, o los siglos de oro de la literatura), filtrando hitos por categorías (arte, ciencia, conflictos, inventos) y haciendo clic en cada nodo para desplegar fichas ilustradas.
- **Componente Visual / Animación SVG:** Una cinta temporal continua renderizada en `<svg>` donde los distintos periodos históricos se representan como bandas onduladas de colores que se ensanchan o contraen. Los hitos aparecen como medallones vectoriales con iconos temáticos en SVG (una corona, un pergamino, un engranaje) que aumentan de escala y despliegan un conector animado hacia la tarjeta de información.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3 (Scroll Snap y transiciones suaves) y JavaScript nativo con datos estructurados en un array local.
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** Es una renderización directa de una lista de eventos ordenados por año; la IA genera tanto el código de visualización como una base de datos histórica inicial lista para usar.

### 8. El Laboratorio de Métrica y Rima Poética
- **Área / Temática:** Literatura (Poesía y Métrica española).
- **Tipología de Artefacto:** Editor de análisis poético asistido con visualización rítmica.
- **Funcionalidad Principal (Qué hace el usuario):** El estudiante elige un poema clásico o escribe una estrofa propia y hace clic entre vocales para marcar sinalefas o hiatos, y selecciona si la palabra final es aguda ($+1$), llana ($0$) o esdrújula ($-1$). La herramienta recuenta las sílabas en tiempo real y deduce el esquema de rima (arte mayor o menor).
- **Componente Visual / Animación SVG:** Sobre el texto del poema se superpone una capa `<svg>` transparente que dibuja arcos curvos verdes bajo las sinalefas unidas por el alumno, barras verticales de separación silábica y una partitura visual a la derecha donde cada verso se representa como una barra de progreso musical que cambia de color cuando alcanza la medida exacta (ej. 11 sílabas para un endecasílabo).
- **Ingeniería Frontend Sugerida:** HTML5, CSS3 y JavaScript nativo (uso de expresiones regulares básicas para separar sílabas y detectar terminaciones vocálicas/consonánticas).
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** La interacción principal se basa en alternar estados visuales al hacer clic sobre letras o espacios, una tarea muy directa y libre de dependencias externas.

### 9. Mapa Conceptual de Filosofía y Corrientes de Pensamiento
- **Área / Temática:** Filosofía, Ética y Literatura Universal.
- **Tipología de Artefacto:** Grafo de conocimiento interactivo y comparador de ideas.
- **Funcionalidad Principal (Qué hace el usuario):** El alumno explora un mapa de nodos conectados (ej. Racionalismo vs. Empirismo, o Platón vs. Aristóteles). Al hacer clic en un filósofo o concepto, se iluminan sus influencias directas (flechas verdes) y sus opuestos (flechas rojas), abriendo un panel lateral con citas célebres y preguntas de debate.
- **Componente Visual / Animación SVG:** Un lienzo `<svg>` interactivo con nodos circulares y líneas conectoras curvas (`<path>`). Al seleccionar un nodo, los nodos no relacionados reducen su opacidad (`opacity: 0.25`) y las líneas activas muestran partículas de luz viajando desde el autor hacia sus conceptos clave mediante la etiqueta nativa `<animateMotion>` de SVG.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3 y JavaScript puro (sin necesidad de librerías pesadas como D3.js, usando coordenadas porcentuales predefinidas en el SVG).
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** Al trabajar con un conjunto cerrado de 8 a 15 nodos en un `viewBox` fijo, la IA puede posicionar los elementos con exactitud milimétrica sin algoritmos complejos de física de grafos.

### 10. La Ruleta de Historias y Conectores Narrativos (Story Cubes Digitales)
- **Área / Temática:** Expresión Escrita, Idiomas Extranjeros (Inglés, Francés) y Creatividad.
- **Tipología de Artefacto:** Generador lúdico de disparadores creativos y temporizador de escritura.
- **Funcionalidad Principal (Qué hace el usuario):** El docente o el grupo pulsa "Lanzar Dados" para obtener 5 iconos aleatorios (personaje, lugar, objeto mágico, conflicto, emoción) junto con 3 conectores gramaticales obligatorios en el idioma elegido. Incluye un botón para bloquear dados individuales y un reloj de cuenta atrás para redactar el microrrelato.
- **Componente Visual / Animación SVG:** Cinco dados isométricos dibujados en `<svg>` que realizan una animación de rotación y rebote en 2D al lanzarse, revelando ilustraciones vectoriales limpias y expresivas en su interior. Alrededor del panel, un anillo de progreso SVG disminuye suavemente su longitud de trazo indicando el tiempo restante para escribir.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3, JavaScript nativo y Web Audio API (sonido sintetizado de dados rodando sobre madera y campana suave al finalizar el tiempo).
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** Es una selección aleatoria de arrays de iconos SVG (`Math.random()`), ideal para generar un resultado visualmente muy rico y colorido en segundos.

---

## 3. Educación Infantil / Primaria Inicial

### 11. El Monstruo de las Emociones: Termómetro y Respiración
- **Área / Temática:** Educación Emocional, Asamblea y Tutoría en Infantil.
- **Tipología de Artefacto:** Personaje interactivo expresivo y guía de relajación visual.
- **Funcionalidad Principal (Qué hace el usuario):** Los niños y niñas tocan en la pizarra digital los botones de emociones básicas (Alegría, Calma, Tristeza, Enfado, Miedo) para identificar cómo se sienten hoy. Si seleccionan "Enfado" o "Miedo", aparece un botón de "Respirar juntos" que guía una inhalación y exhalación pausada.
- **Componente Visual / Animación SVG:** Un personaje simpático construido íntegramente en `<svg>` donde las cejas, los ojos, la boca y el color del cuerpo se transforman suavemente mediante transiciones CSS (`d` path morphing o rotación de elementos) para adoptar cada expresión. En el modo respiración, la barriga del personaje y una flor vectorial en su mano se expanden durante 4 segundos y se contraen durante 4 segundos.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3 (transiciones de color y escala) y Web Audio API (acordes musicales suaves y ascendentes/descendentes acompañando el ritmo de respiración).
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** Cambiar atributos de color (`fill`) y ángulos de cejas/bocas en un personaje SVG es una de las tareas más agradecidas y sencillas de codificar para una IA.

### 12. Tren de las Sílabas y Fonética Divertida
- **Área / Temática:** Lectoescritura, Conciencia Fonológica e Iniciación a la Lectura.
- **Tipología de Artefacto:** Juego táctil de construcción de palabras por arrastrar o tocar.
- **Funcionalidad Principal (Qué hace el usuario):** Aparece una locomotora y el dibujo de un objeto cotidiano (ej. *PA-TO*, *CA-SA*, *PE-LO-TA*). El alumno debe tocar en orden los vagones con las sílabas correctas (entre varias opciones) para engancharlos al tren y hacer que este arranque.
- **Componente Visual / Animación SVG:** Una locomotora colorida en `<svg>` con ruedas que giran, bielas articuladas y volutas de humo circulares que suben y se desvanecen. Cada vez que el niño acierta una sílaba, el vagón se desliza hacia la locomotora con un efecto de rebote elástico; al completar la palabra, el tren cruza toda la pantalla pitando.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3, JavaScript nativo, Web Speech API (`speechSynthesis` nativo del navegador para pronunciar cada sílaba y la palabra completa en voz alta) y Web Audio API (silbato de tren).
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** Utiliza la síntesis de voz nativa del navegador sin archivos `.mp3` externos y se basa en comparar cadenas de texto muy cortas.

### 13. La Máquina de Contar y Sumar Frutas
- **Área / Temática:** Matemáticas Manipulativas (Conteo, Cardinalidad y Sumas hasta el 10/20).
- **Tipología de Artefacto:** Máquina dispensadora interactiva con refuerzo visual y auditivo.
- **Funcionalidad Principal (Qué hace el usuario):** El niño pulsa dos grandes botones con números o iconos para introducir manzanas o naranjas por dos tubos superiores de una máquina. Las frutas caen en una cesta central transparente donde se agrupan automáticamente de 5 en 5 (estructura de *ten-frame*) para facilitar el conteo visual del resultado.
- **Componente Visual / Animación SVG:** Una máquina de estilo dibujo animado en `<svg>` con tubos translúcidos, una palanca que baja al pulsarla y frutas vectoriales que caen siguiendo trayectorias curvas. Cuando se alcanza el total correcto en modo reto, los ojos de la máquina guiñan y lanza estrellas vectoriales por la chimenea.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3 (animaciones `@keyframes` de caída y rebote) y Web Audio API (sonido de *pop* ascendente cada vez que cae una fruta, subiendo el tono musical con cada unidad).
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** El uso de tonos musicales crecientes vinculados a un contador numérico (`frecuencia = 261 + contador * 30`) es trivial de programar y tiene un enorme valor pedagógico para interiorizar la cantidad.

### 14. Semáforo del Ruido y Reloj Visual de Asamblea
- **Área / Temática:** Gestión de Aula, Rutinas Diarias y Autorregulación en Infantil/Primaria.
- **Tipología de Artefacto:** Herramienta ambiental de aula con temporizador visual no numérico.
- **Funcionalidad Principal (Qué hace el usuario):** El docente selecciona el clima de trabajo deseado (Silencio/Lectura, Voz baja/Parejas, Trabajo en equipo) y fija un tiempo de actividad (de 1 a 30 minutos) mediante iconos de reloj de arena. Los alumnos ven en todo momento cuánto tiempo queda sin necesidad de saber leer las horas.
- **Componente Visual / Animación SVG:** Un gran semáforo ilustrado con caras amigables en cada luz (verde sonriente, ámbar atento, rojo pidiendo calma) junto a un disco solar o pastel en `<svg>` (`stroke-dasharray` circular) que se va ocultando progresivamente como un reloj *Time Timer* clásico, revelando debajo un dibujo sorpresa cuando el tiempo llega a cero.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3, JavaScript nativo y Web Audio API (sonido suave de cuenco tibetano o xilófono al terminar el tiempo, evitando alarmas estridentes).
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** El famoso efecto *Time Timer* se logra en SVG con un solo elemento `<circle>` manipulando su propiedad `stroke-dashoffset` mediante un temporizador simple.

### 15. Granja de los Sonidos y Siluetas
- **Área / Temática:** Conocimiento del Entorno, Atención Visual y Discriminación Auditiva.
- **Tipología de Artefacto:** Juego de asociación sombra-figura con descubrimiento animado.
- **Funcionalidad Principal (Qué hace el usuario):** En un escenario de campo o selva aparecen tres siluetas oscuras escondidas tras arbustos y un botón de altavoz. Al pulsar el altavoz o tocar una silueta, el niño debe emparejar el animal con su sombra o encontrar quién se esconde detrás de cada elemento del paisaje.
- **Componente Visual / Animación SVG:** Un paisaje en `<svg>` con arbustos, nubes y granero en capas. Las siluetas son los mismos grupos SVG de los animales con un filtro CSS `brightness(0)`; al acertar, el filtro se desactiva con una transición suave, revelando los colores del animal, que da un pequeño salto alegre mientras los arbustos se apartan a los lados.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3 (filtros visuales y transformaciones) y Web Speech API / Web Audio API para efectos lúdicos de acierto.
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** Reutilizar el mismo dibujo SVG tanto para la sombra (mediante CSS `filter: brightness(0)`) como para el animal descubierto ahorra la mitad del código gráfico y garantiza una coincidencia perfecta.

---

## 4. Uso Personal y Productividad del Docente

### 16. Oasis de Desconexión: Pausas Activas y Regla 20-20-20
- **Área / Temática:** Bienestar Docente, Salud Visual y Ergonomía tras la jornada escolar.
- **Tipología de Artefacto:** Asistente de descanso visual y guía de estiramientos suaves.
- **Funcionalidad Principal (Qué hace el usuario):** Cuando el docente está en casa preparando clases o corrigiendo frente al ordenador, activa este temporizador de bienestar. Cada 20 minutos lanza una pausa visual de 20 segundos para descansar la vista (regla 20-20-20) y propone un estiramiento cervical o de espalda con una guía visual clara.
- **Componente Visual / Animación SVG:** Un paisaje minimalista zen en `<svg>` (un lago tranquilo con ondas concéntricas que se expanden lentamente y un sol que desciende suavemente). Durante los 20 segundos de descanso ocular, un punto focal animado guía la mirada hacia el horizonte lejano mientras una figura humana articulada en líneas SVG muestra la postura del estiramiento recomendado.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3, JavaScript nativo y Web Audio API (sonido suave de gota de agua o campana zen).
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** Es una máquina de estados muy simple (Estado Trabajo $\rightarrow$ Estado Descanso $\rightarrow$ Estado Estiramiento) con animaciones CSS puras y relajantes.

### 17. Presupuesto Mensual "Regla 50 / 30 / 20" sin Hojas de Cálculo
- **Área / Temática:** Finanzas Personales y Ahorro Doméstico.
- **Tipología de Artefacto:** Dashboard visual de distribución de ingresos y gastos locales.
- **Funcionalidad Principal (Qué hace el usuario):** El usuario introduce sus ingresos mensuales netos y va registrando gastos rápidos categorizados en Necesidades (50%), Deseos/Ocio (30%) y Ahorro/Inversión (20%). La aplicación calcula al instante si se está desviando de los porcentajes ideales y guarda los datos automáticamente en el navegador.
- **Componente Visual / Animación SVG:** Un gráfico de anillo (donut chart) interactivo dibujado en `<svg>` puro (usando arcos circulares con `stroke-dasharray`) acompañado de tres "frascos de cristal" vectoriales cuyo nivel de líquido animado sube o baja con ondas suaves según el saldo disponible en cada categoría.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3, JavaScript nativo y `localStorage` (para conservar los datos en el navegador del usuario sin enviar información financiera a ningún servidor).
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** La privacidad total está garantizada gracias a `localStorage`, y los gráficos de anillo en SVG requieren apenas 20 líneas de código, evitando dependencias externas.

### 18. Jardín de Hábitos: Rastreador Visual de Rutinas Personales
- **Área / Temática:** Desarrollo Personal, Deporte, Lectura o Autocuidado.
- **Tipología de Artefacto:** Tracker de constancia gamificado mediante crecimiento orgánico.
- **Funcionalidad Principal (Qué hace el usuario):** El docente define de 1 a 4 hábitos personales fuera del trabajo (ej. "Caminar 30 min", "Leer 15 páginas", "No mirar el correo del centro después de las 19:00"). Cada día que marca un hábito como cumplido, su planta virtual crece una etapa y mantiene su racha activa.
- **Componente Visual / Animación SVG:** Una maceta ilustrada en `<svg>` para cada hábito. Según el número de días completados en el mes, el código revela progresivamente nuevas hojas, tallos más altos, capullos y finalmente flores coloridas que se mecen suavemente con el viento gracias a animaciones CSS `rotate()`. Si pasan varios días sin marcarse, las hojas se inclinan ligeramente.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3, JavaScript nativo y `localStorage` para guardar el historial diario y calcular las rachas.
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** Consiste en vincular un contador entero almacenado en `localStorage` con la visibilidad de grupos `<g>` dentro de un SVG botánico.

### 19. Organizador Visual de Maletas y Escapadas de Fin de Semana
- **Área / Temática:** Viajes, Tiempo Libre y Organización Doméstica.
- **Tipología de Artefacto:** Checklist inteligente por perfiles de viaje con progreso gráfico.
- **Funcionalidad Principal (Qué hace el usuario):** El usuario selecciona el tipo de escapada (Playa, Montaña, Ciudad, Viaje en coche) y la duración en días. La aplicación genera una lista de equipaje ajustada automáticamente (calculando prendas según los días) donde puede tachar elementos o añadir los suyos propios.
- **Componente Visual / Animación SVG:** Una maleta abierta ilustrada en `<svg>` en la parte superior de la pantalla. A medida que se marcan casillas de la lista, pequeños iconos vectoriales (camiseta, pasaporte, cargador, botas) vuelan suavemente hacia el interior de la maleta y, al llegar al 100%, la tapa de la maleta se cierra y se abrochan las correas con una animación de confirmación.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3, JavaScript nativo y `localStorage` (con botón de "Reiniciar viaje" para reutilizar la app en futuras escapadas).
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** Es una evolución visualmente muy atractiva de la clásica lista de tareas (*To-Do List*), el ejercicio estrella que cualquier IA programa sin fallos en el primer intento.

### 20. Planificador Semanal de Menús y Lista de la Compra Automática
- **Área / Temática:** Hogar, Cocina y Organización Familiar.
- **Tipología de Artefacto:** Tablero semanal de comidas con extractor automático de ingredientes.
- **Funcionalidad Principal (Qué hace el usuario):** El usuario asigna comidas y cenas de lunes a domingo eligiendo de un recetario base editable (o pulsando "Sugerir menú equilibrado aleatorio"). Con un solo clic en "Generar Lista", la aplicación agrupa todos los ingredientes necesarios de la semana por secciones del supermercado (Frutería, Despensa, Frescos).
- **Componente Visual / Animación SVG:** Un plato ilustrado en `<svg>` dividido en sectores nutricionales (verduras, proteínas, hidratos) que se colorea dinámicamente conforme se planifica el menú del día, junto con iconos vectoriales minimalistas para cada categoría de alimentos en la lista de la compra interactiva.
- **Ingeniería Frontend Sugerida:** HTML5, CSS3, JavaScript nativo y `localStorage` para guardar el menú de la semana y las recetas favoritas del docente.
- **Por qué es un proyecto "Básico / Ideal para iniciarse":** El cruce de arrays (recetas $\rightarrow$ ingredientes) y el almacenamiento en `localStorage` es lógica pura de manipulación de listas en JavaScript, completamente autónoma y extremadamente útil en el día a día.