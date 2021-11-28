  **1. ¿Qué comando debes utilizar para crear un nuevo proyecto Angular utilizando Angular CLI denominado vinoteca? (A las preguntas que te haga Angular CLI puedes contestar utilizando las opciones por defecto). Explica brevemente la estructura y ficheros que ha generado Angular CLI:**
    
    El comando que debo usar para crear el nuevo proyecto **' vinoteca'** es:
    
    ```jsx
    ng new **vinoteca**
    cd **vinoteca**
    
    ```

**Explica brevemente la estructura y ficheros que ha generado Angular CLI:**

- **Ficheros de configuración en la raíz del proyecto:**
- **tsconfing.app.json** **➜** Configuración de TypeScript específica de la aplicación , incluidas las opciones del compilador de plantillas de TypeScript y Angular.
- **angular.json** **➜** Aquí  se encuentran los valores predeterminados de configuración de CLI para todos los proyectos en el espacio de trabajo, incluidas las opciones de configuración para compilar, servir y probar las herramientas que utiliza la CLI, como TSLint, Karma,etc.
- **package.json** **➜** Configura las dependencias del paquete npm que están disponibles para todos los proyectos en el espacio de trabajo.
- **.editorconfig** **➜** Este ****archivo tiene que ver con el trabajo en equipo que ayuda a tener una normativa y reglas claras en el equipo. Para que esta configuración funcione como se espera es necesario installar el pluggin 'editorConfig' en visual studio code
- **.gitignore ➜** Especifica archivos sin seguimiento intencional que Git debe ignorar.
- …
- **Directorio node_modules** **➜** Proporciona paquetes npm a todo el espacio de  trabajo. Las `node_modules`dependencias de todo el espacio de trabajo son visibles para todos los proyectos.
- **Directorio e2e** **➜** Contiene archivos de origen para un conjunto de pruebas de un extremo a otro que corresponden a la aplicación de nivel raíz, junto con archivos de configuración específicos de la prueba.
- **Directorio src:** **➜** Archivos de origen para el proyecto de aplicación de nivel raíz, soporte para probar y ejecutar su aplicación. Las subcarpetas contienen el origen de la aplicación y la configuración específica de la aplicación.
- **index.html ➜**  La página HTML principal que se muestra cuando alguien visita el sitio. La CLI agrega automáticamente todos los archivos JavaScript y CSS al crear la aplicación, por lo que normalmente no necesita agregar ninguna etiqueta `<script>`o `<link>`aquí manualmente.
- **main.ts** **➜** El principal punto de entrada para su aplicación. Compila la aplicación con el compilador JIT y arranca el módulo raíz de la aplicación (AppModule) para que se ejecute en el navegador.
- **styles.css** **➜**  Muestra una lista de archivos CSS que proporcionan estilos para un proyecto.
- **test.t**s **➜** El principal punto de entrada para las pruebas unitarias, con alguna configuración específica de Angular.
**- polyfills.ts** **➜**  Proporciona scripts de polyfill para compatibilidad con el navegador.
- **Directorio enviroments** **➜** Contiene opciones de configuración de compilación para entornos de destino particulares.
- **Directorio assets** **➜**  Contiene imágenes y otros archivos de activos que se copiarán tal cual cuando se compile la aplicación.
- **Directorio app** **➜** Carpeta que contiene la lógica y los datos del proyecto. Los componentes angulares, las plantillas y los estilos van aquí.
**- Ficheros app.component.*** **➜**  app.component.ts (Define la lógica del componente raíz), app.component.html (Define la plantilla HTML asociada a la raíz), app.component.css (Define la hoja de estilo CSS base para la raíz), app.component.spec.ts (Define una prueba unitaria para la raíz).
**- Fichero app.module.ts** **➜** Define el módulo raíz, llamado `AppModule`, que le dice a Angular cómo ensamblar la aplicación. Inicialmente declara solo el `AppComponent`. A medida que agrega más componentes a la aplicación, deben declararse aquí.

**2. Explica cada uno de los siguientes decoradores generados por Angular CLI, detallando cada una de las propiedades que se definen en:**

```jsx
app.module.ts - @NgModule (declarations, imports,
providers, bootstrap).
```

**declarations ➜** Se utiliza para importar o declarar componentes como vistas, directivas, pipes  que se van a usar en las plantillas HTML.

**imports ➜** Sirve para importar otros módulos que se van a usar.

**providers ➜** Sirve para importar servicios (modelos: las clases para obtener y manejar datos). Una vez importados son accesibles en cualquier parte de la app.

**bootstrap ➜** Es la vista o componente principal de la aplicación, llamado componente raíz.  Por default es  AppComponent.

```jsx
app.component.ts - @Component (selector, templateUrl,
styleUrls).
```

**selector ➜** Es una etiqueta de html o clase css que puede ser usada en el proyecto, con un nombre que identifique al componente.

**templateUrl ➜** Es una ruta a un archivo Html que se haya modificado para ser usado por el componente.

**styleUrls ➜** Es una ruta a un archivo que contiene hojas de estilos CSS para ser usados por el componente.

**3. ¿Es posible poder inyectar el template y los estilos en línea de un componente sin necesidad de especificarlos en templateUrl, styleUrls? ¿Es recomendable hacer esto?**

Si es posible, pero no es recomendable, sería mejor mantener las plantillas dentro de sus componentes donde se encuentren fácilmente. Además el código de la plantilla en línea se estaría volviendo grande y difícil de manejar, por lo que es mejor dividir el componente en varios componentes más pequeños, en el que cada uno cumpla su cometido.