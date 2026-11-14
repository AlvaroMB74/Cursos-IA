# Instrucciones y Directrices del Proyecto: Curso IA (Docentes de Secundaria)

## 📌 Contexto General y Estructura en 3 Niveles
* **Objetivo:** Preparación, organización y actualización de materiales formativos para docentes de Educación Secundaria (Galicia).
* **Edición de Referencia:** Curso académico 2026–2027 (datos y estado del arte a noviembre de 2026).
* **Líneas de Formación (3 Niveles del Proyecto):**
  1. `01_Iniciacion_Docente`: Curso base de iniciación docente (fundamentos, historia, casos de éxito, marco ético/legal y 5 talleres prácticos actualizados).
  2. `02_Reforzo_MicroApps_Moodle`: Módulo intensivo de 3 horas sobre integración de micro-aplicaciones interactivas e incrustación en Moodle.
  3. `02_IA_Axentica`: Curso avanzado sobre el salto al paradigma agéntico, herramientas de escritorio/IDE (Claude Code, Antigravity, Cursor, Windsurf), MCP (Model Context Protocol), diseño de proyectos y gobernanza/normativa docente.
* **Idioma:** 
  * Diálogo, planificación, debates, commits y documentación técnica: **Castellano**.
  * Diapositivas, interfaces web interactivas (Reveal.js / React) y materiales para el profesorado/alumnado: **Gallego**.

---

## 🌐 Alojamiento, Git y Despliegue en GitHub Pages
* **Repositorio Git:** `https://github.com/AlvaroMB74/Cursos-IA.git` (rama `main`).
* **URLs Públicas de Acceso Independiente (GitHub Pages):**
  * **Nivel 1 (Iniciación):** `https://alvaromb74.github.io/Cursos-IA/2026-27/01_Iniciacion_Docente/`
  * **Nivel 2 (Refuerzo MicroApps):** `https://alvaromb74.github.io/Cursos-IA/2026-27/02_Reforzo_MicroApps_Moodle/`
  * **Nivel 3 (IA Axéntica):** `https://alvaromb74.github.io/Cursos-IA/2026-27/02_IA_Axentica/`
* **Reglas Críticas de Alojamiento Web (Servidor Linux):**
  * **Sensibilidad a Mayúsculas/Minúsculas:** Linux distingue `CSS` de `css` e `Img` de `img`. Todas las rutas relativas en `<link>`, `<script>`, `<img>`, `<iframe>` y fetch deben coincidir **exactamente** con la capitalización del disco.
  * **Rutas Relativas Estrictas:** Nunca utilizar rutas absolutas locales (`C:/...` o `/2026-27/...`); usar siempre rutas relativas (`./`, `../`, `../../`) para garantizar portabilidad en GitHub Pages.
  * **Sintaxis de texto e interfaces:** Nunca usar sintaxis matemática LaTeX cruda como `$\rightarrow$` en el HTML; utilizar caracteres Unicode estándar (`→`).
  * **Flujo de trabajo Git:** Tras implementar y verificar cualquier cambio significativo o corrección, realizar `git add`, `git commit` descriptivo y `git push origin main`.

---

## 🎨 Sistema de Diseño Visual Compartido (Dark 70s Retro-Tech)
Las tres presentaciones deben compartir de forma uniforme la misma identidad visual:
* **Fondo Base (`dark`):** `#121212` (negro carbón suave).
* **Superficie de Tarjetas (`card`):** `#1E1E1E` (gris neutro oscuro).
* **Tarjetas Elevadas (`card-elevated`):** `#282828`.
* **Texto Principal (`cream`):** `#EAE0C8` (crema / hueso cálido, alta legibilidad sobre fondos oscuros).
* **Texto Secundario (`dim`):** `#A8A090` (beige / cinza medio apagado).
* **Bordes (`border`):** `#333333` o `rgba(255, 255, 255, 0.1)`.
* **Acentos:**
  * Oro Viejo (`gold`): `#D4AF37`
  * Naranja Agente / Quemado (`orange`): `#f97316` / `#D35400`
  * Rojo Ladrillo / Alerta (`retro` / `rose`): `#C0392B` / `#f43f5e`
  * Cian Tecnológico (`cyan`): `#06B6D4`
  * Púrpura Normativo (`purple`): `#8B5CF6`
  * Esmeralda / Verde (`green` / `emerald`): `#10B981`
* **Regla Técnica Tailwind CDN:** En archivos HTML que utilicen Tailwind CSS vía CDN, los colores personalizados de `tailwind.config` deben definirse con sus códigos hexadecimales directos (no mediante `var(--...)`), para que el compilador de Tailwind pueda procesar correctamente las clases de opacidad (`bg-card/90`, `border-gold/30`, etc.).

---

## 🔄 Regla de Sincronización Inter-Conversaciones
> [!IMPORTANT]
> **Registro Central Obligatorio de Decisiones Globales:**
> Cualquier decisión técnica, de contenido, de paleta o de arquitectura que se tome en **cualquiera de las conversaciones de este proyecto** y que afecte a la estructura global, al diseño común o al despliegue, **debe ser trasladada y documentada inmediatamente en este archivo (`PROJECT_RULES.md`)**.
> 
> Al comenzar una nueva conversación o continuar una existente, el asistente debe leer `PROJECT_RULES.md` para operar siempre bajo el consenso global actualizado.

---

## 🔍 Regla Fundamental de Verificación y Estado del Arte
> [!IMPORTANT]
> **Obligatoriedad de Búsqueda Web en Fuentes Contrastadas:**
> Al tratarse de un proyecto que aborda el **estado actual (2026) y las proyecciones a futuro de la IA**, está estrictamente prohibido basarse en presunciones o extrapolaciones de memoria. 
> 
> **Siempre se debe utilizar la herramienta de búsqueda web** para verificar:
> 1. Versiones reales y vigentes de modelos (OpenAI, Anthropic, Google, DeepSeek, Alibaba, etc.).
> 2. Benchmarks actuales, precios, licencias y disponibilidad en el mercado.
> 3. Hitos científicos, casos de éxito recientes y avances regulatorios (UE, Amtega, etc.).
> 4. Novedades contrastadas antes de redactar o incorporar cualquier contenido a las aplicaciones o presentaciones.
