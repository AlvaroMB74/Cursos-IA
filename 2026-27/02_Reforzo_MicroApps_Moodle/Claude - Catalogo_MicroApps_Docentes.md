# Catálogo de Micro-Aplicaciones Web de Iniciación para Docentes

**20 herramientas interactivas en un único `index.html`**: HTML5, CSS y JavaScript integrados, sin servidor, sin backend y sin APIs externas. Se abren con doble clic, viajan en un pendrive y se incrustan en un `<iframe>` de Moodle.

## Principios comunes de todas las fichas

- **Un solo archivo.** El SVG va escrito directamente en el HTML (`<svg>` en línea), animado con `@keyframes` CSS o manipulado con JavaScript (`setAttribute`, `requestAnimationFrame`).
- **Cero red.** Nada de CDN en el código final si se quiere garantía de funcionamiento offline. Cuando se cite una librería, se puede pegar su código minificado dentro de una etiqueta `<script>`.
- **Sonido nativo.** Web Audio API (osciladores y envolventes) para efectos sin ningún archivo de audio.
- **Persistencia local.** `localStorage` para guardar datos en el propio navegador. Siempre dentro de `try/catch`, porque algunos entornos (iframes restringidos, modo privado) lo bloquean.
- **Diseño adaptable.** Unidades relativas, `viewBox` en los SVG y eventos `pointer` (sirven igual para ratón, dedo y pizarra digital).

---

# 1. Ciencias y STEM

### 1. Taller de Engranajes Vivos
* **Área / Temática:** Tecnología, Física (mecánica, relación de transmisión)
* **Tipología de Artefacto:** Simulador con SVG animado
* **Funcionalidad Principal (Qué hace el usuario):** El alumnado coloca de 2 a 4 ruedas dentadas en una cadena y elige el número de dientes de cada una con un deslizador. Al girar la manivela de la primera, ve cómo giran las demás, en qué sentido y a qué velocidad, y la app calcula la relación de transmisión en directo.
* **Componente Visual / Animación SVG:** Cada engranaje es un `<path>` generado por JavaScript a partir del número de dientes. La rotación se aplica con `transform: rotate()` calculada según la proporción real de dientes, de modo que lo que se ve coincide con la fórmula. Una flecha de color marca el sentido de giro de cada rueda.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS. Una función `crearEngranaje(dientes, radio)` genera el trazado y un bucle con `requestAnimationFrame` actualiza los ángulos.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Toda la lógica es una división y un signo. No hay datos externos ni estado complejo, y el resultado es espectacular desde la primera versión.

### 2. Circuito Vivo: Serie contra Paralelo
* **Área / Temática:** Física y Tecnología (electricidad, ley de Ohm)
* **Tipología de Artefacto:** Simulador con SVG animado
* **Funcionalidad Principal (Qué hace el usuario):** Se monta un circuito con pila, interruptor y hasta tres bombillas, y se alterna entre conexión en serie y en paralelo con un botón. Al cerrar el interruptor, las bombillas se encienden con distinta intensidad y se muestran voltaje, intensidad y resistencia total.
* **Componente Visual / Animación SVG:** Pequeños círculos (electrones) recorren los cables a lo largo de los trazados con `stroke-dashoffset` y su velocidad depende de la intensidad calculada. El brillo de cada bombilla cambia con `opacity` y un filtro de desenfoque. Si una bombilla se «funde», el flujo se corta en esa rama.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS. Dos fórmulas (suma de resistencias y paralelo) y un par de `if`.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Los cálculos caben en diez líneas. Los trazados de los cables son rectángulos sencillos, lo que reduce el riesgo de errores de dibujo de la IA.

