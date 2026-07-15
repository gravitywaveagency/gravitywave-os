# Gravity Wave OS

Sistema operativo interno de **Gravity Wave Agency** — un estudio boutique de crecimiento (Strategic Growth Studio) en Puerto Rico.

Aplicación web **local, de un solo archivo, 100% privada**. Se abre directamente `GravityWave_OS.html` en cualquier navegador. Sin servidor, sin build, sin backend.

## Cómo correrlo

- **Escritorio:** abre `GravityWave_OS.html` en el navegador.
- **iPad / iPhone:** guárdalo en Archivos y ábrelo con **Documents by Readdle** (Safari con `file://` no persiste bien el `localStorage`). Opcional: "Añadir a pantalla de inicio" para usarlo como app.

## Módulos

**Principal:** Dashboard · Clientes
**Observatorio (Gravity Research Lab):** Journal · Sistemas · Patrones · Hipótesis · Experimentos
**Gestión:** Finanzas · Growth System™ · Operaciones
**Estrategia:** Marketing · Análisis IA · Tendencias · Documentos

El Observatorio es un embudo de investigación vinculado al CRM: **observación → patrón → hipótesis → experimento**, y un sistema observado puede **promoverse a prospecto** en Clientes (entidades enlazadas vía `linkedClientId`, no la misma ficha).

## Convenciones (no cambiar sin instrucción explícita)

1. **Un solo archivo** — todo vive en `GravityWave_OS.html`.
2. **Sin dependencias externas** — solo Google Fonts (degradan solas). Las gráficas son **SVG nativo**, no Chart.js.
3. **Tamaño: guía blanda, ~250 KB.** No es un límite duro. El objetivo real es **no añadir dependencias pesadas**; al ser un archivo local sin dependencias, crecer con funciones legítimas está bien (carga al instante). El número solo es un recordatorio para no descuidarlo. (Actual: ~200 KB.)
4. **Tokens de marca (CSS variables)** — no modificar sin instrucción.
5. **Tipografía:** Syne (títulos) · Lora (cursivas) · DM Sans (cuerpo).
6. **UI y copy en español**, tono boutique profesional.
7. **Modelo de API:** `claude-sonnet-4-6`. Las llamadas al API de Claude desde el navegador **requieren** el header `anthropic-dangerous-direct-browser-access: true` (expone la API key en el cliente; aceptable solo para uso local/privado, **nunca** si se publica en web).
8. **Persistencia:** `localStorage` con prefijo `gw_` (estado principal en `gw_state`). Respaldo vía Exportar/Importar (incluye todo el `state`).

## Estado

Funcional. Todos los módulos activos. La IA (Análisis IA, Tendencias, borradores de email, análisis del Observatorio) requiere pegar tu API Key de Claude en el sidebar.
