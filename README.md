

### Diapositiva 1: JavaScript desde Cero

Esta presentacion explica las bases de javascript para aprender desde cero en muy poco tiempo

---

### Diapositiva 2: Introducción a JavaScript
**Contenido:**
- **¿Qué es JavaScript?**
  - Lenguaje de programación interpretado
  - Usado para desarrollo web, tanto en el lado del cliente como del servidor
  - Interactivo y orientado a eventos

---

### Diapositiva 3: Historia de JavaScript
**Contenido:**
- Creado por Brendan Eich en 1995
- Originalmente llamado Mocha, luego LiveScript y finalmente JavaScript
- Estandarizado como ECMAScript

---

### Diapositiva 4: Tipos de Datos Primitivos
**Contenido:**
- **Number**: Enteros y flotantes
  ```javascript
  let edad = 30;
  let precio = 19.99;
  ```
- **String**: Texto
  ```javascript
  let saludo = "Hola, mundo!";
  let nombre = 'Mario';
  ```
- **Boolean**: `true` o `false`
  ```javascript
  let esMayorDeEdad = true;
  let tieneCuenta = false;
  ```
- **Undefined**: Variable no inicializada
  ```javascript
  let variableSinDefinir;
  ```
- **Null**: Ausencia intencional de valor
  ```javascript
  let valorNulo = null;
  ```
- **Symbol**: Identificador único
  ```javascript
  let simbolo = Symbol('descripcion');
  ```
- **BigInt**: Números enteros grandes
  ```javascript
  let granNumero = 1234567890123456789012345678901234567890n;
  ```

---

### Diapositiva 5: Tipos de Datos de Objeto
**Contenido:**
- **Object**: Colección de pares clave-valor
  ```javascript
  let persona = { nombre: 'Mario', edad: 30 };
  ```
- **Array**: Lista ordenada
  ```javascript
  let numeros = [1, 2, 3, 4, 5];
  ```
- **Function**: Objeto invocable
  ```javascript
  function saludar(nombre) {
    return `Hola, ${nombre}`;
  }
  ```
- **Date**: Fechas y horas
  ```javascript
  let hoy = new Date();
  ```
- **RegExp**: Expresiones regulares
  ```javascript
  let expresionRegular = /hola/i;
  ```
- **Map**: Colección de pares clave-valor
  ```javascript
  let mapa = new Map();
  mapa.set('nombre', 'Mario');
  ```
- **Set**: Colección de valores únicos
  ```javascript
  let conjunto = new Set([1, 2, 3, 4, 4]);
  ```

---

### Diapositiva 6: Conversión de Tipos
**Contenido:**
- **Implícita**: Coerción automática
  ```javascript
  let resultado = '5' + 5; // '55'
  ```
- **Explícita**: Conversión manual
  ```javascript
  let numero = Number('5'); // 5
  let texto = String(5); // '5'
  let booleano = Boolean(1); // true
  ```

---

### Diapositiva 7: Programación Orientada a Objetos
**Contenido:**
- **Clases y Objetos**
  ```javascript
  class Persona {
    constructor(nombre, edad) {
      this.nombre = nombre;
      this.edad = edad;
    }
    saludar() {
      return `Hola, soy ${this.nombre}`;
    }
  }

  const mario = new Persona('Mario', 30);
  console.log(mario.saludar());
  ```

---

### Diapositiva 8: Uso de Módulos
**Contenido:**
- **Exportar e Importar**
  ```javascript
  // math.js
  export const PI = 3.14159;
  export function suma(a, b) { return a + b; }

  // app.js
  import { PI, suma } from './math.js';
  console.log(PI); // 3.14159
  console.log(suma(2, 3)); // 5
  ```

---

### Diapositiva 9: Creación y Uso de Librerías
**Contenido:**
- **Configuración del Proyecto**
  ```sh
  mkdir mi-libreria
  cd mi-libreria
  npm init -y
  ```
- **Escribir el Código de la Librería**
  ```javascript
  // src/math.js
  export function suma(a, b) { return a + b; }
  export function resta(a, b) { return a - b; }
  ```
