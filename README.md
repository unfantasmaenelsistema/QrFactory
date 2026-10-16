# QrFactory

**Generador de códigos QR con diseño**, de [Un Fantasma en el Sistema](https://www.unfantasmaenelsistema.com).

▶ **Abrir:** https://unfantasmaenelsistema.github.io/QrFactory/

Crea códigos QR de 15 tipos y personaliza su aspecto (formas, colores, degradados, ojos, logo, texto y marco) sin perder legibilidad. Todo se genera en tu navegador.

## Tipos de contenido

URL · Texto · vCard (tarjeta de contacto) · WiFi · Email · SMS · Teléfono · WhatsApp · Ubicación · Evento de calendario · Bitcoin · App Store / Google Play · YouTube · Instagram · Zoom

Cada tipo genera el formato estándar que entienden los móviles:

- **WiFi:** `WIFI:T:…;S:…;P:…;;`, con los caracteres especiales (`; , : " \`) escapados. Sin campo de contraseña en redes abiertas.
- **vCard 3.0:** nombre y apellidos por separado y texto escapado (comas, punto y coma, saltos de línea).
- **Evento:** iCalendar con `DTSTART`/`DTEND` en formato `AAAAMMDDTHHMMSS` y `DTSTAMP`, que las apps de calendario exigen.
- **Ubicación:** URI `geo:` con zoom y etiqueta opcionales, y validación de latitud y longitud.

El texto se codifica en **UTF-8**, así que la ñ, las tildes, el € o los emojis llegan bien al móvil.

## Diseño

- Seis formas de módulo, cuatro estilos de ojo, color sólido o cuatro degradados y diez combinaciones de color.
- Logo central (hasta el 30 % del código, con corrección de errores H), texto al pie y cuatro marcos.
- Los **patrones de posición y de alineación se dibujan siempre macizos**, aunque elijas puntos o barras, para que el lector los encuentre.
- Avisos si el código puede costar de leer: poco contraste, colores invertidos (claro sobre oscuro) o logo sin corrección alta.

Se ha comprobado con un lector independiente (jsQR) que se leen las 63 combinaciones probadas de forma, ojos, degradado, marco, nivel de corrección y logo hasta el 30 %.

## Exportación

- **PNG** (alta calidad), **JPG** (con fondo blanco), **WebP** y **SVG vectorial con el mismo diseño** que la vista previa (formas, degradado, ojos, logo, texto y marco).
- Copiar la imagen al portapapeles.
- Historial de los últimos 12 códigos: guarda el contenido, los campos y el estilo para restaurarlos tal cual (en tu navegador).

## Privacidad

Nada sale de tu equipo: el contenido, el logo y el historial se quedan en tu navegador.

## Estructura

```
index.html   la aplicación (HTML, CSS y JS; incluye la librería QR de Kazuhiko Arase, MIT)
icono.png    logo de la casa
```

Para probar en local: `python -m http.server` y abre `http://localhost:8000`.

## English

**QrFactory** creates styled QR codes of 15 types (URL, text, vCard, WiFi, email, SMS, phone, WhatsApp, location, calendar event, Bitcoin, app stores, YouTube, Instagram, Zoom) with standard, properly escaped payloads and UTF-8 text. Customise module shape, eyes, colours, gradients, centre logo, caption and frame; finder and alignment patterns are always drawn solid so codes stay scannable, and it warns about low contrast or inverted colours. Export to PNG, JPG, WebP or a vector SVG that matches the preview. Everything runs in your browser. Bilingual (ES/EN), light/dark themes.

## Licencia / License

[MIT](LICENSE) © Un Fantasma en el Sistema. La librería QR incluida es de Kazuhiko Arase (MIT).
