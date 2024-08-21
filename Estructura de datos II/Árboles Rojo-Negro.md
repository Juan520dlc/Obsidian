## Propiedades
 1. **Color del nodo:** Cada nodo es rojo o negro
2. **Propiedad de la raíz:** la raíz del árbol siempre es negra
3. **Propiedad rojo:** los nodos rojos no pueden tener hijos rojos (no pude haber dos nodos rojos consecutivos en ningún camino).
4. **Propiedad negro:** cada camino desde un nodo hasta sus nodos nulos descendientes (hojas) tiene la misma cantidad de nodos negros.
5. **Propiedad de la hoja:** todas las hojas (nodos NULL) son negras.

## Comparación con árboles AVL

Los árboles AVL están más balanceados en comparación con los árboles rojo-negro, pero pueden provocar más rotaciones durante la inserción y la eliminación.

Por lo tanto, si su aplicación implica **inserciones y eliminaciones frecuentes,** entonces se deben preferir los árboles rojo-negros.

Y si las inserciones y eliminaciones son menos frecuentes y la búsqueda es una operación más frecuente, entonces se debe preferir el árbol AVL sobre el árbol rojo-negro

### ¿Cómo se asegura el balance?

Ejemplo sencillo

Una cadena de 3 nodos no es posible en el árbol rojo-negro. Podemos probar cualquier combinación de colores y ver si todos ellos violan la propiedad del árbol rojo-negro

## Operaciones Principales

1. Buscar un elemento
2. Insertar un elemento
3. Eliminar un elemento

Las dos últimas operaciones conducen a un cambio en la estructura del árbol y, por lo tanto, su resultado puede ser un desequilibrio en el árbol.