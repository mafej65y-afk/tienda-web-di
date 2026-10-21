   # El Botín de la Bastilla — Tienda de objetos de la Revolución

   Proyecto de Diseño de Interfaces.

   ## Integrantes

   - José Luis — @mafej65y-afk
   - Dani — @danieru0608

   ## Descripcion

El Botín de la Bastilla es una tienda ficticia de objetos "requisados" durante la Revolución francesa: coronas, pelucas, cartas coleccionables, un cuadro firmado por Messi… La web tiene cuatro páginas enlazadas entre sí:

| Página | Archivo | Contenido |
|---|---|---|
| Inicio | `index.html` | Hero, novedades, garantías y banner de ofertas |
| Catálogo | `catalogo.html` | 12 piezas mostradas con el componente tarjeta |
| Ficha de producto | `producto.html` | Cuadro firmado por Messi con selector de marco |
| Contacto | `contacto.html` | Formulario y datos de la tienda |

Todas comparten la misma cabecera, el mismo pie y la hoja `css/main.css`. El diseño es responsive con un punto de corte en 768px y usa una paleta oscura de verdes con acentos dorados.

## Cómo compilar el SCSS

Usamos la extensión **Live Sass Compiler** de VS Code.

1. Abrir la carpeta del repositorio en VS Code.
2. Crear el archivo `.vscode/settings.json` con esta configuración, para que compile solo `scss/main.scss` en `css/main.css`:

```json
   {
     "liveSassCompile.settings.formats": [
       { "format": "expanded", "extensionName": ".css", "savePath": "/css" }
     ],
     "liveSassCompile.settings.generateMap": false,
     "liveSassCompile.settings.autoprefix": false,
     "liveSassCompile.settings.includeItems": ["/scss/main.scss"]
   }
```

3. Pulsar **Watch Sass** en la barra inferior. Cada vez que se guarda un `.scss`, se regenera `css/main.css`.

El archivo `css/main.css` **sí se sube al repositorio**, así la web funciona al abrir `index.html` sin compilar nada.

## Estructura

    index.html
    catalogo.html
    producto.html
    contacto.html
    css/
    └── main.css
    img/
    scss/
    ├── main.scss              ← solo contiene @use
    ├── abstracts/
    │   ├── _variables.scss    ← colores, tipografías, espaciados, breakpoints y maps
    │   ├── _mixins.scss       ← hasta, desde, flex, rejilla, contenedor, foco
    │   └── _functions.scss    ← rem() con math.div
    ├── base/
    │   └── _reset.scss        ← reset, contenedor, secciones y formularios
    ├── components/
    │   ├── _card.scss         ← tarjeta, rejilla, ficha de producto y ventajas
    │   └── _button.scss       ← botones, banner y selector de marco
    └── layout/
        ├── _header.scss       ← cabecera, cabecera de página y hero
        └── _footer.scss
    .gitignore
    README.md

Qué usamos de SCSS:

- `@use` en todos los archivos (nada de `@import`), con espacios de nombres `v.`, `m.` y `f.`.
- Variables de colores, espaciados, tipografías y breakpoints, todas en `_variables.scss`.
- Anidación con `&` y nombres BEM: `.card__titulo`, `.card--destacada`, `.btn--primario`…
- 6 mixins con argumentos; `hasta()` y `desde()` usan `@content` para las media queries.
- Función `rem()` con `math.div()` en lugar de `/`.
- Dos maps recorridos con `@each`: variantes de botón y etiquetas de tarjeta.

## Reparto de tareas

| Tarea | José Luis | Dani |
|---|:---:|:---:|
| Repositorio, README inicial y `.gitignore` | ✔ | |
| Variables, función `rem()` y mixins | ✔ | |
| Reset, cabecera y pie | ✔ | |
| Componentes botón y tarjeta | ✔ | |
| Las 4 páginas HTML | ✔ | |
| Rediseño "El Botín de la Bastilla" | ✔ | |
| README completo | | ✔ |
| Ajustes responsive y de la ficha | | ✔ |
| Producto nuevo en el catálogo | | ✔ |
| Revisión de Pull Requests | ✔ | ✔ |

## Prefijos de los commits

Usamos `feat:`, `fix:`, `style:` y `docs:`. Algunos commits del principio usan `build:`, `chore:` o `refactor:`; a partir del rediseño solo usamos los cuatro prefijos del enunciado.

## Conflicto de fusión resuelto

_(Rellenar si aparece alguno.)_