### 3. Círculo Trigonométrico Vivo
* **Área / Temática:** Matemáticas (trigonometría, funciones periódicas)
* **Tipología de Artefacto:** Simulador con SVG animado
* **Funcionalidad Principal (Qué hace el usuario):** Se arrastra un punto sobre la circunferencia unidad y se leen en tiempo real el ángulo (grados y radianes), el seno y el coseno. A la derecha se va dibujando la gráfica de la función elegida (seno, coseno o tangente) a medida que el punto gira.
* **Componente Visual / Animación SVG:** Los segmentos de seno y coseno se estiran y se encogen con el punto, con colores coherentes entre la circunferencia y la gráfica. Una línea de puntos horizontal une el punto con su ordenada en la curva, de modo que se ve de dónde sale la onda. Los ángulos notables (30°, 45°, 60°...) actúan como imanes.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS con eventos `pointer` y `Math.sin`/`Math.cos`. No hace falta ninguna librería.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Es geometría de coordenadas polares con una sola variable de estado (el ángulo). Casi no hay forma de que falle.

### 4. Viaje de una Gota de Sangre
* **Área / Temática:** Biología (aparato circulatorio)
* **Tipología de Artefacto:** Esquema interactivo con animación SVG
* **Funcionalidad Principal (Qué hace el usuario):** El alumnado sigue una gota de sangre por el corazón, los pulmones y el cuerpo. Con el botón «Siguiente parada» avanza por aurícula, ventrículo, arteria pulmonar, pulmón, vena pulmonar y así hasta cerrar el circuito, y en cada parada aparece una ficha explicativa. Un modo «Latido» deja correr todo en bucle.
* **Componente Visual / Animación SVG:** La gota se desplaza a lo largo de un `<path>` mediante `offset-path` en CSS o con `getPointAtLength()` en JavaScript. La sangre cambia de rojo oscuro (pobre en oxígeno) a rojo vivo (oxigenada) según el tramo. Las cuatro cámaras laten con un `@keyframes scale`.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS. El recorrido es un array de paradas con coordenadas, texto y color.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Es un esquema fijo, sin cálculo, donde la IA solo debe encadenar un trazado y una lista de paradas. Los errores, si los hay, son visuales y se corrigen en una iteración.

### 5. Balanza de Átomos
* **Área / Temática:** Química (ajuste de ecuaciones, ley de conservación de la masa)
* **Tipología de Artefacto:** Minijuego/Quiz visual
* **Funcionalidad Principal (Qué hace el usuario):** Aparece una reacción sin ajustar, por ejemplo H₂ + O₂ → H₂O. El usuario sube o baja los coeficientes con botones + y − hasta que la balanza se equilibra, y el contador de átomos de cada elemento se pone verde cuando coincide en ambos lados.
* **Componente Visual / Animación SVG:** Las moléculas se dibujan con círculos de colores (un color por elemento) y se multiplican al cambiar el coeficiente. Un fiel de balanza SVG se inclina según la diferencia de átomos y se estabiliza con un rebote cuando la ecuación está ajustada, con lluvia de chispas como recompensa.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS. Un array de reacciones con sus fórmulas descompuestas en `{elemento: cantidad}`. Opcionalmente, Web Audio para un «ding» al acertar.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** La comprobación es una simple suma por elemento. Se puede empezar con tres reacciones y ampliar el banco sin tocar la lógica.

---

# 2. Letras y Humanidades

### 6. Línea del Tiempo Elástica
* **Área / Temática:** Historia (cualquier etapa), también Literatura y Arte
* **Tipología de Artefacto:** Esquema interactivo desplegable
* **Funcionalidad Principal (Qué hace el usuario):** Se explora un eje cronológico que se estira y se encoge con la rueda del ratón o el gesto de pellizco. Al acercarse aparecen los hitos pequeños, y al hacer clic en uno se despliega una tarjeta con fecha, descripción y su relación con otros hechos. Un filtro por colores separa política, cultura y ciencia.
* **Componente Visual / Animación SVG:** El eje y los hitos son elementos SVG cuya posición se recalcula con una escala lineal. Las tarjetas se despliegan con una transición suave y unos arcos curvos unen causas y consecuencias. El profesorado puede editar los datos desde un único bloque JSON al principio del archivo.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS. Los hitos viven en un array de objetos y el zoom es una transformación `viewBox`.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Es el patrón «datos + dibujo» más puro. Cambiar de tema es reemplazar un array, sin tocar el código.

