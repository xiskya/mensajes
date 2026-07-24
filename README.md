[README-mismo-mensaje-tres-versiones.md](https://github.com/user-attachments/files/30332650/README-mismo-mensaje-tres-versiones.md)
# El mismo mensaje, tres versiones

Herramienta interactiva para aprender a **comunicar una situación sensible adaptándola a personas distintas**, sin perder el fondo. Toma una misma noticia difícil —el cierre de una obra— y muestra cómo se reformula para tres perfiles de hermanas: primero se adivina a quién va dirigida cada versión, luego se analiza qué cambió, y por último **se practica escribiendo una propia**.

Archivo: `mismo-mensaje-tres-versiones.html` · Herramienta web autónoma (un solo archivo, sin dependencias que instalar).

Dos ideas de fondo: **adaptar no es distorsionar** (el fondo no cambia, cambia la forma) y **adaptar es conocer a la persona, no suponer** por su edad o su cultura.

---

## Qué es

Cinco secciones:

1. **El mensaje base.** Un correo genérico y frío sobre el cierre del colegio —el tipo de mensaje que no llega bien a nadie—, con una nota de por qué falla.
2. **¿Para quién es cada una?** Las tres versiones adaptadas aparecen como A, B y C, **sin decir a quién van dirigidas y desordenadas**. Se asigna un perfil a cada una y, al comprobar, se revela el acierto, el canal y **la pista que estaba en el texto**.
3. **¿Qué cambió en cada una?** Una pestaña por perfil, con el mensaje, su canal y un desglose en cinco dimensiones que se abre una a una (qué cambió y por qué).
4. **La comparación.** Una tabla que cruza las cinco dimensiones con los tres perfiles, más una checklist reutilizable.
5. **Ahora te toca.** Un escenario nuevo —una hermana muy querida se marcha de forma inesperada— para **escribir el mensaje propio** dirigido al perfil que se elija, con las cinco dimensiones como guía. Después se puede ver una **versión modelo** para comparar (no como respuesta correcta).

## Los tres perfiles

Enfocados por **necesidad de comunicación**, no por cliché cultural:

1. **Hermana mayor, poco acceso digital** — presencia, calma y palabras sencillas.
2. **Hermana joven de otra cultura** — claridad literal, contexto que no da por supuesto y comprobar que ha entendido (que un cambio no es un castigo).
3. **Comunidad internacional, varias lenguas** — un mensaje simple, escrito, traducible y con espacio para preguntar.

## Las cinco dimensiones

Lo que se detecta que cambia de una versión a otra: **lenguaje, canal, ritmo, ejemplos y explicación**.

## Para quién

Formación en comunicación interna, comunidades y equipos. Funciona en dos modos:

- **En grupo:** proyectado. En la sección 2, que voten a mano alzada antes de comprobar; en la 3, que digan qué creen que cambió antes de abrir cada dimensión; en la 5, escritura individual y puesta en común.
- **Individual:** cada persona recorre las cinco secciones a su ritmo.

## Cómo usarlo

- **Abrir en local:** doble clic en `mismo-mensaje-tres-versiones.html` → se abre en el navegador.
- **En una sesión:** publícalo en línea (ver más abajo) y comparte el enlace o un código QR. Los mensajes están escritos para poder leerse en voz alta tal cual.
- **Si vas justa de tiempo:** las secciones 1 y 2 ya son un ejercicio completo y muy vivo. La 5 puede quedar para otro momento.
- **Avisa antes de la sección 5:** lo que escriban no se guarda; si quieren conservarlo, que usen *Imprimir / Guardar PDF* antes de cerrar.

> **URL publicada:** `https://xiskya.github.io/mensajes/`
> Publicada en GitHub Pages. Si algún día cambias esa dirección, habrá que regenerar su QR.

## Cómo está pensada

- **Adaptar no es distorsionar:** la decisión y el porqué son idénticos en las tres versiones; solo cambia la forma. Así se desactiva el miedo a «suavizar la verdad».
- **Adaptar es conocer, no suponer:** los perfiles se definen por acceso, lengua y momento, no por nacionalidad. En el perfil 2 aparece a propósito el malentendido intercultural más típico: un cambio de destino leído como castigo.
- **Reconocer no basta:** por eso la sección 5. Adaptar se consolida escribiendo, no solo leyendo.

## Personalizar

Casi todo el contenido vive en el bloque `<script>` del propio archivo:

- **Los tres perfiles:** objeto `PROFILES`. Cada uno tiene la necesidad (`need`), el mensaje adaptado (`message`), el canal (`channel`), la **pista** que se revela en la sección 2 (`clue`) y las cinco dimensiones (`dims`), cada una con qué cambió (`what`) y por qué (`why`).
- **El orden en que aparecen A, B y C:** array `ANON_ORDER` (por defecto `["p3","p1","p2"]`, para que no coincida con el orden de los perfiles).
- **Las versiones modelo de la práctica:** objeto `PRACTICE`, una por perfil.
- **Las dimensiones (etiquetas e iconos):** array `DIMS`.
- **La tabla comparativa:** objeto `MATRIX` (una frase corta por celda).
- **La checklist:** array `CHECKLIST`.

En el HTML (no en el script) se editan: el **mensaje base** y su situación (`<div class="msg base">` y `.scenario`), el **escenario de la práctica** (sección 5) con su guía de dimensiones, y los **dos recordatorios** (`<div class="reminders">`).

**Colores y tipografía:** variables `:root` al principio del CSS (`--p1`, `--p2`, `--p3`, `--accent`, etc.).

Para cambiar de escenario, reescribe el mensaje base y los tres mensajes de `PROFILES` (y, si quieres, el escenario de práctica y `PRACTICE`); la estructura no cambia.

## Publicar y compartir

Rápido y gratis con **Netlify Drop**: arrastra el archivo a `app.netlify.com/drop` y obtienes una URL al instante. También sirven GitHub Pages, Cloudflare Pages o tu propio WordPress. Con la URL, genera un **código QR** para proyectar en la sesión.

## Privacidad

La herramienta **no guarda ni envía nada**. En la sección 5 se escribe un mensaje, pero se queda en el navegador de cada persona: no se registra en ningún sitio y desaparece al recargar o cerrar la página. Lo que se quiera conservar, se guarda antes con *Imprimir / Guardar PDF*. No hay servidor, cuentas ni registro.

## Uso

Libre para formación. Adáptalo, tradúcelo o intégralo en tus materiales según lo necesites.