- **Publicar en npm**
  ```sh
  npm login
  npm publish
  ```

---

### Diapositiva 10: APIs Comunes en JavaScript
**Contenido:**
- **DOM API**
  ```javascript
  const header = document.querySelector('h1');
  header.textContent = 'Nuevo Título';
  ```
- **Fetch API**
  ```javascript
  fetch('https://api.example.com/data')
    .then(response => response.json())
    .then(data => console.log(data));
  ```
- **Local Storage**
  ```javascript
  localStorage.setItem('nombre', 'Mario');
  console.log(localStorage.getItem('nombre')); // Mario
  ```
- **Canvas API**
  ```javascript
  const canvas = document.getElementById('myCanvas');
  const ctx = canvas.getContext('2d');
  ctx.fillStyle = 'red';
  ctx.fillRect(20, 20, 150, 100);
  ```

---

### Diapositiva 11: Beneficios de Tipos Estáticos (TypeScript y Flow)
**Contenido:**
- **Detección Temprana de Errores**
- **Documentación Implícita**
- **Refactorización Segura**
- **Mejor Autocompletado**

**Ejemplo TypeScript:**
  ```typescript
  function suma(a: number, b: number): number {
    return a + b;
  }
  let resultado = suma(10, 20);
  console.log(resultado); // 30
  ```

**Ejemplo Flow:**
  ```javascript
  // @flow
  function suma(a: number, b: number): number {
    return a + b;
  }
  let resultado = suma(10, 20);
  console.log(resultado); // 30
  ```

---

### Diapositiva 12: Conclusiones y Recursos
**Contenido:**
- **Resumen**
  - JavaScript es versátil y esencial para el desarrollo web
  - Conocer tipos de datos, objetos y módulos es clave
  - Uso de herramientas como TypeScript mejora la calidad del código
