Catálogo de Micro-Aplicaciones Web de Iniciación para Docentes

1\. Ciencias y STEM

1\. La Fábrica de Engranajes

\- Área / Temática: Tecnología, Física y Matemáticas. Máquinas simples, transmisión del movimiento y proporcionalidad.

\- Tipología de Artefacto: Simulador mecánico interactivo con SVG animado.

\- Funcionalidad Principal (Qué hace el usuario): El usuario coloca engranajes de distintos tamaños, conecta sus dientes y activa un motor. Puede modificar la velocidad de giro del engranaje principal y observar cómo se transmite el movimiento al resto del mecanismo.

\- Componente Visual / Animación SVG: Engranajes vectoriales que giran mediante CSS @keyframes o transformaciones JavaScript. Flechas animadas indican el sentido de giro y etiquetas muestran las relaciones de transmisión.

\- Ingeniería Frontend Sugerida: SVG inline, CSS animations, JavaScript para calcular velocidades angulares y relaciones de transmisión. Sin dependencias externas.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": Los engranajes pueden dibujarse con formas SVG sencillas. La lógica matemática es elemental y las animaciones CSS permiten conseguir resultados espectaculares sin motores físicos.

2\. Laboratorio de Reacciones Químicas

\- Área / Temática: Química. Estructura atómica, moléculas y reacciones químicas.

\- Tipología de Artefacto: Simulador molecular visual con esquema interactivo.

\- Funcionalidad Principal (Qué hace el usuario): El usuario selecciona diferentes elementos químicos y construye moléculas arrastrando átomos a una zona de trabajo. Puede activar una reacción sencilla, como la formación de agua, y comprobar cómo se reorganizan los átomos conservando la materia.

\- Componente Visual / Animación SVG: Átomos representados como esferas vectoriales con símbolos químicos. Los enlaces son líneas SVG animadas que aparecen y desaparecen durante las reacciones.

\- Ingeniería Frontend Sugerida: SVG inline, JavaScript para gestionar posiciones y enlaces, Drag \& Drop nativo y CSS animations.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": Se puede limitar a un conjunto pequeño de reacciones predefinidas. No requiere cálculos químicos complejos ni simulación molecular real.

3\. Ecosistema en Equilibrio

\- Área / Temática: Biología y Ciencias Naturales. Cadenas tróficas y equilibrio de los ecosistemas.

\- Tipología de Artefacto: Simulador ecológico con visualización dinámica.

\- Funcionalidad Principal (Qué hace el usuario): El usuario modifica las poblaciones de productores, herbívoros y depredadores mediante controles deslizantes. Al avanzar el tiempo, observa cómo evolucionan las poblaciones y qué sucede cuando desaparece una especie o se introduce una nueva.

\- Componente Visual / Animación SVG: Paisaje SVG con árboles, plantas y animales animados. Los animales pueden desplazarse, aparecer o desaparecer según la población simulada.

\- Ingeniería Frontend Sugerida: SVG inline, JavaScript para un modelo simplificado de población, CSS animations y controles HTML nativos.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": El modelo puede utilizar reglas matemáticas sencillas y datos ficticios. La parte visual se construye con ilustraciones SVG reutilizables.

4\. El Universo en tus Manos

\- Área / Temática: Astronomía, Física y Ciencias Naturales. Sistema solar, gravedad y movimientos planetarios.

\- Tipología de Artefacto: Simulador astronómico interactivo.

\- Funcionalidad Principal (Qué hace el usuario): El usuario selecciona planetas, modifica la velocidad de la simulación y detiene el tiempo para observar sus posiciones relativas. Puede consultar información de cada planeta y comparar tamaños y distancias mediante escalas didácticas.

\- Componente Visual / Animación SVG: Sistema solar vectorial con órbitas elípticas, planetas giratorios y estrellas parpadeantes. Al seleccionar un planeta, se destaca visualmente y aparece una ficha informativa.

\- Ingeniería Frontend Sugerida: SVG inline, CSS keyframes, JavaScript para controlar las órbitas y LocalStorage para recordar preferencias.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": Los movimientos se pueden representar con funciones trigonométricas sencillas. No necesita datos astronómicos en tiempo real ni conexión a internet.

5\. Circuitos Eléctricos: ¡Que Fluya la Energía!

\- Área / Temática: Física y Tecnología. Electricidad, circuitos en serie y paralelo.

