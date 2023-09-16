# Reto No. 3: "Entre prima y primo, más me arrimo"
1. A partir del algoritmo de identificación de los divisores plantear la serie de pasos para determinar los números primos hasta un natural n, usando pseudocódigo y diagramas de flujo.

## SEUDOCÓDIGO: 
Defino las variables iniciales:
 - n es el número natural hasta el que se determinarán los primos.
 - i es un contador para saber si es primo, haciendo uso de la criba de Heratóstenes, va desde 2 hasta (n^0.5)+1
 - j es un contador que prueba si ese número es primo, va desde 2 hasta n
 - lista_primos es la lista en donde serán agregados los números primos.

```pseudocode
[variables]
n : entero    
i : entero    
j : entero
lista_primos: ()  

inicio
  j :=2
  Mientras (j <= n) hacer
    i := 2

    Mientras (i < ((n^0.5)+1) ) hacer
    # Haciendo uso de la criba de Heratóstenes, verificamos hasta (n^0.5)+1
      Si modulo(j,i) == 0 entonces
        escribir("i es divisor de j, j no es primo")
        salir del ciclo interno, pues j no es primo y probar con el siguiente número (j + 1) 
      sino
        escribir("i no es divisor de j")
      i := i + 1
    Fin mientras

    Si ( i > ((n^0.5)+1) )
       Agregar j a la lista de números primos lista_primos
       escribir("j es un número primo")
    j := j + 1
 Fin mientras
fin
```




2. Revise el procedimiento matemático para hallar raíces cuadradas (son divisiones y restas), plantee el algoritmo en pseudocódigo y en diagrama de flujo.