### 7. Taller de Métrica Poética
* **Área / Temática:** Literatura y Lengua (métrica, rima, figuras)
* **Tipología de Artefacto:** Análisis poético interactivo
* **Funcionalidad Principal (Qué hace el usuario):** Se muestra un poema de dominio público (por ejemplo, de Rosalía de Castro, Manrique o Bécquer) con cada verso dividido en sílabas. El alumnado toca las sílabas para marcar las tónicas, une vocales con sinalefas y colorea las rimas. La app comprueba el resultado contra el análisis correcto, previamente cargado.
* **Componente Visual / Animación SVG:** Sobre cada verso se dibujan arcos SVG que unen las sinalefas y puntos que marcan los acentos. Las rimas conectan las palabras finales con hilos de color que se «iluminan» al acertar, y un contador de sílabas métricas aparece al final de cada línea.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS. El poema se carga con las sílabas ya separadas manualmente, lo que evita implementar un silabeador automático, que suele fallar con diptongos y hiatos.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Al usar datos pre-etiquetados, la IA no tiene que resolver lingüística computacional: solo pintar, comparar y puntuar.

### 8. La Caverna de Platón en Movimiento
* **Área / Temática:** Filosofía (mito de la caverna, conocimiento y apariencia)
* **Tipología de Artefacto:** Simulador con SVG animado
* **Funcionalidad Principal (Qué hace el usuario):** En una escena dividida en dos mitades, el usuario mueve objetos delante de una hoguera y observa cómo cambian las sombras proyectadas en la pared. Después avanza por cinco etapas (cadenas, sombras, liberación, salida, regreso) con un texto breve y una pregunta de debate en cada una.
* **Componente Visual / Animación SVG:** Las sombras son copias deformadas de los objetos, con `transform` y desenfoque, que se recalculan al arrastrar. En la etapa de salida, el fondo pasa del tono de cueva al luminoso del exterior con un fundido, y los prisioneros se animan con movimientos sutiles.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS. Las cinco etapas son un array y un índice. Proyección de sombras simplificada con una escala y un desplazamiento.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Es una escena estática con una sola interacción de arrastre y una máquina de estados lineal. Convierte un tema abstracto en algo que se puede tocar.

### 9. La Casa de las Preposiciones
* **Área / Temática:** Idiomas (inglés, preposiciones de lugar: in, on, under, next to, between...)
* **Tipología de Artefacto:** Minijuego/Quiz visual
* **Funcionalidad Principal (Qué hace el usuario):** Una voz o un texto da una orden («Put the cat under the table») y el alumno arrastra el personaje al lugar correcto de la casa. Si acierta, el gato se acomoda con una animación y sube la puntuación; si falla, la app muestra dónde estaba la posición correcta.
* **Componente Visual / Animación SVG:** Una casa vista en corte con mesa, cama, ventana y armario, todo en SVG. El gato (o el personaje elegido) reacciona: se sienta, salta o se esconde según la posición. Un cuaderno SVG va coleccionando las frases ya dominadas.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS. Zonas de destino definidas como rectángulos invisibles, comprobación por colisión. La Web Speech API puede leer las frases, pero conviene tener el texto siempre visible porque las voces disponibles dependen del dispositivo.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Arrastrar y soltar con zonas de destino es una técnica estándar que la IA domina. Se puede reutilizar para cualquier vocabulario visual cambiando el decorado.

### 10. Mondrian Machine: Laboratorio de Composición
* **Área / Temática:** Educación Plástica y Visual (color, equilibrio, composición)
* **Tipología de Artefacto:** Simulador con SVG animado
* **Funcionalidad Principal (Qué hace el usuario):** Se divide un lienzo en rectángulos tocando para trazar líneas, se pinta cada zona con la paleta de Mondrian o con otras paletas (Bauhaus, Pop Art) y se puede pulsar «Sorpréndeme» para generar una composición aleatoria. Un indicador muestra el equilibrio visual según el peso de cada color.
* **Componente Visual / Animación SVG:** Los rectángulos son `<rect>` que se subdividen con una transición de crecimiento. Un modo «diagnóstico» superpone un mapa de calor del peso visual y dibuja el centro de gravedad de la composición como un punto móvil.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS. División recursiva de rectángulos. Botón de descarga del lienzo como `.svg` con `Blob` y `URL.createObjectURL` (todo local).
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Genera arte con reglas muy simples y siempre queda bien. Además, permite que el alumnado guarde y compare sus propias obras.