\- Tipología de Artefacto: Constructor de circuitos eléctricos interactivo.

\- Funcionalidad Principal (Qué hace el usuario): El usuario conecta pilas, interruptores, cables y bombillas para construir circuitos. Al cerrar el interruptor, comprueba si el circuito está correctamente conectado y observa cómo cambia el brillo de las bombillas.

\- Componente Visual / Animación SVG: Circuitos dibujados mediante trazados SVG. Pequeños electrones luminosos recorren los cables y las bombillas se iluminan mediante filtros y cambios de color.

\- Ingeniería Frontend Sugerida: SVG inline, JavaScript para validar conexiones, CSS animations y Web Audio API opcional para sonidos de interruptores.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": Se puede empezar con circuitos predefinidos y reglas lógicas sencillas, sin necesidad de implementar un simulador eléctrico profesional.



2\. Letras y Humanidades

6\. La Máquina del Tiempo

\- Área / Temática: Historia. Cronología de acontecimientos históricos.

\- Tipología de Artefacto: Línea temporal interactiva y narrativa visual.

\- Funcionalidad Principal (Qué hace el usuario): El usuario desplaza un selector temporal para viajar por distintas épocas históricas. Puede descubrir acontecimientos, personajes, inventos y transformaciones sociales, así como comparar simultáneamente distintas civilizaciones.

\- Componente Visual / Animación SVG: Línea temporal SVG que se desplaza horizontalmente. Los acontecimientos aparecen mediante ilustraciones animadas y pequeños elementos visuales relacionados con cada época.

\- Ingeniería Frontend Sugerida: SVG inline, JavaScript, CSS transitions y un objeto JSON integrado en el propio HTML con los acontecimientos.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": Los contenidos se almacenan directamente en el código. La interacción consiste fundamentalmente en filtrar y presentar información.

7\. Detective de Palabras

\- Área / Temática: Lengua y Literatura. Morfología, sintaxis y categorías gramaticales.

\- Tipología de Artefacto: Analizador lingüístico visual y minijuego educativo.

\- Funcionalidad Principal (Qué hace el usuario): El usuario introduce una oración y selecciona palabras para clasificarlas como sustantivos, verbos, adjetivos, determinantes, etc. La aplicación permite descubrir las funciones sintácticas mediante ejemplos guiados y ejercicios de autocorrección.

\- Componente Visual / Animación SVG: Las palabras se convierten en tarjetas de colores que encajan en diferentes compartimentos gramaticales. Un detective SVG animado ofrece pistas y reacciona ante los aciertos.

\- Ingeniería Frontend Sugerida: HTML, CSS, JavaScript, Drag \& Drop nativo y SVG inline. Banco de oraciones predefinidas en JSON.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": No hace falta implementar un analizador lingüístico real. Puede funcionar mediante ejercicios preparados y clasificación manual, con una lógica de corrección muy sencilla.

8\. El Museo de los Estilos Artísticos

\- Área / Temática: Historia del Arte. Arquitectura, pintura y movimientos artísticos.

\- Tipología de Artefacto: Galería interactiva y explorador visual.

\- Funcionalidad Principal (Qué hace el usuario): El usuario explora diferentes estilos artísticos, descubre sus características y compara sus elementos visuales. Puede modificar los parámetros de una obra ficticia para transformarla entre estilos, por ejemplo, impresionista, cubista o geométrico.

\- Componente Visual / Animación SVG: Obras vectoriales originales cuyos colores, formas, patrones y composiciones cambian al seleccionar cada movimiento artístico.

\- Ingeniería Frontend Sugerida: SVG inline, CSS variables, JavaScript para modificar atributos SVG y filtros CSS.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": No necesita reconocimiento de imágenes ni inteligencia artificial. Las transformaciones se consiguen modificando propiedades visuales de ilustraciones vectoriales preparadas.

9\. El Poeta Interactivo

\- Área / Temática: Lengua y Literatura. Poesía, métrica, rima y figuras retóricas.

\- Tipología de Artefacto: Taller creativo y analizador poético visual.

\- Funcionalidad Principal (Qué hace el usuario): El usuario selecciona palabras y construye versos mediante un banco de vocabulario. Puede experimentar con diferentes estructuras métricas, buscar rimas y descubrir recursos literarios mediante ejemplos interactivos.

