# Webpack Template

Plantilla para iniciar proyectos de HTML, CSS y JavaScript con Webpack. Incluye configuraciones separadas para desarrollo y producción y soporte para módulos ES.

## Requisitos

- Node.js 22.15.0 o superior.
- npm.

## Instalación

Desde la carpeta del proyecto, instala las dependencias:

```bash
npm install
```

## Desarrollo

```bash
npm run dev
```

Inicia el servidor de desarrollo, abre el navegador y actualiza la página al guardar cambios.

Para detener el servidor, pulsa `Ctrl + C` en la terminal.

## Compilación para producción

```bash
npm run build
```

Genera los archivos de producción en `dist/`. El contenido anterior de esa carpeta se limpia en cada compilación. No edites los archivos generados: trabaja en `src/`.

> En PowerShell, si la política de ejecución bloquea `npm`, utiliza `npm.cmd`, por ejemplo: `npm.cmd run dev`.

## Estructura

```text
src/
  index.js           # Punto de entrada de JavaScript; importa los estilos
  styles.css         # Estilos de la página
  template.html      # Plantilla HTML
webpack.common.js    # Entrada, salida, plugins y reglas compartidas
webpack.dev.js       # Servidor y configuración de desarrollo
webpack.prod.js      # Configuración de producción
```

## Qué incluye

- Procesamiento de CSS mediante `css-loader` y `style-loader`.
- Generación del HTML mediante `html-webpack-plugin`, que añade el script generado automáticamente.
- Tratamiento de imágenes PNG, SVG, JPG, JPEG y GIF importadas desde JavaScript o referenciadas desde CSS.
- Combinación de las configuraciones mediante `webpack-merge`.

## Reutilizar la plantilla

1. Crea una copia de esta base para el nuevo proyecto.
2. Cambia el nombre y la descripción en `package.json` y ejecuta `npm install` para actualizar `package-lock.json`.
3. Personaliza el título y el contenido de `src/template.html`.
4. Desarrolla el proyecto en `src/` y adapta este README.

Conserva `package-lock.json` en el repositorio. Las carpetas `node_modules/` y `dist/` están excluidas mediante `.gitignore`.
