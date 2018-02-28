1)
Pre-procesador: Se declaran las funciones y los macros que estan en los directorios incluidos.
Compilacion I: En tres etapas, realiza un analisis sintanctico, semantico y lexico generando una representacion intermedia que la optimiza y genera un nuevo codigo assembler.
Compilacion II: "Traduce" el codigo assembler en lenguaje binario.
Linkeo: Une todas las funciones y macros involucradas en el programa. Existen dos tipos: estatico que copia el codigo de las funciones involucradas y dinamico que apunta la direccion de memoria donde se encuentra dicho codigo. 
2)
El procesador declara la funcion printf incluida en el directorio stdio.h que a su vez esta incluida en el directorio calculadora.h.
3)
add_numbers:
.LFB1:
	.cfi_startproc
	push	ebp
	.cfi_def_cfa_offset 8
	.cfi_offset 5, -8
	mov	ebp, esp
	.cfi_def_cfa_register 5
	mov	eax, DWORD PTR [ebp+12]
	mov	edx, DWORD PTR [ebp+8]
	add	eax, edx
	pop	ebp
	.cfi_def_cfa 4, 4
	.cfi_restore 5
	ret
	.cfi_endproc
4)
0000003d T add_numbers
00000000 T main
         U printf

Los numeros indican la direccion de memoria donde se alojan dichas funciones. 
Las letras indican si las funciones pueden ser llamadas externamente (mayusculas) o localmente por funciones dentro del programa (minusculas)(descriptores).
La ultima columna contienen el nombre de la funcion (entrada).
5)
En los decoradores y los sonames. Los sonames indican que las funciones  deben ser cargadas de una libreria local.