---

# 3. Educación Infantil / Primaria Inicial

### 11. El Monstruo de las Emociones
* **Área / Temática:** Educación emocional (reconocer y nombrar emociones)
* **Tipología de Artefacto:** Juego táctil con SVG animado
* **Funcionalidad Principal (Qué hace el usuario):** Un monstruito grande ocupa la pantalla. El niño toca botones con iconos (alegría, tristeza, enfado, miedo, sorpresa, calma) y la cara del monstruo cambia al instante. Un segundo modo pregunta «¿Cómo está el monstruo?» y el niño elige la cara correcta entre tres.
* **Componente Visual / Animación SVG:** Cejas, ojos y boca son trazados SVG que se transforman suavemente de una emoción a otra (`d` del `<path>` con transición). El monstruo cambia de color, tiembla de enfado, llora con lágrimas animadas o salta de alegría. Un sonido distinto acompaña cada emoción.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS con Web Audio para sonidos simples (tonos ascendentes para alegría, descendentes para tristeza).
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Son seis estados predefinidos con parámetros numéricos. La IA solo debe interpolar entre ellos.

### 12. La Granja de los Números
* **Área / Temática:** Matemáticas iniciales (conteo y cardinalidad del 1 al 10)
* **Tipología de Artefacto:** Minijuego/Quiz visual
* **Funcionalidad Principal (Qué hace el usuario):** Aparece un número grande y el niño toca animales en el prado para contarlos hasta llegar a él. Cada animal que se toca salta, hace un sonido y muestra el número que le corresponde. Al completar la cuenta, llega una celebración.
* **Componente Visual / Animación SVG:** Animales muy simples hechos con formas geométricas (círculos, óvalos, triángulos), reutilizables con distintos colores. Al tocarlos rebotan y un contador de huevos o manzanas va llenando una cesta visible. Con cada acierto, el sol del fondo se anima.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS con Web Audio. Opcionalmente, una pequeña lluvia de confeti hecha en `<canvas>` propio, sin librería.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Mecánica de un solo toque, sin texto que leer y con retroalimentación inmediata. Es una de las categorías donde la IA acierta casi siempre.

### 13. Letras Mágicas
* **Área / Temática:** Lectoescritura inicial (fonética y relación letra-sonido)
* **Tipología de Artefacto:** Juego táctil con SVG animado
* **Funcionalidad Principal (Qué hace el usuario):** Se muestra una letra grande. Al tocarla suena su fonema y la letra se transforma en un dibujo (la M en una montaña, la S en una serpiente, la L en una luna). Después el niño trazará con el dedo la letra siguiendo una guía punteada.
* **Componente Visual / Animación SVG:** El trazado de la letra se anima con `stroke-dashoffset` para enseñar el orden del trazo, y luego se «metamorfosea» en el dibujo asociado. Una estrella de recompensa aparece al terminar el trazo correctamente.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS. Como no todos los dispositivos disponen de voces en español sin conexión, los sonidos pueden ser tonos propios con Web Audio, y la lectura de la palabra con `speechSynthesis` se deja como mejora opcional.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Se puede empezar con 5 letras y ampliar. La animación de trazo es una técnica clásica de SVG que las IAs resuelven bien.