\- Componente Visual / Animación SVG: Versos que aparecen como trazos de escritura animada. Las sílabas métricas se representan mediante pequeñas partículas y las rimas se conectan mediante líneas de colores.

\- Ingeniería Frontend Sugerida: HTML, CSS, JavaScript, SVG inline y Web Audio API opcional para acompañamiento sonoro.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": Puede limitarse a una colección de palabras y versos previamente preparados. La detección de rimas puede realizarse mediante coincidencias de terminaciones.

10\. Babel: Viaje entre Idiomas

\- Área / Temática: Idiomas. Vocabulario, expresiones cotidianas y comprensión lingüística.

\- Tipología de Artefacto: Minijuego visual de asociación y aprendizaje.

\- Funcionalidad Principal (Qué hace el usuario): El usuario relaciona palabras con sus traducciones, completa expresiones y resuelve pequeños retos de vocabulario. Puede seleccionar distintos idiomas y niveles de dificultad.

\- Componente Visual / Animación SVG: Personajes viajeros que visitan distintos países, bocadillos animados y tarjetas ilustradas. Los aciertos provocan animaciones de celebración y desbloquean nuevos escenarios.

\- Ingeniería Frontend Sugerida: JavaScript, SVG inline, CSS animations, LocalStorage para guardar progresos y Web Speech API opcional para pronunciar palabras.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": Todo el vocabulario puede almacenarse en un pequeño diccionario JSON. No requiere traductores automáticos ni servicios externos.



3\. Educación Infantil / Primaria Inicial

11\. La Orquesta de las Emociones

\- Área / Temática: Educación Emocional. Identificación y expresión de emociones.

\- Tipología de Artefacto: Juego visual interactivo y herramienta de educación emocional.

\- Funcionalidad Principal (Qué hace el usuario): El niño selecciona una emoción y modifica los rasgos faciales de un personaje para expresarla. Puede escuchar pequeñas melodías asociadas a cada emoción y relacionar situaciones cotidianas con diferentes estados emocionales.

\- Componente Visual / Animación SVG: Caritas SVG con ojos, cejas y bocas independientes que cambian de posición. El personaje puede sonreír, llorar, sorprenderse, enfadarse o relajarse mediante animaciones.

\- Ingeniería Frontend Sugerida: SVG inline, JavaScript para modificar atributos y clases CSS, Web Audio API para generar sonidos sencillos.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": Una cara vectorial se construye con círculos y curvas. La animación depende únicamente de cambiar unas pocas propiedades visuales.

12\. El Tren de las Letras

\- Área / Temática: Educación Infantil y Lengua. Reconocimiento de letras, fonética y conciencia fonológica.

\- Tipología de Artefacto: Minijuego de asociación visual y auditiva.

\- Funcionalidad Principal (Qué hace el usuario): El niño debe seleccionar la letra que corresponde al sonido escuchado o completar palabras sencillas colocando letras en los vagones de un tren. La aplicación ofrece pistas visuales y refuerzo positivo.

\- Componente Visual / Animación SVG: Un tren animado recorre la pantalla con vagones que contienen letras. Cuando el niño acierta, la locomotora avanza y aparecen estrellas y pequeñas animaciones de celebración.

\- Ingeniería Frontend Sugerida: SVG inline, CSS keyframes, JavaScript, Web Speech API para reproducir sonidos de letras cuando esté disponible y sonidos alternativos mediante Web Audio API.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": Las palabras y respuestas se preparan previamente. El movimiento del tren se resuelve con CSS y la lógica del juego es una sencilla comprobación de respuestas.

13\. El Jardín de los Números

\- Área / Temática: Matemáticas iniciales. Conteo, asociación número-cantidad y sumas básicas.

\- Tipología de Artefacto: Juego manipulativo y simulador matemático visual.

\- Funcionalidad Principal (Qué hace el usuario): El niño planta semillas, añade flores y cuenta elementos para completar pequeños desafíos numéricos. Puede realizar sumas sencillas arrastrando flores de un grupo a otro.

\- Componente Visual / Animación SVG: Un jardín SVG que crece a medida que se resuelven los ejercicios. Las semillas germinan, aparecen tallos y florecen al completar correctamente cada actividad.

\- Ingeniería Frontend Sugerida: SVG inline, CSS animations, JavaScript, Drag \& Drop nativo y Web Audio API opcional.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": La mecánica se basa en operaciones aritméticas elementales y un conjunto reducido de ilustraciones SVG. No necesita ninguna biblioteca adicional.

