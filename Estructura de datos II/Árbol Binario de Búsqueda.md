## ¿Cómo insertar un nuevo nodo?
```
procedimiento insertar(entero dato) //* = puntero
	Nodo* nuevoNodo = nuevo Nodo(dato) // Apuntando a una dirección de memoria
	Nodo* padre = NULO
	Nodo* actual = raiz
	// Setear nodo Padre
	mientras (actual != NULO)
		padre = actual
		si (nuevoNodo.dato < actual.dato)
			actual = actual.hijoIzquierdo
		si_no
			actual = actual.hijoDerecho
	nuevoNodo.padre = padre
	// Fin setear nodo padre
	// Inicio Seteo nodo hijo
	si (padre == NULO)
		raiz = nuevoNodo
	si_no_si (nuevoNodo.dato < padre.dato)
		padre.hijoIzquierdo = nuevoNodo
	si_no
		padre.hijoDerecho = nuevoNodo
	// Fin seteo nodo hijo
fin_procedimiento
```

BST = Árbol Binario de Búsqueda (No es balanceable por defecto)

