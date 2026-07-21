# Landing page — 2222Bull Tattoo

> Página simple (un solo archivo `index.html`) con portfolio, cómo funciona,
> garantía y el formulario calificador con cupón de 10%. Pensada para
> mandarla por DM cuando alguien te escribe por el anuncio o el Instagram.

## Lo que falta que hagas vos (Douglas)

### 1. Poner tus fotos reales
Meté tus mejores 6 fotos en la carpeta `landing/fotos/`, con estos nombres
exactos:

```
fotos/hero.jpg      → la foto grande de fondo, arriba de todo
fotos/pieza-1.jpg   → tu mejor trabajo
fotos/pieza-2.jpg
fotos/pieza-3.jpg
fotos/pieza-4.jpg
fotos/pieza-5.jpg
fotos/pieza-6.jpg
```

Mientras no las pongas, esos espacios se ven vacíos con el nombre del
archivo que falta — no rompe nada, es solo un aviso para vos.

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