14\. ¡A Vestir al Monstruo!

\- Área / Temática: Educación Infantil. Partes del cuerpo, colores, ropa y vocabulario.

\- Tipología de Artefacto: Juego de arrastrar y soltar con personaje personalizable.

\- Funcionalidad Principal (Qué hace el usuario): El niño recibe instrucciones como "ponle el sombrero rojo" o "busca los zapatos azules". Puede combinar prendas, colores y accesorios para crear personajes diferentes.

\- Componente Visual / Animación SVG: Monstruo SVG con extremidades, ojos y boca animados. Las prendas son elementos vectoriales independientes que se superponen al personaje y reaccionan con pequeños movimientos.

\- Ingeniería Frontend Sugerida: SVG inline, JavaScript, CSS transitions y Drag \& Drop nativo.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": Los elementos gráficos se pueden dibujar una sola vez y reutilizar. La lógica consiste en detectar dónde se suelta cada prenda y comprobar si coincide con la instrucción.

15\. Mi Día en Movimiento

\- Área / Temática: Educación Infantil y Primaria Inicial. Rutinas, autonomía personal y gestión del tiempo.

\- Tipología de Artefacto: Agenda visual interactiva y secuenciador de rutinas.

\- Funcionalidad Principal (Qué hace el usuario): El niño organiza las actividades de su día colocando pictogramas en orden: levantarse, desayunar, vestirse, ir al colegio, jugar y dormir. Puede marcar cada actividad como completada y visualizar su progreso.

\- Componente Visual / Animación SVG: Un personaje acompaña al niño durante el día y cambia de escenario según la actividad. Un sol recorre el cielo y se transforma en luna conforme avanza la secuencia.

\- Ingeniería Frontend Sugerida: SVG inline, CSS animations, JavaScript, LocalStorage para guardar las rutinas y Web Audio API para pequeñas señales sonoras.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": Funciona mediante tarjetas predefinidas y una secuencia ordenable. No necesita calendarios externos ni gestión de usuarios.



4\. Uso Personal y Productividad del Docente

16\. Mi Dinero Bajo Control

\- Área / Temática: Finanzas personales. Presupuesto doméstico, ahorro y control de gastos.

\- Tipología de Artefacto: Dashboard financiero local.

\- Funcionalidad Principal (Qué hace el usuario): El usuario introduce sus ingresos y gastos mensuales, los clasifica por categorías y establece objetivos de ahorro. La aplicación muestra cuánto dinero queda disponible y permite comparar distintos meses.

\- Componente Visual / Animación SVG: Gráficos vectoriales circulares y barras de progreso animadas. Una hucha SVG se llena progresivamente según el porcentaje del objetivo de ahorro conseguido.

\- Ingeniería Frontend Sugerida: HTML, CSS, JavaScript, SVG inline, LocalStorage y Chart.js opcional si se desea una representación gráfica más elaborada.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": Los cálculos son operaciones aritméticas sencillas y todos los datos se almacenan localmente. No requiere conexión bancaria ni acceso a información financiera externa.

17\. El Reloj de la Concentración

\- Área / Temática: Productividad personal. Técnica Pomodoro, concentración y gestión del tiempo.

\- Tipología de Artefacto: Temporizador visual animado.

\- Funcionalidad Principal (Qué hace el usuario): El usuario configura intervalos de concentración y descanso, inicia el temporizador y registra las sesiones completadas. Puede personalizar sus ciclos de trabajo y consultar cuántos minutos ha dedicado a cada actividad.

\- Componente Visual / Animación SVG: Un reloj circular SVG cuyo arco disminuye progresivamente. Un pequeño personaje cambia de postura durante el trabajo y celebra cuando llega el descanso.

\- Ingeniería Frontend Sugerida: JavaScript con setInterval, SVG inline, CSS animations, LocalStorage y Web Audio API para alarmas.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": Es uno de los mejores proyectos para empezar a programar. Solo necesita un contador de tiempo, algunas operaciones matemáticas y una representación circular SVG.

18\. Mi Casa en Equilibrio

\- Área / Temática: Organización doméstica. Tareas del hogar, mantenimiento y reparto de responsabilidades.

\- Tipología de Artefacto: Gestor visual de tareas y tablero doméstico.

