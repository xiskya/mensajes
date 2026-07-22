[README-mismo-mensaje-tres-versiones.md](https://github.com/user-attachments/files/30250416/README-mismo-mensaje-tres-versiones.md)
# El mismo mensaje, tres versiones

Herramienta interactiva para aprender a **comunicar una situación sensible adaptándola a personas distintas**, sin perder el fondo. Toma una misma noticia difícil —el cierre de una obra— y muestra cómo se reformula para tres perfiles de hermanas; el grupo lee las versiones y detecta qué cambió en cinco dimensiones.

Archivo: `mismo-mensaje-tres-versiones.html` · Herramienta web autónoma (un solo archivo, sin dependencias que instalar).

Dos ideas de fondo: **adaptar no es distorsionar** (el fondo no cambia, cambia la forma) y **adaptar es conocer a la persona, no suponer** por su edad o su cultura.

---

## Qué es

Un ejemplo trabajado, en tres pasos:

1. **El mensaje base.** Un correo genérico y frío sobre el cierre del colegio —el tipo de mensaje que no llega bien a nadie—, con una nota de por qué falla.
2. **Tres versiones.** Una pestaña por perfil. Cada una muestra la necesidad de esa hermana, el mensaje adaptado y su canal. Dentro, un desglose **¿qué cambió?** en cinco dimensiones (se abre una a una y revela qué cambió y por qué).
3. **La comparación.** Una tabla que cruza las cinco dimensiones con los tres perfiles, una checklist reutilizable y dos recordatorios.

## Los tres perfiles

Enfocados por **necesidad de comunicación**, no por cliché cultural:

1. **Hermana mayor, poco acceso digital** — presencia, calma y palabras sencillas.
2. **Hermana joven de otra cultura** — claridad literal, contexto que no da por supuesto y comprobar que ha entendido (que un cambio no es un castigo).
3. **Comunidad internacional, varias lenguas** — un mensaje simple, escrito, traducible y con espacio para preguntar.

## Las cinco dimensiones

Lo que se detecta que cambia de una versión a otra: **lenguaje, canal, ritmo, ejemplos y explicación**.

## Para quién

Formación en comunicación interna, comunidades y equipos. Funciona en dos modos:

- **En grupo:** proyectado. Antes de abrir cada dimensión, el grupo dice qué cree que cambió; luego se contrasta con la clave.
- **Individual:** cada persona explora las tres versiones a su ritmo.

## Cómo usarlo

- **Abrir en local:** doble clic en `mismo-mensaje-tres-versiones.html` → se abre en el navegador.
- **En una sesión:** publícalo en línea (ver más abajo) y comparte el enlace o un código QR. Los mensajes adaptados están escritos para poder leerse en voz alta tal cual.
- **Guardar el resultado:** el botón *Imprimir / Guardar PDF* despliega todo (versiones, claves y tabla) como guion del facilitador.

> URL publicada: _(pégala aquí cuando la subas a Netlify)_
> Al publicarla, genera su código QR con esa dirección.

## Cómo está pensada

- **Adaptar no es distorsionar:** la decisión y el porqué son idénticos en las tres versiones; solo cambia la forma. Así se desactiva el miedo a «suavizar la verdad».
- **Adaptar es conocer, no suponer:** los perfiles se definen por acceso, lengua y momento, no por nacionalidad. En el perfil 2 aparece a propósito el malentendido intercultural más típico: un cambio de destino leído como castigo.

## Personalizar

Casi todo el contenido vive en el bloque `<script>` del propio archivo:

- **Los tres perfiles:** objeto `PROFILES`. Cada uno tiene la necesidad (`need`), el mensaje adaptado (`message`), el canal (`channel`) y las cinco dimensiones (`dims`), cada una con qué cambió (`what`) y por qué (`why`).
- **Las dimensiones (etiquetas e iconos):** array `DIMS`.
- **La tabla comparativa:** objeto `MATRIX` (una frase corta por celda).
- **La checklist:** array `CHECKLIST`.

En el HTML (no en el script) se editan: el **mensaje base** y la descripción de la situación (`<div class="msg base">` y `.scenario`), y los **dos recordatorios** (`<div class="reminders">`).

**Colores y tipografía:** variables `:root` al principio del CSS (`--p1`, `--p2`, `--p3`, `--accent`, etc.).

Para cambiar de escenario (de un cierre de obra a otra situación sensible), basta con reescribir el mensaje base y los tres mensajes de `PROFILES`; la estructura no cambia.

## Publicar y compartir

Rápido y gratis con **Netlify Drop**: arrastra el archivo a `app.netlify.com/drop` y obtienes una URL al instante. También sirven GitHub Pages, Cloudflare Pages o tu propio WordPress. Con la URL, genera un **código QR** para proyectar en la sesión.

## Privacidad

La herramienta **no guarda ni envía nada**. Es un ejemplo trabajado que se lee y explora; no pide ni registra ninguna respuesta. No hay servidor, cuentas ni registro.

## Uso

Libre para formación. Adáptalo, tradúcelo o intégralo en tus materiales según lo necesites.
