# Reto No. 3: "Entre prima y primo, más me arrimo"

## Cálculo de Números Primos hasta n: 

1.  A partir del algoritmo de identificación de los divisores plantear la serie de pasos para determinar los números primos hasta un natural n, usando pseudocódigo y diagramas de flujo.

Para el seudocódigo defino las variables iniciales:
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

[![](https://mermaid.ink/img/pako:eNp1kclOw0AMhl_F8qmV0ipLm00s6kIRBzhQTjQVGiXTdEoyU00mgpL0kXgBLkj0xZgkIHFhDpZlf_ZvjyuMRUIxxE0mXuItkQoe5hGPOOg36d1wFjPRh8HgouZlTqUAXsO0Z8PZOewaw_sdO20YmFVfn8CBFrCXLBdweeyys7bD8vRew3x1TwuWlKKAhG2opFxpPKFgrluIaBmuiISdFvpbfSdquFpNsvT0wUF2PRql_-vmbWKSSpoSWcNi9eMCgYwVijy1QxZr6PBFg1_3Fux3JzRQr5wTlugPqppYhGpLcxphqN2EyOcII37UHCmVWB54jKGSJTWw3CdE0TkjqSQ5hhuSFTq6JxzDCl8xdEb20PZsL3A9dxz43tjAA4aWNRp6ru9YluM7XmD5ztHANyF0B3Po2mYw9n3L9qyRb7qWgTRhSsjb7oDtHVuJx7agmeP4DXLKktU?type=png)](https://mermaid.live/edit#pako:eNp1kclOw0AMhl_F8qmV0ipLm00s6kIRBzhQTjQVGiXTdEoyU00mgpL0kXgBLkj0xZgkIHFhDpZlf_ZvjyuMRUIxxE0mXuItkQoe5hGPOOg36d1wFjPRh8HgouZlTqUAXsO0Z8PZOewaw_sdO20YmFVfn8CBFrCXLBdweeyys7bD8vRew3x1TwuWlKKAhG2opFxpPKFgrluIaBmuiISdFvpbfSdquFpNsvT0wUF2PRql_-vmbWKSSpoSWcNi9eMCgYwVijy1QxZr6PBFg1_3Fux3JzRQr5wTlugPqppYhGpLcxphqN2EyOcII37UHCmVWB54jKGSJTWw3CdE0TkjqSQ5hhuSFTq6JxzDCl8xdEb20PZsL3A9dxz43tjAA4aWNRp6ru9YluM7XmD5ztHANyF0B3Po2mYw9n3L9qyRb7qWgTRhSsjb7oDtHVuJx7agmeP4DXLKktU)


## Cálculo de la raíz cuadrada de un número: 

2. Revise el procedimiento matemático para hallar raíces cuadradas (con divisiones y restas), plantee el algoritmo en pseudocódigo y en diagrama de flujo.

Para calcular una aproximación de la raíz cuadrada de un número utilizando divisiones y restas usamos el método de aproximación babilónico, también conocido como el método Herón.

Comenzamos con una suposición inicial igual al número que queremos calcular. Luego en cada iteración, calculamos una nueva aproximación de la raíz cuadrada dividiendo y restando, y comparamos la diferencia entre las aproximaciones con una tolerancia para decidir si detener las iteraciones. Cuantas más iteraciones realices, mayor será la precisión de la aproximación.

Para el seudocódigo defino las variables iniciales:
 - numero es el número real al que se le aproximará su raíz cuadrada
 - iteraciones es un número natural grande, supongo hacer 1000
 - tolerancia es un número real pequeño, lo defino como el 0,01% del numero
 - raiz es un número real resultado

```pseudocode
[variables]
numero : real
iteraciones : entero
tolerancia  : real
raiz : real 

inicio
    iteraciones := 1000
    tolerancia := 0,0001 * numero
    # Suposición inicial (cualquier valor positivo)
    raiz = numero

    # Realizar iteraciones
    Mientras (iteraciones esté en el rango de 1 a 1000) hacer
        # Calcular una nueva aproximación dividiendo y restando, nueva_raiz es una variable temporal
        nueva_raiz = 0.5 * (raiz + numero / raiz)

        # Verificar si la diferencia entre las aproximaciones es menor que la tolerancia
        si    (valor absoluto de(nueva_raiz - raiz) < tolerancia)
            salir del ciclo porque llegamos a la tolerancia esperada (break)

        raiz = nueva_raiz
     Fin mientras

    imprimir ("La raiz cuadrada de numero es " +  raiz)
  fin

```


