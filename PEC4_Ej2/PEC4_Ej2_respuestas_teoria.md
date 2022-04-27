1. (0.75 puntos) ¿Qué comando debes utilizar para crear un nuevo proyecto Angular 
utilizando Angular CLI denominado vinoteca? 

ng new vinoteca

(A las preguntas que te haga Angular 
CLI puedes contestar utilizando las opciones por defecto). Explica brevemente la 
estructura y ficheros que ha generado Angular CLI:

- Ficheros de configuración en la raíz del proyecto: 

Con los siguientes archivos, tenemos la configuración del proyecto para poder compilar correctamente.
    - tsconfing.app.json
    - angular.json
    - package.json
    - .editorconfig,
    - .gitignore : los ficheros que se tienen que ignorar a la hora de hacer push con el git
- Directorio node_modules : es donde se guardan todas las dependencias del proyecto
- Directorio src: 
    - index.html : la vista html del proyecto
    - main.ts : la lògica con Typescript del proyecto
    - styles.css : los estilos que se le quieren dar a los elementos del proyecto
    - test.ts : donde iran los testos unitarios del proyecto
    - polyfills.ts
    - Directorio environments
    - Directorio assets
    - Directorio app : donde tenemos organizado el codigo del proyecto, con los componentes, sus modelos y sus templates
- Ficheros app.component.* : donde se generaran los nuevos componentes del proyecto
- Fichero app.module.ts : en el fichero de module, declaramos los componentes que se utilitzaran en el proyecto

2. (0.25 puntos) Explica cada uno de los siguientes decoradores generados por 
Angular CLI, detallando cada una de las propiedades que se definen en:

- app.module.ts - @NgModule (declarations, imports, providers, bootstrap).
declarations: declaramos los componentes que se utilizaran en el proyecto
imports: si queremos importar alguna dependencia de modulos para facilitar el trabajo
bootstrap: es donde definimos el componente raíz de nuestro modulo
- app.component.ts - @Component (selector, templateUrl, styleUrls). 
selector: es el nombre como utilizaremos el componente en un template.
templateUrl: la url de la interficie (html) del componente
styleUrls: las urls de los estilos que se le dan al componente (css)

3. (0.25 puntos) ¿Es posible poder inyectar el template y los estilos en línea de un 
componente sin necesidad de especificarlos en templateUrl, styleUrls? ¿Es 
recomendable hacer esto?

Si utilizando template en vez de templateUrl y definiendo los elementos HTML como atributo, y utilizando styles en vez de styleUrls,
definiendo los estilos como atributo de styles.

No hay ningun inconveniente a nivel de rendimiento en utilizar template y styles o templateUrl y styleUrls, pero a nivel de organización, es mejor tener los archivos separados.