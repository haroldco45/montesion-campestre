# MonteSion Campestre · 7% en tu lote

App (PWA) estilo Toyota para que **Sonia Polo** venda lotes campestres de MonteSion Campestre durante la promoción del **7% de descuento (8 de octubre – 8 de noviembre de 2026)**.

**URL:** https://haroldco45.github.io/montesion-campestre/

## Qué trae
- Portada con el 7% y **contador regresivo** hasta el 8 de noviembre de 2026, 11:59 p.m. hora Colombia (UTC-5). Al vencer, la app avisa sola que la promo terminó.
- Pieza oficial de la promoción, con botones para **descargarla y compartirla**.
- **Calculadora de ahorro**: el cliente escribe el valor del lote y ve cuánto se ahorra; el resultado se envía a Sonia por WhatsApp.
- Horarios con indicador **"Abierto / Cerrado ahora"** en hora Colombia.
- Ubicación: Vía Lorica – Purísima, a 3 minutos de Lorica, con botón a Google Maps.
- **Agenda de visitas**: solo deja escoger horas dentro del horario de atención y arma el mensaje de WhatsApp para Sonia.
- Aviso de Habeas Data (Ley 1581 de 2012). La app no guarda datos personales.
- Barra fija con WhatsApp, Agendar y Compartir. Instalable como app (manifest + service worker).

## Antes de publicar
En `index.html`, sección CONFIGURACIÓN, poner el WhatsApp de Sonia:

```js
const WHATSAPP = "573002657818"; // Sonia Polo
```

Si se deja vacío, WhatsApp abre para escoger el contacto manualmente.

## Archivos
| Archivo | Para qué |
|---|---|
| index.html | La app |
| promo.jpg | Pieza de la promoción |
| og-image.jpg | Vista previa al compartir (1200×630, menos de 300 KB para WhatsApp) |
| icon-192.png, icon-512.png | Íconos de la app |
| manifest.json, sw.js | PWA |

## Publicar
1. Crear el repo `haroldco45/montesion-campestre` y subir todos los archivos.
2. Settings → Pages → Branch `main` / root.
3. Netlify se actualiza solo desde el repo.

---
Desarrollada por **Vibras Positivas HM** — Derechos de Autor Reservados
