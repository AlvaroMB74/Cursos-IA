# Análise de partida: "Iniciación á IA Axéntica"

## Fonte revisada

Presentación de referencia: `Curso IA/2025-26/01_Iniciacion_Docente`.

É unha presentación reveal.js en galego, organizada como portal interactivo: portada e oito seccións cargadas como micrositios HTML embebidos.

## Contidos xa tratados

| Bloque | Contido e enfoque |
| --- | --- |
| Fundamentos | Definición de IA, diferenza entre programación determinista e IA baseada en datos/modelos, rede neuronal e “caixa negra”. Mitos: a IA non pensa como unha persoa nin é neutral. |
| Historia | Percorrido desde a lóxica clásica, Turing e Dartmouth ata deep learning, transformers, difusión, ChatGPT, RAG, multimodalidade e unha primeira mención aos axentes autónomos. |
| Casos reais | AlphaFold, descubrimento de fármacos e materiais, NASA/Kepler, robótica, papiros de Herculano, loxística, condución autónoma e apoio ao diagnóstico. |
| Uso docente e normativa | Protección de datos, anonimización, supervisión humana na avaliación, plataformas corporativas, transparencia, propiedade intelectual, sesgos e usos prohibidos. |
| Obradoiro LLM | Comparativa de asistentes e prompts para burocracia, deseño didáctico, rúbricas, adaptación NEAE e tarefas persoais. |
| Obradoiros multimodais | Xeración de imaxe, vídeo/voz e música, con exemplos de ferramentas e prompts educativos. |

## Coñecementos previos que se poden asumir

- Que é a IA xerativa e que son os modelos de linguaxe.
- Prompting estruturado: rol, contexto, tarefa, requisitos e formato.
- Xeración de texto, imaxe, voz, vídeo e música para fins docentes.
- Usos educativos: planificación, comunicación, situacións de aprendizaxe, rúbricas e adaptación de materiais.
- Limitacións: alucinacións, sesgos, privacidade, dereitos de autor e supervisión humana.
- Nocións introdutorias de RAG, multimodalidade, ferramentas externas e axentes autónomos.

## Fortalezas que convén conservar

- Lingua galega e exemplos próximos ao traballo docente.
- Navegación modular, interacción visual, tarxetas e misións prácticas.
- Prompts listos para adaptar e reutilizar.
- Ética, privacidade e protección de datos integradas en situacións reais de centro.
- Unha secuencia histórica que permite enlazar “chat → modelo con fontes → sistema que actúa”.

## Actualizacións necesarias

- Reducir a cronoloxía xeral e orientala a LLM, RAG, multimodalidade e sistemas axénticos.
- Diferenciar con claridade capacidades actuais, tendencias e hipóteses, evitando presentar predicións especulativas como feitos.
- Revisar ferramentas, prezos, plans gratuítos, límites e capacidades antes de incluílos.
- Verificar e actualizar todas as referencias legais e afirmacións sobre RGPD, Regulamento Europeo de IA, normativa galega e ferramentas corporativas.
- Matizar explicacións demasiado simplificadas sobre LLM e ferramentas baseadas en documentos.
- Engadir trazabilidade: fontes, decisións, permisos, revisión das accións e rexistro de incidencias.

## Huecos para o novo curso

A presentación anterior menciona os axentes, pero non explica como se deseñan nin como se controlan. O novo curso debe cubrir:

1. **Que distingue un axente dun chat:** obxectivo persistente, planificación, memoria, ferramentas, execución e avaliación.
2. **Arquitectura básica:** entrada → contexto/fontes → plan → ferramentas → resultado → verificación humana.
3. **Tipos de axentes:** asistente con instrucións, axente con documentos, axente con ferramentas, fluxos automatizados e sistemas multiaxente.
4. **Deseño de tarefas:** converter unha necesidade docente nun encargo acoutado, verificable e reversible.
5. **Ferramentas e permisos:** que pode consultar ou crear un axente, e que non pode enviar nin decidir sen aprobación.
6. **Memoria e contexto:** cando usar documentos, bases de coñecemento ou RAG; que datos nunca se deben incorporar.
7. **Avaliación práctica:** criterios de calidade, casos límite, detección de erros e rexistro de incidencias.
8. **Human-in-the-loop:** puntos obrigatorios de aprobación, especialmente en avaliación, comunicacións a familias, datos do alumnado e publicacións.
9. **Casos educativos seguros:** preparar secuencias a partir de documentos autorizados, auditar rúbricas, organizar recursos, xerar borradores e deseñar apoios sen datos identificativos.
10. **Proxecto final:** cada participante deseña e proba un axente acoutado, coa súa ficha de propósito, datos permitidos, ferramentas, límites e lista de validación.