- **Recursos Adicionales**
  - [MDN Web Docs](https://developer.mozilla.org/es/)
  - [TypeScript Documentation](https://www.typescriptlang.org/docs/)
  - [JavaScript.info](https://javascript.info/)

---

Aquí tienes las diapositivas adicionales sobre buenas y malas prácticas en JavaScript. Estas diapositivas te ayudarán a destacar las técnicas adecuadas y los errores comunes que se deben evitar para escribir código JavaScript más limpio, mantenible y eficiente.

---

### Diapositiva 13: Buenas Prácticas en JavaScript
**Contenido:**
- **Usar `const` y `let` en lugar de `var`**
  - `const`: para constantes y valores inmutables
  - `let`: para variables que pueden cambiar
  - **Ejemplo:**
    ```javascript
    const PI = 3.14159;
    let contador = 0;
    contador += 1;
    ```

---

### Diapositiva 14: Evitar `var`
**Contenido:**
- **`var` tiene alcance de función, no de bloque**
  - Puede causar errores difíciles de depurar
  - **Ejemplo Malo:**
    ```javascript
    if (true) {
      var nombre = 'Mario';
    }
    console.log(nombre); // 'Mario'
    ```
  - **Ejemplo Bueno:**
    ```javascript
    if (true) {
      let nombre = 'Mario';
    }
    console.log(nombre); // ReferenceError: nombre is not defined
    ```

---

### Diapositiva 15: Evitar el Uso de `eval()`
**Contenido:**
- **`eval()` puede ejecutar código arbitrario**
  - Riesgo de inyección de código y problemas de seguridad
  - **Ejemplo Malo:**
    ```javascript
    let codigo = "alert('Hola, mundo!')";
    eval(codigo);
    ```
  - **Alternativa Segura:**
    - Usa funciones más seguras y específicas para cada caso

---

### Diapositiva 16: Nombrado Claro y Descriptivo
**Contenido:**
- **Usar nombres significativos para variables y funciones**
  - Facilita la lectura y el mantenimiento del código
  - **Ejemplo Malo:**
    ```javascript
    let a = 10;
    let b = 20;
    function add(x, y) {
      return x + y;
    }
    ```
  - **Ejemplo Bueno:**
    ```javascript
    let width = 10;
    let height = 20;
    function calculateArea(width, height) {
      return width * height;
    }
    ```

---

### Diapositiva 17: Comentarios Útiles
**Contenido:**
- **Escribir comentarios que expliquen el "por qué"**
  - Evitar comentarios obvios
  - **Ejemplo Malo:**
    ```javascript
    let x = 10; // Define x as 10
    ```
  - **Ejemplo Bueno:**
    ```javascript
    // Calcula el área del rectángulo para la función principal
    let area = width * height;
    ```

---

### Diapositiva 18: Usar Funciones de Flecha
**Contenido:**
- **Funciones de flecha (`=>`) son más concisas**
  - Preservan el valor de `this`
  - **Ejemplo:**
    ```javascript
    const sumar = (a, b) => a + b;
    let resultado = sumar(2, 3); // 5
    ```

---

### Diapositiva 19: Evitar Anidamiento Profundo
**Contenido:**
- **Mantener el código plano y simple**
  - Refactorizar con funciones auxiliares
  - **Ejemplo Malo:**
    ```javascript
    if (a) {
      if (b) {
        if (c) {
          // Código...
        }
      }
    }
    ```
  - **Ejemplo Bueno:**
    ```javascript
    function checkConditions(a, b, c) {
      return a && b && c;
    }

    if (checkConditions(a, b, c)) {
      // Código...
    }
    ```

---

### Diapositiva 20: Manejo de Errores Adecuado
**Contenido:**
- **Usar `try...catch` para manejar errores**
  - Proporcionar mensajes de error claros
  - **Ejemplo:**
    ```javascript
    try {
      let resultado = potencialmenteFallo();
    } catch (error) {
      console.error('Ocurrió un error:', error.message);
    }
    ```

---

Claro, aquí tienes un conjunto de diapositivas sobre Node.js, que pueden complementar tu presentación sobre JavaScript desde cero.

---

### Diapositiva 24: Introducción a Node.js
**Contenido:**
- **¿Qué es Node.js?**
  - Entorno de ejecución para JavaScript en el lado del servidor
  - Basado en el motor V8 de Google Chrome
  - Asíncrono, orientado a eventos
  - Ideal para aplicaciones en tiempo real y servicios web

---

### Diapositiva 25: Historia de Node.js
**Contenido:**
- **Creación y Evolución**
  - Creado por Ryan Dahl en 2009
  - Originalmente enfocado en aplicaciones de red escalables
  - Gran adopción y apoyo de la comunidad de código abierto

---

### Diapositiva 26: Instalación de Node.js
**Contenido:**
- **Descargar e Instalar**
  - Página oficial: [nodejs.org](https://nodejs.org/)
  - **Instalación en Windows/Mac/Linux**
  ```sh
  # Usando nvm (Node Version Manager)
  nvm install node
  nvm use node
  ```

---

### Diapositiva 27: Primer Programa en Node.js
**Contenido:**
- **Hola Mundo**
  ```javascript
  // app.js
  const http = require('http');

  const server = http.createServer((req, res) => {
    res.statusCode = 200;
    res.setHeader('Content-Type', 'text/plain');
    res.end('Hola, Mundo!\n');
  });

  server.listen(3000, '127.0.0.1', () => {
    console.log('Servidor corriendo en http://127.0.0.1:3000/');
  });
  ```

  ```sh
  node app.js
  ```

---

### Diapositiva 28: Módulos en Node.js
**Contenido:**
- **Uso de Módulos**
  - CommonJS: `require` y `module.exports`
  - ES Modules: `import` y `export`
  - **Ejemplo:**
    ```javascript
    // modulo.js
    module.exports = function() {
      return 'Hola desde el módulo!';
    };

    // app.js
    const saludar = require('./modulo');
    console.log(saludar());
    ```

---

### Diapositiva 29: NPM (Node Package Manager)
**Contenido:**
- **Gestión de Paquetes**
  - Instalar paquetes: `npm install`
  - Archivo `package.json`
  - **Ejemplo:**
    ```sh
    npm init -y
    npm install express
    ```

  - **Uso de un paquete:**
    ```javascript
    const express = require('express');
    const app = express();

    app.get('/', (req, res) => {
      res.send('Hola, Mundo!');
    });

    app.listen(3000, () => {
      console.log('Servidor corriendo en http://localhost:3000/');
    });
    ```

---

### Diapositiva 30: Asincronía en Node.js
**Contenido:**
- **Callbacks**
  ```javascript
  const fs = require('fs');
  fs.readFile('archivo.txt', 'utf8', (err, data) => {
    if (err) throw err;
    console.log(data);
  });
  ```
- **Promises**
  ```javascript
  const fs = require('fs').promises;
  fs.readFile('archivo.txt', 'utf8')
    .then(data => console.log(data))
    .catch(err => console.error(err));
  ```
- **Async/Await**
  ```javascript
  async function leerArchivo() {
    try {
      const data = await fs.readFile('archivo.txt', 'utf8');
      console.log(data);
    } catch (err) {
      console.error(err);
    }
  }
  leerArchivo();
  ```

---

### Diapositiva 31: Frameworks y Librerías Populares
**Contenido:**
- **Express.js**
  - Framework minimalista para aplicaciones web
- **Koa.js**
  - Framework más moderno y ligero, desarrollado por los creadores de Express
- **Socket.io**
  - Biblioteca para aplicaciones en tiempo real
- **Mongoose**
  - Modelado de datos para MongoDB

---

### Diapositiva 32: Buenas Prácticas en Node.js
**Contenido:**
- **Manejo de Errores**
  - Siempre manejar errores asíncronos
  - **Ejemplo:**
    ```javascript
    app.use((err, req, res, next) => {
      console.error(err.stack);
      res.status(500).send('Algo salió mal!');
    });
    ```
- **Organización del Código**
  - Separar rutas, controladores y modelos
  - **Ejemplo:**
    ```sh
    ├── app.js
    ├── routes
    │   └── index.js
    ├── controllers
    │   └── mainController.js
    └── models
        └── userModel.js
    ```
- **Uso de Variables de Entorno**
  - Configuración sensible usando `dotenv`
    ```sh
    npm install dotenv
    ```
    ```javascript
    require('dotenv').config();
    const dbPassword = process.env.DB_PASSWORD;
    ```

---

### Diapositiva 33: Herramientas de Desarrollo
**Contenido:**
- **Nodemon**
  - Reinicia automáticamente el servidor cuando hay cambios
  - **Instalación:**
    ```sh
    npm install -g nodemon
    nodemon app.js
    ```
- **Debugger**
  - Utilizar herramientas de depuración como `node --inspect`
    ```sh
    node --inspect-brk app.js
    ```
  - Integración con editores como Visual Studio Code

---

### Diapositiva 34: Despliegue de Aplicaciones Node.js
**Contenido:**
- **Plataformas de Despliegue**
  - Heroku
  - Vercel
  - DigitalOcean
- **Preparación para Producción**
  - Variables de entorno
  - Manejo de sesiones
  - Seguridad: encabezados HTTP, CORS, etc.

---

### Diapositiva 35: Conclusión y Recursos Adicionales
**Contenido:**
- **Resumen**
  - Node.js es poderoso y versátil para aplicaciones del lado del servidor
  - Conocimiento de asincronía, módulos y manejo de paquetes es crucial
- **Recursos Adicionales**
  - [Node.js Documentation](https://nodejs.org/en/docs/)
  - [Express.js Guide](https://expressjs.com/)
  - [MDN Web Docs: Node.js](https://developer.mozilla.org/es/docs/Learn/Server-side/Node_server_without_framework)

---

Claro, aquí tienes un conjunto de diapositivas sobre herramientas de empaquetado, con un énfasis especial en Vite y por qué se considera mejor en muchos aspectos.

---

### Diapositiva 36: Introducción a las Herramientas de Empaquetado
**Contenido:**
- **¿Qué son las herramientas de empaquetado?**
  - Herramientas que transforman, optimizan y agrupan archivos de código fuente para ser ejecutados en el navegador
  - Ejemplos: Webpack, Rollup, Parcel, Vite

---

### Diapositiva 37: ¿Qué es Webpack?
**Contenido:**
- **Definición y Características**
  - Herramienta de construcción y empaquetado de módulos
  - Altamente configurable y extensible
  - Utiliza loaders y plugins para transformar archivos
- **Ejemplo de configuración básica:**
  ```javascript
  // webpack.config.js
  const path = require('path');

  module.exports = {
    entry: './src/index.js',
    output: {
      filename: 'bundle.js',
      path: path.resolve(__dirname, 'dist')
    },
    module: {
      rules: [
        {
          test: /\.js$/,
          exclude: /node_modules/,
          use: {
            loader: 'babel-loader'
          }
        }
      ]
    }
  };
  ```

---

### Diapositiva 38: Ventajas y Desventajas de Webpack
**Contenido:**
- **Ventajas:**
  - Gran ecosistema y comunidad
  - Flexibilidad y configurabilidad
- **Desventajas:**
  - Configuración compleja y verbosa
  - Tiempos de compilación lentos, especialmente en grandes proyectos

---

### Diapositiva 39: Introducción a Vite
**Contenido:**
- **¿Qué es Vite?**
  - Herramienta de desarrollo de frontend rápida y ligera
  - Creada por Evan You, el creador de Vue.js
  - Enfoque en velocidad y simplicidad
- **Características Clave:**
  - Servidor de desarrollo ultra-rápido con Hot Module Replacement (HMR)
  - Empaquetado de producción optimizado con Rollup

---

### Diapositiva 40: ¿Por qué Vite es Mejor?
**Contenido:**
- **Velocidad de Arranque**
  - Servidor de desarrollo inicia en milisegundos
- **HMR Instantáneo**
  - Actualizaciones instantáneas en el navegador sin recargar toda la página
- **Configuración Simplificada**
  - Configuración mínima comparada con Webpack
- **Soporte para Múltiples Frameworks**
  - Compatible con React, Vue, Svelte y más

---

### Diapositiva 41: Comparación de Rendimiento
**Contenido:**
- **Tiempo de Arranque:**
  - Webpack: Varios segundos a minutos
  - Vite: Milisegundos
- **Hot Module Replacement:**
  - Webpack: Lento, requiere recargas parciales
  - Vite: Instantáneo
- **Construcción de Producción:**
  - Webpack: Lenta, especialmente con configuraciones complejas
  - Vite: Rápida y optimizada con Rollup

---

### Diapositiva 42: Ejemplo de Proyecto con Vite
**Contenido:**
- **Instalación y Configuración**
  ```sh
  npm create vite@latest my-vite-project
  cd my-vite-project
  npm install
  npm run dev
  ```
- **Archivo de configuración:**
  ```javascript
  // vite.config.js
  import { defineConfig } from 'vite';

  export default defineConfig({
    plugins: [],
    server: {
      port: 3000
    }
  });
  ```

---

### Diapositiva 43: Buenas Prácticas con Vite
**Contenido:**
- **Organización del Proyecto**
  - Mantener una estructura de carpetas clara y modular
  - **Ejemplo:**
    ```sh
    ├── public
    ├── src
    │   ├── components
    │   ├── styles
    │   ├── assets
    │   └── main.js
    └── index.html
    ```
- **Uso de Plugins**
  - Añadir funcionalidades fácilmente
  - **Ejemplo:**
    ```sh
    npm install @vitejs/plugin-vue
    ```

---

### Diapositiva 44: Ecosistema de Plugins para Vite
**Contenido:**
- **Plugins Populares:**
  - `@vitejs/plugin-vue`: Soporte para Vue.js
  - `@vitejs/plugin-react`: Soporte para React
  - `vite-plugin-pwa`: Soporte para Progressive Web Apps (PWA)
- **Configuración de Plugins:**
  ```javascript
  // vite.config.js
  import { defineConfig } from 'vite';
  import vue from '@vitejs/plugin-vue';

  export default defineConfig({
    plugins: [vue()]
  });
  ```

---

### Diapositiva 45: Conclusión y Recursos Adicionales
**Contenido:**
- **Resumen**
  - Vite ofrece una experiencia de desarrollo más rápida y sencilla comparada con Webpack
  - Ideal para proyectos modernos que requieren rapidez en el desarrollo y la construcción
- **Recursos Adicionales**
  - [Vite Documentation](https://vitejs.dev/)
  - [Webpack Documentation](https://webpack.js.org/)
  - [Comparative Study of Build Tools](https://example.com/study)

---


### Diapositiva 46: Introducción a Astro
**Contenido:**
- **¿Qué es Astro?**
  - Framework moderno para construir sitios web rápidos y eficientes
  - Enfoque en rendimiento y simplicidad
  - Soporte para múltiples frameworks de frontend

---

### Diapositiva 47: Características Principales de Astro
**Contenido:**
- **Contenido Estático por Defecto**
  - Genera HTML estático para una mayor velocidad de carga
- **Island Architecture**
  - Componentes interactivos solo donde se necesitan
- **Soporte Multiframework**
  - Compatible con React, Vue, Svelte, y más

---

### Diapositiva 48: Instalación y Configuración de Astro
**Contenido:**
- **Instalación Básica**
  ```sh
  npm create astro@latest
  cd mi-proyecto-astro
  npm install
  npm run dev
  ```
- **Estructura de Archivos**
  ```sh
  ├── public
  ├── src
  │   ├── components
  │   ├── layouts
  │   ├── pages
  │   └── styles
  └── astro.config.mjs
  ```

---

### Diapositiva 49: Ejemplo de Proyecto con Astro
**Contenido:**
- **Creación de una Página Básica**
  ```jsx
  ---
// src/pages/index.astro
  ---
  <html>
    <head>
      <title>Mi Proyecto Astro</title>
    </head>
    <body>
      <h1>Hola, Mundo!</h1>
    </body>
  </html>
  ```
- **Añadir un Componente de React**
  ```jsx
  // src/components/MiComponente.jsx
  import React from 'react';

  export default function MiComponente() {
    return <h2>Hola desde React!</h2>;
  }

  // src/pages/index.astro
  ---
  import MiComponente from '../components/MiComponente.jsx';
  ---
  <html>
    <body>
      <h1>Hola, Mundo!</h1>
      <MiComponente />
    </body>
  </html>
  ```

---

### Diapositiva 50: Ventajas de Usar Astro
**Contenido:**
- **Rendimiento Superior**
  - Menos JavaScript en el cliente, carga más rápida
- **Flexibilidad de Framework**
  - Integración con múltiples frameworks de frontend
- **Optimización Automática**
  - Generación de HTML optimizado

---

### Diapositiva 51: Island Architecture
**Contenido:**
- **¿Qué es Island Architecture?**
  - Concepto donde solo partes interactivas (islands) tienen JavaScript
  - Mejora el rendimiento cargando solo lo necesario
- **Ejemplo de Uso:**
  ```jsx
  ---
// src/pages/index.astro
  ---
  <html>
    <body>
      <h1>Hola, Mundo!</h1>
      <div>
        <MiComponente client:load />
      </div>
    </body>
  </html>
  ```

---

### Diapositiva 52: Buenas Prácticas con Astro
**Contenido:**
- **Organización del Proyecto**
  - Mantener una estructura clara y modular
  - **Ejemplo:**
    ```sh
    ├── public
    ├── src
    │   ├── components
    │   ├── layouts
    │   ├── pages
    │   └── styles
    └── astro.config.mjs
    ```
- **Uso de Componentes**
  - Reutilizar componentes entre páginas
  - Minimizar el JavaScript en el cliente

---

### Diapositiva 53: Integración con CMS y APIs
**Contenido:**
- **Uso de CMS Headless**
  - Integración fácil con CMS como Contentful, Sanity, etc.
- **Consumo de APIs**
  - Obtener datos dinámicos y generar páginas estáticas
  - **Ejemplo:**
    ```jsx
    ---
// src/pages/blog/[slug].astro
    const { slug } = Astro.params;
    const post = await fetch(`https://mi-api.com/posts/${slug}`).then(res => res.json());
    ---
    <html>
      <body>
        <h1>{post.title}</h1>
        <p>{post.content}</p>
      </body>
    </html>
    ```

---

### Diapositiva 54: Despliegue de Aplicaciones Astro
**Contenido:**
- **Plataformas de Despliegue**
  - Netlify
  - Vercel
  - GitHub Pages
- **Preparación para Producción**
  - Generar sitio estático
    ```sh
    npm run build
    ```
  - Desplegar en la plataforma elegida

---

### Diapositiva 55: Comparativa Astro vs Otros Frameworks
**Contenido:**
- **Astro vs Next.js**
  - Astro: Mejor rendimiento por defecto, menos JavaScript
  - Next.js: Más características integradas como SSR y API Routes
- **Astro vs Gatsby**
  - Astro: Menos sobrecarga de JavaScript, más simple
  - Gatsby: Más plugins y ecosistema más grande

---

### Diapositiva 56: Recursos y Documentación
**Contenido:**
- **Documentación Oficial**
  - [Astro Documentation](https://docs.astro.build/)
- **Tutoriales y Guías**
  - [Astro Blog](https://astro.build/blog/)
  - [YouTube: Astro Tutorials](https://www.youtube.com/results?search_query=astro+tutorial)

---


### Diapositiva 57: Introducción a los Microservicios
**Contenido:**
- **¿Qué son los Microservicios?**
  - Arquitectura que descompone una aplicación monolítica en pequeños servicios independientes
  - Cada servicio es responsable de una funcionalidad específica
  - Comunicación entre servicios a través de API REST o mensajería

---

### Diapositiva 58: Ventajas de los Microservicios
**Contenido:**
- **Escalabilidad**
  - Escalar servicios independientemente
- **Despliegue Independiente**
  - Desplegar y actualizar servicios sin afectar al resto del sistema
- **Mejora del Desarrollo**
  - Equipos pueden trabajar en diferentes servicios de forma simultánea

---

### Diapositiva 59: Desventajas de los Microservicios
**Contenido:**
- **Complejidad**
  - Gestión y orquestación de múltiples servicios
- **Comunicación Interservicios**
  - Latencia y fallos potenciales en la comunicación
- **Consistencia de Datos**
  - Gestión de transacciones distribuidas

---

### Diapositiva 60: Creación de un Microservicio en Node.js
**Contenido:**
- **Configuración Inicial**
  ```sh
  mkdir user-service
  cd user-service
  npm init -y
  npm install express
  ```

- **Estructura de Archivos**
  ```sh
  ├── user-service
  │   ├── src
  │   │   ├── routes
  │   │   │   └── userRoutes.js
  │   │   ├── controllers
  │   │   │   └── userController.js
  │   │   └── app.js
  └── package.json
  ```

---

### Diapositiva 61: Implementación de un Microservicio
**Contenido:**
- **app.js**
  ```javascript
  const express = require('express');
  const userRoutes = require('./routes/userRoutes');

  const app = express();

  app.use(express.json());
  app.use('/users', userRoutes);

  const PORT = process.env.PORT || 3000;
  app.listen(PORT, () => {
    console.log(`User Service running on port ${PORT}`);
  });
  ```

- **userRoutes.js**
  ```javascript
  const express = require('express');
  const { getUsers, createUser } = require('../controllers/userController');

  const router = express.Router();

  router.get('/', getUsers);
  router.post('/', createUser);

  module.exports = router;
  ```

- **userController.js**
  ```javascript
  const getUsers = (req, res) => {
    res.send('Get all users');
  };

  const createUser = (req, res) => {
    res.send('Create a new user');
  };

  module.exports = { getUsers, createUser };
  ```

---

### Diapositiva 62: Comunicación entre Microservicios
**Contenido:**
- **API REST**
  - Servicios se comunican a través de endpoints HTTP
  - Ejemplo: `http://localhost:3000/users`
- **Mensajería**
  - Uso de colas de mensajes para comunicación asíncrona
  - Herramientas: RabbitMQ, Kafka

---

### Diapositiva 63: Gestión de Configuración
**Contenido:**
- **Variables de Entorno**
  - Configurar servicios mediante `.env`
  ```sh
  PORT=3000
  DB_URL=mongodb://localhost:27017/users
  ```

- **Ejemplo en Node.js**
  ```javascript
  require('dotenv').config();
  const port = process.env.PORT;
  ```

---

### Diapositiva 64: Autenticación y Autorización
**Contenido:**
- **JWT (JSON Web Tokens)**
  - Generar y verificar tokens de autenticación
  - Ejemplo:
  ```javascript
  const jwt = require('jsonwebtoken');

  const token = jwt.sign({ userId: 1 }, 'secret', { expiresIn: '1h' });
  ```

- **Middleware de Autenticación**
  ```javascript
  const auth = (req, res, next) => {
    const token = req.header('Authorization').replace('Bearer ', '');
    try {
      const decoded = jwt.verify(token, 'secret');
      req.user = decoded;
      next();
    } catch (e) {
      res.status(401).send('Please authenticate');
    }
  };
  ```

---

### Diapositiva 65: Buenas Prácticas en Microservicios
**Contenido:**
- **Desacoplamiento**
  - Mantener servicios independientes
- **Versionado de API**
  - Gestionar versiones de servicios sin afectar a consumidores existentes
- **Monitoreo y Logs**
  - Implementar herramientas para monitoreo (Prometheus, Grafana) y logging (Winston, Logstash)

---

### Diapositiva 66: Herramientas y Frameworks
**Contenido:**
- **Frameworks Populares**
  - Express.js
  - Koa.js
  - Nest.js
- **Herramientas de Orquestación**
  - Kubernetes
  - Docker Swarm

---

### Diapositiva 67: Ejemplo de Microservicio con Nest.js
**Contenido:**
- **Configuración Inicial**
  ```sh
  npm i -g @nestjs/cli
  nest new project
  ```

- **Implementación de Controlador**
  ```typescript
  import { Controller, Get, Post, Body } from '@nestjs/common';
  import { CreateUserDto } from './dto/create-user.dto';

  @Controller('users')
  export class UserController {
    @Get()
    getAllUsers() {
      return 'Get all users';
    }

    @Post()
    createUser(@Body() createUserDto: CreateUserDto) {
      return 'Create a new user';
    }
  }
  ```

---

### Diapositiva 68: Despliegue de Microservicios
**Contenido:**
- **Contenedores Docker**
  - Crear un `Dockerfile` para cada servicio
  - Ejemplo:
  ```dockerfile
  FROM node:14
  WORKDIR /app
  COPY package*.json ./
  RUN npm install
  COPY . .
  EXPOSE 3000
  CMD ["node", "src/app.js"]
  ```
- **Orquestación con Kubernetes**
  - Definir despliegues y servicios en archivos YAML
  ```yaml
  apiVersion: apps/v1
  kind: Deployment
  metadata:
    name: user-service
  spec:
    replicas: 2
    selector:
      matchLabels:
        app: user-service
    template:
      metadata:
        labels:
          app: user-service
      spec:
        containers:
        - name: user-service
          image: user-service:latest
          ports:
          - containerPort: 3000
  ```

---

### Diapositiva 69: Conclusión y Recursos Adicionales
**Contenido:**
- **Resumen**
  - Los microservicios permiten una arquitectura escalable y flexible
  - Node.js proporciona herramientas y frameworks poderosos para implementar microservicios
- **Recursos Adicionales**
  - [Microservices Architecture](https://microservices.io/)
  - [Node.js Documentation](https://nodejs.org/en/docs/)
  - [NestJS Documentation](https://docs.nestjs.com/)

---

