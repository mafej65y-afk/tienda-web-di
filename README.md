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