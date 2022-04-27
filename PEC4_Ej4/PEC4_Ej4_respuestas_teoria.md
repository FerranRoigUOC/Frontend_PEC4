1. Explica qué son y cuándo se deberían utilizar las siguientes variables locales de la 
directiva estructural NgFor:

- index : obté l'índex de l'element actual d'un array que estem recorrent
- even: retorna true si l'índex de l'ojbecte actual és parell, en cas contrari retorna fals
- odd: retorna true si l'índex de l'ojbecte actual és impar, en cas contrari retorna fals
- first: retorna true si l'objecte actual és el primer objecte, en cas contrari retorna fals
- last: retorna true si l'objecte actual és l'últim objecte, en cas contrari retorna fals

2. ¿Para qué sirve la opción trackBy de la directiva estructural NgFor? Pon ejemplos 
de uso.

L'opció trackBy pren una funció que té dos arguments: un índex i l'element. Si la funció trackBy es proporciona a la directiva NgFor, utilitzarà el valor de retorn de la funció per decidir com identificar elements individuals.

Per exemple, si volem traquejar l'array segons les ids dels elements.

3. ¿Es posible ejecutar dos directivas estructurales simultáneamente? Explica la razón 
tanto si es si posible como si no lo es.

No, no és possible executar dos directives estructurals simultàniament, perquè no se sap quina de les dos s'ha de executar primer.