### 14. El Reloj de las Rutinas
* **Área / Temática:** Rutinas diarias y noción de tiempo (mañana, tarde, noche)
* **Tipología de Artefacto:** Juego de ordenar con SVG animado
* **Funcionalidad Principal (Qué hace el usuario):** El niño arrastra tarjetas de actividades (despertarse, desayunar, ir al cole, comer, bañarse, dormir) a los huecos de un día dibujado. Al colocar cada una correctamente, el sol avanza por el cielo; al acabar el día, llega la noche con estrellas.
* **Componente Visual / Animación SVG:** El cielo es un degradado SVG que cambia con el tiempo del día, con un sol y una luna que recorren un arco. Los objetos de cada rutina (cama, tazón, mochila) son iconos sencillos que se animan al colocarse en su lugar.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS con eventos `pointer`. Orden correcto guardado en un array. El docente puede editar las rutinas desde un bloque JSON.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Arrastrar y comprobar un orden es lógica trivial, y el cambio del cielo es una sola interpolación de color.

### 15. El Tren de las Formas
* **Área / Temática:** Geometría inicial, colores y discriminación visual
* **Tipología de Artefacto:** Minijuego/Quiz visual
* **Funcionalidad Principal (Qué hace el usuario):** Un tren con vagones vacíos espera en la estación. Cada vagón tiene una silueta (círculo, cuadrado, triángulo, estrella). El niño arrastra las formas de colores al vagón que corresponde. Cuando el tren se llena, arranca con sonido de silbato y se va por la vía.
* **Componente Visual / Animación SVG:** Las siluetas son versiones grises de las formas. Al encajar, la forma se «ilumina» con su color y el vagón da un saltito. Las ruedas giran con `@keyframes` y el humo de la locomotora son círculos que suben y se desvanecen.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS. Silbato y traqueteo con Web Audio. Opción de ampliar con una puntuación que se guarda en `localStorage`.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Formas geométricas simples, detección de colisión por distancia y una animación final lucida. Resultado muy vistoso con muy poco código.

---

# 4. Uso Personal y Productividad del Docente

### 16. Los Frascos de Dinero
* **Área / Temática:** Finanzas personales (presupuesto por sobres)
* **Tipología de Artefacto:** Dashboard de datos locales
* **Funcionalidad Principal (Qué hace el usuario):** Se crean «frascos» para cada categoría de gasto (vivienda, ocio, ahorro, imprevistos...) con una cantidad mensual asignada. Cada gasto que se apunta vacía un poco el frasco correspondiente, y a final de mes se ve cuánto queda en cada uno y cuánto se ha ahorrado.
* **Componente Visual / Animación SVG:** Cada frasco es un SVG con líquido cuyo nivel baja con una animación de ola suave. El color pasa de verde a ámbar y a rojo conforme se vacía. Cuando un frasco se agota, tiembla ligeramente, y al final del mes un resumen en barras muestra el balance.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS con `localStorage`. Botón de exportar e importar los datos como archivo `.json` para hacer copia de seguridad en el pendrive.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Sumas y restas con persistencia local. No hay que conectar con ningún banco y los datos nunca salen del equipo, lo que además es una buena lección de privacidad.

### 17. Temporizador Paisaje
* **Área / Temática:** Gestión del tiempo y concentración (técnica Pomodoro)
* **Tipología de Artefacto:** Temporizador visual
* **Funcionalidad Principal (Qué hace el usuario):** Se elige la duración de un bloque de trabajo y una escena. Mientras se trabaja, el paisaje cambia lentamente: un sol que baja hasta el atardecer, una vela que se consume o un árbol que crece. Al terminar suena un carillón suave y empieza un descanso con otra escena.
* **Componente Visual / Animación SVG:** El elemento central (sol, vela, árbol) se anima con una única variable de progreso entre 0 y 1 que controla posición, tamaño y color. Un halo suave reemplaza a los números, para que el tiempo se perciba sin mirar un cronómetro.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS con `requestAnimationFrame` y comparación de marcas de tiempo (`Date.now()`), no con `setInterval`, para que no se desajuste. Carillón con Web Audio.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Una sola variable de estado y un solo bucle. Es el ejemplo perfecto para entender qué significa «progreso» como número entre 0 y 1.

