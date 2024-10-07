
# Proyecto de Predicción de Cáncer de Pulmón

Este proyecto tiene como objetivo desarrollar una aplicación para predecir la probabilidad de cáncer de pulmón en pacientes, utilizando Machine Learning. La aplicación está construida con el stack MEAN (MongoDB, Express, Angular y Node.js).

## Tecnologías Utilizadas
- **Angular**: Framework frontend para la construcción de la interfaz de usuario.
- **PrimeNG**: Biblioteca de componentes avanzada para Angular.
- **Tailwind CSS**: Framework de utilidades CSS para la personalización del diseño.

## Instrucciones para Configurar el Proyecto

### 1. Crear un Nuevo Proyecto Angular

Primero, crea un nuevo proyecto Angular ejecutando:

```bash
ng new cancer-prediction-app
```

Selecciona "Yes" para habilitar el routing y elige "CSS" como opción de estilos.

### 2. Instalar PrimeNG

Instala PrimeNG y PrimeIcons con los siguientes comandos:

```bash
npm install primeng primeicons
```

Luego, añade las siguientes líneas al archivo `angular.json` en la sección "styles":

```json
"styles": [
  "node_modules/primeng/resources/themes/saga-blue/theme.css",
  "node_modules/primeng/resources/primeng.min.css",
  "node_modules/primeicons/primeicons.css",
  "src/styles.css"
]
```

### 3. Instalar y Configurar Tailwind CSS

Instala Tailwind CSS y sus dependencias:

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init
```

Configura el archivo `tailwind.config.js` para que observe los archivos HTML y TypeScript de la carpeta `src`:

```js
module.exports = {
  content: [
    './src/**/*.{html,ts}',
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

En el archivo `src/styles.css`, agrega las directivas de Tailwind CSS:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### 4. Verificar la Configuración

Para verificar que PrimeNG y Tailwind CSS están funcionando correctamente, reemplaza el contenido del archivo `src/app/app.component.html` con el siguiente código:

```html
<div class="container mx-auto p-4">
  <h1 class="text-2xl font-bold text-blue-500">Probando PrimeNG con Tailwind CSS</h1>

  <!-- Botón de PrimeNG con clases de Tailwind CSS -->
  <p-button label="Enviar" class="mt-4 bg-green-500 hover:bg-green-700 text-white py-2 px-4 rounded"></p-button>

  <!-- Input de PrimeNG con Tailwind CSS aplicado -->
  <div class="mt-4">
    <label for="nombre" class="block text-sm font-medium text-gray-700">Nombre</label>
    <input type="text" pInputText class="mt-1 block w-full border-gray-300 rounded-md shadow-sm focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm" />
  </div>
</div>
```

### 5. Ejecutar el Proyecto

Finalmente, ejecuta el proyecto con:

```bash
ng serve
```

Accede a `http://localhost:4200/` en tu navegador para verificar que todo esté funcionando correctamente.

---

Este proyecto es parte del desarrollo de una aplicación que permita la predicción de cáncer de pulmón mediante el uso de Machine Learning.
