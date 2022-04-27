1. (0.75 puntos) ¿Qué comando debes utilizar para crear un nuevo proyecto Angular 
utilizando Angular CLI denominado vinoteca? 

ng new vinoteca

(A las preguntas que te haga Angular 
CLI puedes contestar utilizando las opciones por defecto). Explica brevemente la 
estructura y ficheros que ha generado Angular CLI:

- Ficheros de configuración en la raíz del proyecto:
    - tsconfing.app.json : la configuración del proyecto para compilar
    - angular.json
    - package.json
    - .editorconfig,
    - .gitignore : los ficheros que se tienen que ignorar a la hora de hacer push con el git
- Directorio node_modules
- Directorio src: 
    - index.html : la vista html del proyecto
    - main.ts : la lògica con Typescript del proyecto
    - styles.css : los estilos que se le quieren dar a los elementos del proyecto
    - test.ts : donde iran los testos unitarios del proyecto
    - polyfills.ts
    - Directorio environments
    - Directorio assets
    - Directorio app
- Ficheros app.component.* : donde se generaran los nuevos componentes del proyecto
- Fichero app.module.ts

2. (0.25 puntos) Explica cada uno de los siguientes decoradores generados por 
Angular CLI, detallando cada una de las propiedades que se definen en:

- app.module.ts - @NgModule (declarations, imports, providers, bootstrap).
- app.component.ts - @Component (selector, templateUrl, styleUrls). 

3. (0.25 puntos) ¿Es posible poder inyectar el template y los estilos en línea de un 
componente sin necesidad de especificarlos en templateUrl, styleUrls? ¿Es 
recomendable hacer esto?