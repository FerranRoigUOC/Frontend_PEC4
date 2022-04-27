1. ¿Cuáles son los style encapsulation de los componentes? Pon un ejemplo 
de uso de cada uno de ellos.

Són ViewEncapsulation.Emulated, valor per defecte, on Angular crea CSS per emular el comportament que proporcionen els DOMs d'ombra i les arrels de l'ombra, ViewEncapsulation.Native, valor ideal, on Angular utilitzarà arrels d'ombra, que sols funcionarà en navegadors i plataformes que ho suportin de forma nativa, i ViewEncapsulation.None, on angular utilitza CSS global, sense cap encapsulació.

2. ¿Qué es el shadow DOM?

Proporciona la possibilitat de tenir un estil (CSS) per a un component (per tal d'evita que els estils es filtrin i afectin la resta de l'aplicació) i també la capacitat d'aïllar i fer que el DOM sigui autònom.

3. ¿Qué es el changeDetection?

Per defecte, angular comprova en cada binding amb la interficie per veure si hi ha algun canvi i s'ha d'actualitzar algun element. També podem canviar el valor d'aquest changeDetection, per veure quan volem que angular actualitzi la interface d'usuari.

4. ¿Qué diferencias existen entre las estrategias Default y OnPush? ¿Cuándo 
debes usar una y otra? Ventajas e inconvenientes.

Default: en el comportament per defecte, quan Angular noti un esdeveniment (per exemple, una resposta del servidor o una interacció de l'usuari), passarà per cada component de l'arbre de components i comprovarà cadascuna de les bindings individualment per veure si algun dels valors ha canviat i s'ha d'actualitzar a la vista.

OnPush: en canvi en aquest comportament, Angular revisarà les bindings d'aquest component modificat en particular en funció de l'entrada a aquest component.

La ventatja d'utilitzar OnPush, es que no fa falta actualitzar tota la pàgina quan sols canvia un component, i per tant millora el rendiment.

5. Explica con detalle el ciclo de vida de los componentes. Haz hincapié en cuándo se 
disparan los hooks OnChanges, OnInit, AfterViewInit y OnDestroy, 
puesto que son los más utilizados.

- OnChanges: es crida just després del constructor i desprès cada vegada que canvïa les propietats d'entrada d'una directiva. Es cridat abans del mètode ngOnInit.
- OnInit: com hem dit, es crida desprès de OnChanges, aquest permet fer qualsevol inicialització única específica del vostre component o directiva. Per tal de tindre el codi organitzat, en aquest mètode s'utilitza per carregar les dades del servidor, encomptes del constructor
- AfterViewInit: es crida després que tots els components secundaris que s'utilitzen directament en el template del component s'acabin inicialitzant i les seves visualitzacions s'actualitzin amb els bindings. Solament es crida una vegada, durant la càrrega del component.
- OnDestroy: es crida quan un component està a punt de ser destruït i eliminat de la interfície d'usuari. És un bon lloc per fer tota la neteja, com donar-se de baixa de qualsevol listener que s'hagi inicialitzat i similars.