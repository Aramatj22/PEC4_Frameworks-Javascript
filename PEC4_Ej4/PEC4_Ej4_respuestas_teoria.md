**1. Explica qué son y cuándo se deberían utilizar las siguientes variables locales de la directiva estructural NgFor:**
**`index`** → Esta directiva sirve para trabajar con elementos de un array,  permite obtener la información de cada elemento dentro
del arreglo.
**`even`** → Muestra el valor booleano de true, cuando el índice del elemento es par.
**`odd`** → Muestra el valor booleano de true, cuando el índice del elemento es impar.
**`first`** → Determina cuál es el primer elemento en el array, puede ser de mucha utilidad al trabajar con tablas.
**`last`** → Determina cual es el último elemento en el array, puede tener la misma funcionalidad que first.
**2. ¿Para qué sirve la opción trackBy de la directiva estructural NgFor? Pon ejemplos de uso.**
Uno de los usos mas comunes es cuando se actualiza una propiedad en particular, evitar volver a cargar toda la información. Sí se usa el trackBy esto
solamente actualizará el cambio respectivo del elemento, omitiendo la información restante que no ha sido modificada. 
**3. ¿Es posible ejecutar dos directivas estructurales simultáneamente? Explica la razón tanto si es si posible como si no lo es.**
 A partir de Angular 2 no es posible aplicar dos directivas estructurales a un elemento huesped, debido a que cada una de estas (ngFor, ngIf) cumplen una condición independiente.