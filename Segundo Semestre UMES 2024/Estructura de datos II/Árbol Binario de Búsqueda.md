---
excalidraw-plugin: parsed
tags:
  - excalidraw
---
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

==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin settings under 'Saving'


# Excalidraw Data
## Text Elements
%%
## Drawing
```compressed-json
N4KAkARALgngDgUwgLgAQQQDwMYEMA2AlgCYBOuA7hADTgQBuCpAzoQPYB2KqATLZMzYBXUtiRoIACyhQ4zZAHoFAc0JRJQgEYA6bGwC2CgF7N6hbEcK4OCtptbErHALRY8RMpWdx8Q1TdIEfARcZgRmBShcZQUebQBWbQAGGjoghH0EDihmbgBtcDBQMBKIEm4IAFUAYWIofQBlAEkKADNcAE0AGXwAKQAVAH0OGAB1YnpUkshYRAqgojkkflLM

bmcAdgA2FcgYdZ4ADg3tABYATgBmDfjzgEZ4+J4Ny9PT3YgKEnVuN+0N86A44AnjnLbHeIfSQIQjKaTcHiJLZJFFJLZ3JKXeIPLaIj7WZTBbhJD7MKCkNgAawQ1TY+DYpAqAGI7ghWaypqVNLhsJTlBShBxiLT6YyJOTrMw4LhAtlOZBWoR8PgGrAiRJBB55RAyRTqaNvpIEaTyVSEKqYOr0Jryh8BXCOOFcmg7h82NLsGp9i6UR9+cI4E1iM7UH

kALofVrkTJB7gcITKj6EIVYCq4FJ24RCx3MEPFabQeDiXiFMAAX1JCAQxG4GMu4I2SVOSQ2H0YLHYXDQrdLDCYrE4ADlOGJa4dThsNqcjvEewXCMwACLpKDV7jtfBhD6aLPEACiwUy2RD8cTvaEcGIuFXNZdG2eda2942dx2vaIHEpcYT+A+9N5a5oBuYSFGW4ARnQuBwHAqrXsW+bQNCmQVEQcJQJyDCEAgFAAEI8nyApCiKDLMq0ZHkRh2AiLK

UBNKujSmtSxFiugLJsuxlHUVktH0XhvL+oKwp0iR4rkBwUoytxnGkDRdEZAAYkqKpqsWOp0rahQQFRMncXJDF6ggBp1EaaB8Jp2myfRqoGRaVpqVqKxaVx2R6QASsIDpOrWjkWbp9EAPIel6ta+uZzk8QpnBQPJuD6Eq3qoJCYU6S59HyVFDSEEYxY8CSyWWRk/RYFAACCqFdugwStOhPnhXpsGkKVMlsBQ0K4LeqCnr++V+Rke5CiVzWtSEHUQD

KFJULVKURfog0Tf0RYVIRNaOcw2AUsqAAavznElpRrRt+AdNwlznHE8Rooi6KYti8RvqURhsAY3D5pA9AEEIxZ3KBU0Ffo7mCTmIYQMtGH8iQmXZQieWlODxCqggcDcHtkBwwAsmwxAIP1uCaMEHXAQgjlw8xL29jhdKjaQyjcgAFDwdytrwjPUMzTNJAkACU2quQgygJjKS007g9OXCSvBi6zPCS6gHPxNzP09dk1lmoFUCdieP6OVGsUILzKak

MmyhkwWWS4/j3Dkp9HzYIslukNbvYcLr9uOwWwhQB+xZWwgiulHYABWCDYDkDTO3AGNYzjeOAaghOOTy6uMP0T34CbpSzKpYTBCHnbalRZIGAtcxoF1f5sABBMEFu76hKVufJ6n37KqB4AVnQirBHmYFlkAA
```
%%