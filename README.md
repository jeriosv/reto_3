# Reto No. 3: "Entre prima y primo, más me arrimo"
1. A partir del algoritmo de identificación de los divisores plantear la serie de pasos para determinar los números primos hasta un natural n, usando pseudocódigo y diagramas de flujo.

SEUDOCÓDIGO

```pseudocode
[variables]
n : entero (es el n)
i : entero
inicio
  i := 2
  Mientras (i < ((n^0.5)+1) ) hacer      #Haciendo uso de la criba de Heratóstenes, verificamos hasta (n^0.5)+1
    Si modulo(n,i) == 0 entonces
      escribir("i es divisor de n")
    sino
      escribir("i no es divisor de n")
    i := i + 1
  Fin mientras
fin
```




2. Revise el procedimiento matemático para hallar raíces cuadradas (son divisiones y restas), plantee el algoritmo en pseudocódigo y en diagrama de flujo.