\- Funcionalidad Principal (Qué hace el usuario): El usuario crea tareas domésticas, asigna responsables, establece periodicidades y marca actividades como completadas. Puede consultar las tareas pendientes y organizar las actividades de la semana.

\- Componente Visual / Animación SVG: Una casa SVG dividida en habitaciones. Cada estancia cambia de aspecto según las tareas realizadas: una cocina se limpia, una planta crece o una habitación recupera su orden.

\- Ingeniería Frontend Sugerida: HTML, CSS, JavaScript, SVG inline y LocalStorage para persistencia.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": Es un CRUD sencillo (crear, consultar, modificar y eliminar tareas). La información se gestiona con arrays y objetos JavaScript, sin necesidad de bases de datos.

19\. Mi Ruta Perfecta

\- Área / Temática: Ocio y viajes. Planificación de escapadas, itinerarios y presupuestos.

\- Tipología de Artefacto: Planificador visual de viajes.

\- Funcionalidad Principal (Qué hace el usuario): El usuario introduce destinos, actividades, horarios y presupuestos para organizar una escapada. Puede distribuir las visitas por días, modificar el orden de las paradas y consultar el coste estimado del viaje.

\- Componente Visual / Animación SVG: Un mapa esquemático SVG con una ruta que se dibuja progresivamente. Un pequeño vehículo animado recorre las paradas y cada destino dispone de una ilustración identificativa.

\- Ingeniería Frontend Sugerida: SVG inline, JavaScript, CSS animations y LocalStorage. Sin mapas comerciales ni APIs de geolocalización externas.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": Se puede utilizar un mapa ilustrativo ficticio o una representación esquemática. El itinerario es una lista ordenable de elementos y los presupuestos se calculan localmente.

20\. Mi Huerto Inteligente

\- Área / Temática: Hobbies y bienestar. Jardinería, horticultura y seguimiento de hábitos.

\- Tipología de Artefacto: Dashboard de seguimiento y simulador de crecimiento.

\- Funcionalidad Principal (Qué hace el usuario): El usuario registra las plantas de su huerto o jardín, anota los riegos, establece recordatorios y registra el crecimiento. Puede consultar un calendario de cuidados y visualizar la evolución de sus plantas.

\- Componente Visual / Animación SVG: Cada planta tiene una ilustración SVG que crece conforme se registran cuidados. Las hojas se despliegan, aparecen flores y los indicadores visuales muestran cuándo necesita agua o atención.

\- Ingeniería Frontend Sugerida: SVG inline, CSS keyframes, JavaScript, LocalStorage y notificaciones mediante Notification API opcional, sujetas a los permisos del navegador.

\- Por qué es un proyecto "Básico / Ideal para iniciarse": La aplicación utiliza registros sencillos de fechas y acciones. Las animaciones son cambios de escala y transformaciones CSS, sin necesidad de modelos botánicos complejos.



Consideraciones técnicas comunes para los 20 proyectos

Una de las mejores enseñanzas de este catálogo es que todos los proyectos pueden compartir una arquitectura muy sencilla.

Arquitectura de una micro-aplicación

index.html

Un único archivo autocontenido



HTML5

Estructura



CSS

Diseño y animación



JavaScript

Interactividad







LocalStorage

Persistencia de datos en el navegador



Aplicación funcional

Offline · Pendrive · Navegador · Moodle iframe\*

\*Con las restricciones habituales de permisos y almacenamiento que pueda imponer el navegador o Moodle.

Tecnologías recomendadas

Tecnología	Aplicación

HTML5	Estructura y controles

CSS3	Diseño, transiciones y keyframes

SVG inline	Ilustraciones y animaciones vectoriales

JavaScript ES6+	Lógica e interactividad

LocalStorage	Guardar datos localmente

Web Audio API	Sonidos generados en el navegador

Canvas	Dibujos y simulaciones

Chart.js	Gráficos, cuando resulte útil

Web Speech API	Síntesis de voz, si está disponible



Una recomendación importante para el curso: priorizar SVG, CSS y JavaScript nativos antes de introducir librerías externas. Así los docentes descubren que pueden crear animaciones, personajes, simulaciones y herramientas visualmente sofisticadas sin depender de servicios de terceros.



El objetivo pedagógico no debería ser enseñarles a programar desde cero, sino enseñarles a describir bien una necesidad, diseñar una interacción y conseguir que una IA convierta esa idea en una aplicación funcional.

