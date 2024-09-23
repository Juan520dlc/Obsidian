## Árbol binario balanceado

Se le da prioridad al lado izquierdo

El primer elemento siempre está vacío

## Formulas

La fórmula para acceder a cada hijo, dado el índice padre(i), sería:

```jsx
hijo_izquierdo = 2i
hijo_derecho = 2i + 1
```

El acceso al padre se realizaría con una división entera:

```jsx
padre = i/2
```

## Pseudocódigo Max Heap

```jsx
// Atributos
entero[] monticulo
entero n

// Métodos
constructos(entero: capacidad) {
	monticulo = nuevo Arreglo(capacidad + 1)
	n = 0
}

funcion booleana estaVacia(){
	regresar n==0
}

funcion entera obtenerTamaño(){
	regresar n==0
}

procedimiento insertar(entero: valor) {
	si (n == monticulo.longitud() - 1)
		redimensionar(2 * monticulo.longitud())
	n++
	monticulo[n] = valor
	intercambiar(n)
}

procedimiento intercambiar(entero: i) {
	entero padre = i/2
	mientras(i > 1 && monticulo[padre] < monticulo[i]) {
		entero temp = monticulo[i]
		monticulo[i] = monticulo[padre]
		monticulo[padre] = temp
		i = i/2
	}
}
```

![[Montículo 2024-09-23 09.16.26.excalidraw]]