### 18. La Rueda del Bienestar
* **Área / Temática:** Bienestar personal (equilibrio entre áreas de la vida)
* **Tipología de Artefacto:** Dashboard de datos locales
* **Funcionalidad Principal (Qué hace el usuario):** Una vez por semana se puntúan del 1 al 10 ocho áreas de la vida (descanso, familia, amistades, salud, trabajo, aficiones, aprendizaje, tiempo propio). La app dibuja el resultado como un gráfico de radar y permite superponer semanas anteriores para ver la evolución.
* **Componente Visual / Animación SVG:** El polígono del radar se deforma con una transición suave al mover cada deslizador. Las semanas pasadas se muestran como contornos translúcidos de otros colores y el área más baja late suavemente para invitar a prestarle atención.
* **Ingeniería Frontend Sugerida:** SVG propio calculado con trigonometría básica (sin Chart.js, para evitar dependencias) y `localStorage` para el historial.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Un gráfico de radar son puntos en una circunferencia, algo que la IA resuelve de forma fiable. Es un buen ejemplo de herramienta privada, de uso íntimo, sin servidor.

### 19. Constelación de Hábitos
* **Área / Temática:** Hábitos y constancia (ejercicio, lectura, descanso, aprendizaje...)
* **Tipología de Artefacto:** Dashboard de datos locales
* **Funcionalidad Principal (Qué hace el usuario):** Se definen hasta cinco hábitos y cada día se marca con un toque lo cumplido. Cada marca enciende una estrella en un cielo nocturno. Con las estrellas de un mismo hábito se va formando una constelación, y las rachas largas las unen con líneas luminosas.
* **Componente Visual / Animación SVG:** El cielo es un SVG con estrellas que parpadean con `@keyframes`. Al marcar un día, la estrella aparece con un destello. Los hábitos fallados dejan una estrella apagada, sin castigo visual, y a final de mes la constelación puede descargarse como imagen `.svg`.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS con `localStorage`. Posición de las estrellas generada con una semilla fija por hábito, para que la constelación sea siempre la misma.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** Una lista de fechas por hábito y un dibujo derivado. Es un ejemplo claro de cómo convertir datos personales en algo bello sin enviarlos a ninguna parte.

### 20. Perfil de Ruta: Cuaderno de Senderismo
* **Área / Temática:** Aficiones y viajes (senderismo, ciclismo, rutas a pie)
* **Tipología de Artefacto:** Dashboard de datos locales
* **Funcionalidad Principal (Qué hace el usuario):** Se anotan los puntos de una ruta (kilómetro y altitud) o se pegan desde una tabla, y la app dibuja el perfil de altitud, calcula desnivel acumulado, distancia y tiempo estimado, y guarda la ruta en un cuaderno con fecha, notas y valoración. Una mejora opcional permite cargar un archivo `.gpx` desde el disco, procesado localmente.
* **Componente Visual / Animación SVG:** El perfil se dibuja como un área SVG con degradado. Un marcador se desliza por la curva siguiendo el cursor y muestra altitud y pendiente en cada punto, con colores que indican los tramos duros. Al abrir una ruta guardada, el trazo se dibuja progresivamente.
* **Ingeniería Frontend Sugerida:** Puro HTML/CSS/JS con `localStorage`. Para el `.gpx` opcional, `FileReader` y `DOMParser`, ambos nativos y sin red.
* **Por qué es un proyecto "Básico / Ideal para iniciarse":** La versión mínima (tabla de puntos y perfil) es muy sencilla. El `.gpx` queda como extensión para quien quiera dar un paso más.

---

## Cómo usar este catálogo

Cada ficha puede convertirse en un prompt de partida con esta fórmula:

> «Crea un único archivo `index.html` autocontenido (HTML, CSS y JavaScript integrados, sin librerías externas ni peticiones de red) que implemente: [pegar la ficha]. El SVG debe ir en línea y animado con CSS o JavaScript. Diseño adaptable a móvil y pizarra digital.»

Un buen ejercicio de iniciación es pedir la versión mínima (una sola pantalla y una sola interacción) y después pedir una mejora por iteración: sonido, persistencia, un segundo nivel.
