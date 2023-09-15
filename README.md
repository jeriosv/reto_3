# Reto No. 3: "Entre prima y primo, más me arrimo"
1. A partir del algoritmo de identificación de los divisores plantear la serie de pasos para determinar los números primos hasta un natural n, usando pseudocódigo y diagramas de flujo.



```pseudocode
[variables]
n : entero
i : entero
inicio
  i := 2
  Mientras (i < n) hacer
    Si modulo(n,i) == 0 entonces
      escribir("i es divisor de n")
    sino
      escribir("i no es divisor de n")
    i := i + 1
  Fin mientras
fin
```




2. Revise el procedimiento matemático para hallar raíces cuadradas (son divisiones y restas), plantee el algoritmo en pseudocódigo y en diagrama de flujo.


