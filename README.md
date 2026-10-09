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

## Código de referido
- Por defecto todo sale con el código **HAROLD-HM (Harold Marín)**.
- El código se agrega solo al final de **todos** los mensajes de WhatsApp que le llegan a Sonia (botón WhatsApp, calculadora y agenda), y se muestra en la portada, en la agenda y en el pie.
- El botón Compartir manda el enlace con el código: `https://haroldco45.github.io/montesion-campestre/?ref=HAROLD-HM`
- Si otra persona va a referir, se le da su propio enlace, por ejemplo `?ref=ANA-77`. El código queda guardado en el celular del cliente aunque vuelva a entrar sin el enlace.
- Para mostrar el nombre junto al código, agregarlo en `REF_NOMBRES` dentro de `index.html`.

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