## Fío pedagóxico recomendado

> Pasamos de pedir unha resposta a deseñar e supervisar un colaborador dixital que traballa sobre un proxecto.

Esta é a formulación central do curso. A interacción será en linguaxe natural, a través dunha plataforma conversacional con contexto de proxecto, e non mediante programación nin construción manual de fluxos.

### O que xa xestiona un LLM moderno

Como introdución, unha diapositiva mostrará que a experiencia conversacional oculta unha cadea de traballo: comprender o encargo, consultar o contexto e as fontes autorizadas, planificar, empregar ferramentas permitidas, producir resultados intermedios e pedir validación cando é necesaria. O alumnado non precisa construír todos eses compoñentes desde cero para aprender a dirixir e supervisar o proceso.

### Implicación didáctica

O obxectivo non é que o profesorado "constrúa un axente" tecnicamente. É que aprenda a:

1. Definir o obxectivo e o resultado esperado.
2. Delimitar a carpeta ou espazo de proxecto e as fontes permitidas.
3. Establecer o que o colaborador pode facer e o que debe consultar antes de actuar.
4. Pedir un plan previo á execución.
5. Revisar produtos intermedios, corrixir e acoutar.
6. Validar o resultado final e asumir a responsabilidade profesional.

O nivel debe seguir sendo de iniciación práctica para profesorado: sen programación obrigatoria, con experiencias reais de configuración, proba, supervisión e mellora dun colaborador dixital seguro.

## Decisións de implementación adoptadas

### Enfoque de experiencia

- O curso utilizará unha experiencia conversacional en linguaxe natural, similar ao uso de OpenClaw, DeepSeek Harness, Work, Cowork ou Antigravity, e non un construtor visual de fluxos como actividade principal.
- Dify poderá aparecer nunha diapositiva inicial unicamente como representación visual dos compoñentes que un LLM moderno xa coordina: contexto, planificación, ferramentas, regras, fontes e validación.
- Non se pretende que o profesorado constrúa a infraestrutura dun axente nin que programe. Aprenderá a dirixilo, acoutalo e supervisalo dentro dun espazo de proxecto.

### Entorno de aula previsto

- Preferencia por unha instancia conversacional centralizada e específica para o curso, accesible por navegador desde Linux ou Windows.
- Non usar a instancia persoal habitual sen separar contas, sesións, espazos de traballo e credenciais.
- Cada participante ou parella traballará nun espazo de proxecto illado, con fontes e entregables propios.
- As claves de modelos/API estarán só no servidor ou instancia xestionada; o alumnado non deberá velas nin manexalas.

### Límites iniciais do colaborador dixital

- Lectura limitada aos documentos autorizados do proxecto.
- Escritura limitada á carpeta de entregables do proxecto.
- Plan previo obrigatorio antes da execución.
- Aprobación humana antes de sobrescribir, borrar, enviar, publicar ou realizar unha acción externa.
- Sen datos reais do alumnado; emprego de datos sintéticos ou anonimizados.
- Sen terminal, correo, mensaxería, plugins de terceiros nin navegación web libre na primeira edición.

### Estratexia de práctica

- A práctica central será un único proxecto por persoa ou parella, non unha sucesión de exercicios descontextualizados.
- Cada proxecto combinará: finalidade, fontes, accións autorizadas e revisión humana.
- O entregable incluirá tanto o produto final como a ficha de deseño do colaborador: obxectivo, fontes, permisos, límites, validación e riscos.
- O catálogo de posibilidades para escoller proxectos queda recollido no documento `CATALOGO_PROXECTOS_PRACTICOS.md`.
