# Observatorio de IA Aplicada

Observatorio que se actualiza solo y registra **cómo se aplica la IA** en personas, equipos, organizaciones y gobiernos, en siete industrias núcleo (finanzas, pharma, bio, salud, agro, robótica, productividad) más las emergentes. Incluye un capítulo propio sobre **Claude Code, Kimi y DeepSeek**.

Se consume como un artefacto de Claude, pensado primero para iPhone e iPad y que también funciona en laptop. Tres tareas programadas de Claude lo alimentan:

| Cadencia | Qué hace |
|---|---|
| Diaria | Recolecta, verifica y clasifica de 8 a 15 hallazgos nuevos. Cada día profundiza en una industria distinta. |
| Semanal (lunes) | Escribe la síntesis de la semana (5 titulares, tendencias, señales débiles) y actualiza las fichas de herramientas. |
| Quincenal (días 1 y 16) | Mide las fuentes, agrega fuentes nuevas para cubrir vacíos, pausa las que no rinden y propone ajustes a la taxonomía. |

## Contenido del repositorio

| Ruta | Qué es |
|---|---|
| [`docs/concepto.md`](docs/concepto.md) | La idea completa: unidad de observación, taxonomía, experiencia, ritmo, arquitectura y modelo de datos. |
| [`observatorio/index.html`](observatorio/index.html) | La página del artefacto: cinco vistas (Hoy, Explorar, Mapa, Herramientas, Síntesis) que leen la base del artefacto en vivo. |
| [`datos/taxonomia.json`](datos/taxonomia.json) | Dimensiones, valores, fronteras entre industrias, fórmula de relevancia y esquema de un hallazgo. |
| [`datos/fuentes-semilla.json`](datos/fuentes-semilla.json) | Registro inicial de fuentes: frontier labs, academia, multilaterales, gobierno, industria, medios, analistas, comunidades y redes. |
| [`datos/semilla/`](datos/semilla) | Primera carga de la base: hallazgos iniciales y fichas de herramientas. |
| [`agentes/`](agentes) | Instrucciones de las tres tareas programadas. Son la fuente de verdad de cada prompt: si cambias un archivo, actualiza también la tarea programada. |

## Dónde verlo

Artefacto (privado): https://claude.ai/artifact/8kCUbAftYHDqHWoTCFY9V9

## Cómo se publica la página

La página se publica como artefacto con la capacidad `db` (y `user`). Los datos no viven en el HTML: los agentes los escriben en la base del artefacto con `ArtifactData`, así que el contenido se actualiza sin volver a publicar la página. Para cambiar el diseño se edita `observatorio/index.html` y se publica de nuevo en la misma URL.
