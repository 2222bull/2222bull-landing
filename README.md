# Landing page — 2222Bull Tattoo

> Página simple (un solo archivo `index.html`) con portfolio, cómo funciona,
> garantía y el formulario calificador con cupón de 10%. Pensada para
> mandarla por DM cuando alguien te escribe por el anuncio o el Instagram.

## Diseño (actualizado 2026-07-22)
- **Tipografía de títulos:** Anton (bold, condensada, onda portada de manga),
  cargada desde Google Fonts. Texto de párrafos: Rubik.
- **Tema claro/oscuro:** botón (🌙/☀️) arriba a la derecha, recuerda la
  elección en el navegador de cada visitante (`localStorage`). Los colores
  de cada tema están en `:root` y `:root[data-theme="light"]` en el
  `<style>` de `index.html` — para cambiar un color, tocar ahí.
- **Ojo con el hero:** la sección de arriba de todo tiene su propia foto de
  fondo oscura fija, así que sus colores de texto están fijados aparte
  (no cambian con el tema) para que siempre se lean bien.

## Lo que falta que hagas vos (Douglas)

### 1. Poner tus fotos y videos reales
Meté tus mejores fotos y videos en la carpeta `fotos/` (el nombre de la
carpeta quedó así por como arrancó el proyecto, pero adentro entran los dos
tipos de archivo), con estos nombres exactos:

```
fotos/hero.jpg      → la foto grande de fondo, arriba de todo
fotos/pieza-1.jpg   → foto
fotos/pieza-2.mp4   → video (ya viene armado para reproducirse solo, sin sonido)
fotos/pieza-3.jpg   → foto
fotos/pieza-4.jpg   → foto
fotos/pieza-5.mp4   → video
fotos/pieza-6.jpg   → foto
```

Los casilleros 2 y 5 ya están preparados para **video** (mp4) — se
reproducen solos en bucle, sin sonido, como en Instagram. Si preferís que
alguno de esos sea foto en vez de video (o al revés), avisale a tu Claude
y se lo cambia — es solo intercambiar la etiqueta en el HTML.

**Consejo:** tu reel de Sukuna x Itadori (el que tuvo casi 25.000 likes) es
un candidato perfecto para uno de los casilleros de video — ya demostró que
funciona.

Mientras no pongas los archivos, esos espacios se ven vacíos con el nombre
del archivo que falta — no rompe nada, es solo un aviso para vos.

### 2. Conectar el formulario a tu email (Formspree, gratis)
Así te llega un mail cada vez que alguien completa el formulario:

1. Andá a [formspree.io](https://formspree.io/) y creá una cuenta gratis
   con tu email (esto lo hacés vos, con tu cuenta — no la mía).
2. Creá un "New Form", ponele un nombre (ej. "2222bull leads").
3. Formspree te da una URL tipo `https://formspree.io/f/xxxxxxxx` — copiala.
4. Abrí `landing/index.html`, buscá la línea que dice:
   ```js
   const FORM_ENDPOINT = "";
   ```
   y pegá tu URL entre las comillas:
   ```js
   const FORM_ENDPOINT = "https://formspree.io/f/xxxxxxxx";
   ```
5. Guardá el archivo. Listo — cada envío te llega por mail.

**Mientras no hagas este paso**, el formulario igual muestra el cupón al
que lo completa (así no perdés esa parte), pero el dato no te llega a
ningún lado — solo queda en la pantalla de esa persona.

### 3. Publicar la página (GitHub Pages, gratis)
Con esto tu landing queda en una URL real que podés mandar por DM. Tu
Claude te puede guiar paso a paso para activarlo — pedile "activame
GitHub Pages para la landing" y te lleva.

## Cómo editar el texto
Todo el texto de la página está en `landing/index.html`. Es HTML plano —
buscá la frase que querés cambiar (ej. "Tu personaje favorito") y
reemplazala ahí mismo, entre las etiquetas.

## El cupón
Hoy el código es fijo: **ANIME10**. Si en algún momento querés que sea un
código distinto por persona (para controlar mejor cuántos se usan), avisale
a tu Claude — se puede sumar, pero es un paso más de complejidad que no
hace falta para arrancar.
