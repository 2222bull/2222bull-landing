# Cómo activar el Píxel de Meta en tu landing

> Douglas, esto lo dejó Maicol en la rama `lab/maicol`. Es para que tu web
> empiece a **medir** y te deje hacer **remarketing**. La landing ya funciona
> sin esto — el píxel solo la hace más inteligente. Son 3 pasos, 10 minutos.

---

## ¿Qué es el Píxel y por qué te sirve?

El Píxel es un pedacito de código que le avisa a Meta (Facebook/Instagram) qué
pasa en tu web. Sin él, cuando alguien hace clic en tu anuncio y entra a la
landing, **Meta no se entera de nada**. Con él, ganás 3 cosas:

1. **Medir de verdad:** cuántos de los que ven el anuncio llegan a la web y
   cuántos completan el formulario. Hoy no lo sabés.
2. **Remarketing:** volver a mostrarle el anuncio a la gente que entró pero no
   te escribió (los "casi"). Son los más baratos de convertir.
3. **Optimizar hacia clientes:** decirle a Meta "buscame más gente parecida a
   la que completa el formulario", en vez de "más clics" a secas. Esto es lo
   que hace que mandar el anuncio a la **landing** rinda más que mandarlo
   directo al WhatsApp.

---

## Paso 1 — Sacar tu ID de Píxel

1. Entrá a **business.facebook.com** con tu cuenta.
2. Buscá en el menú **"Administrador de eventos"** (Events Manager).
3. Tocá **"Conectar orígenes de datos"** → elegí **"Web"** → **"Continuar"**.
4. Ponele de nombre `2222Bull` y creá el píxel.
5. Te va a mostrar un **número largo de unos 15 dígitos**. Ese es tu
   **ID de Píxel**. Copialo (o dejá esa pestaña abierta).

---

## Paso 2 — Pegar tu ID en la web

1. Abrí el archivo `index.html` de tu landing.
2. Buscá (Ctrl+F o Cmd+F) el texto **`TU_PIXEL_ID`**.
3. En la línea `const META_PIXEL_ID = "TU_PIXEL_ID";` reemplazá `TU_PIXEL_ID`
   por tu número. Debe quedar así (con TU número real, entre las comillas):
   ```js
   const META_PIXEL_ID = "123456789012345";
   ```
   Ese es el único lugar que importa. (Si hacés "reemplazar todo" también está
   bien — la página está armada para que no se rompa.)
4. Guardá el archivo y volvé a publicar (subir a GitHub / republicar como
   hiciste hoy). Listo, el píxel ya está midiendo.

> Si dejás el texto `TU_PIXEL_ID` sin cambiar, no pasa nada malo: el píxel
> queda apagado y la web funciona igual. Solo se prende cuando el valor son
> puros números (tu ID de verdad).

---

## Paso 3 — Verificar que funciona

1. En Chrome, instalá la extensión gratis **"Meta Pixel Helper"** (buscala en
   la Chrome Web Store, "Agregar a Chrome").
2. Entrá a tu landing publicada.
3. Tocá el ícono de la extensión (arriba a la derecha). Si está bien:
   - Se pone **azul** y dice tu píxel + **"PageView"**.
4. Completá el formulario de tu propia web (como si fueras un cliente) y fijate
   que aparezca **"Lead"** en la extensión. Ese es el evento que se dispara
   cada vez que alguien te deja sus datos.

---

## Después: apuntar el anuncio a la landing

Una vez que el píxel mide, en tu próxima campaña de Meta:

- Elegí el objetivo **"Clientes potenciales" / "Conversiones"** (no "Mensajes").
- Como evento a optimizar, elegí **"Lead"** (el que ya dispara tu formulario).
- Poné como destino la **URL de tu landing** (no el WhatsApp directo).

Así Meta te busca gente parecida a la que ya completó el formulario, y podés
hacer remarketing a los que entraron y no cerraron. Esa es la jugada de la
reunión: **anuncio → landing (que mide y filtra) → tu WhatsApp con el lead ya
calificado**, en vez de mandar todo crudo al WhatsApp.

---

*Cualquier duda técnica, escribila en el `BUZON.md` y la vemos.*
