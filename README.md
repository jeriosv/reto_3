# Reto No. 3: "Entre prima y primo, más me arrimo"
1.  A partir del algoritmo de identificación de los divisores plantear la serie de pasos para determinar los números primos hasta un natural n, usando pseudocódigo y diagramas de flujo.

## SEUDOCÓDIGO: 
Defino las variables iniciales:
 - numero es el número natural hasta el que se determinarán los primos.
 - i es un contador para saber si es primo, haciendo uso de la criba de Heratóstenes, va desde 2 hasta (numero^0.5)+1
 - j es un contador que prueba si ese número es primo, va desde 2 hasta n
 - lista_primos es la lista en donde serán agregados los números primos.

```pseudocode
[variables]
numero : entero    
i : entero    
j : entero
lista_primos: ()  

inicio
  j :=2
  Mientras (j <= numero) hacer
     i := 2
 
     Mientras (i < ((numero^0.5)+1) ) hacer
     # Haciendo uso de la criba de Heratóstenes, verificamos hasta (numero^0.5)+1
        Si modulo(j,i) == 0 entonces
           escribir("i es divisor de j, j no es primo")
           salir del ciclo interno, pues j no es primo y probar con el siguiente número (j + 1) 
        sino
           escribir("i no es divisor de j")
        i := i + 1
     Fin mientras

     Si ( i > ((numero^0.5)+1) )
         Agregar j a la lista de números primos lista_primos
         escribir("j es un número primo")
     j := j + 1
 Fin mientras
fin
```




2. Revise el procedimiento matemático para hallar raíces cuadradas (con divisiones y restas), plantee el algoritmo en pseudocódigo y en diagrama de flujo.

Para calcular una aproximación de la raíz cuadrada de un número utilizando divisiones y restas usamos el método de aproximación babilónico, también conocido como el método Herón.

Comenzamos con una suposición inicial igual al número que queremos calcular. Luego en cada iteración, calculamos una nueva aproximación de la raíz cuadrada dividiendo y restando, y comparamos la diferencia entre las aproximaciones con una tolerancia para decidir si detener las iteraciones. Cuantas más iteraciones realices, mayor será la precisión de la aproximación.

```pseudocode
[variables]
numero : real
iteraciones : entero
tolerancia  : real
raiz : real 


inicio
    iteraciones := 1000
    tolerancia := 0,0001 * n
    # Suposición inicial (cualquier valor positivo)
    raiz = numero

    # Realizar iteraciones
    Mientras (iteraciones esté en el rango de 1 a 1000) hacer
        # Calcular una nueva aproximación dividiendo y restando, nueva_raiz es una variable temporal
        nueva_raiz = 0.5 * (raiz + numero / raiz)

        # Verificar si la diferencia entre las aproximaciones es menor que la tolerancia
        si    (valor absoluto de(nueva_raiz - raiz) < tolerancia)
            continuar con la siguiente iteracion

        raiz = nueva_raiz
     Fin mientras

    imprimir ("La raiz cuadrada de numero es " +  raiz)
  fin

```


