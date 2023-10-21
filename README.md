# Reto_8_Estuvo_chimbita_pa_que

## Punto 1

Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.

```
for n in range(0, 100):
  
    print(n, n**2)
    print(str(n) , (n**2))

```

## Punto 2

Imprimir un listado con los números impares desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.

```

for n in range(1,1001):
    if 2*n== 0:
    print(n)

for n in range(1,1000):
    if n % 2 == 1:
        print(n)
    n += 1

```

## Punto 3

Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado

```

n = int(input("Ingrese un numero mayor o igual a 2: "))
for n in range(n,1,-1):
  if n % 2 == 0:
  
    print(n)

```

## Punto 4

Imprimir los números de 1 hasta un número natural n dado, cada uno con su respectivo factorial

```
import math 

x=int(input("Ingrese un número: "))

for x in range (1, x+1):
 fact= math.factorial(x)
print("El factorial de" + str(x) + "es = " + str(fact))

```

## Punto 5

Calcular el valor de 2 elevado a la potencia n usando ciclos for.

```
n = int(input("Ingrese un número: "))
potencia = 1

for i in range(n-1):
  potencia *= 2
  
print("El resultado es: " + str(potencia))

```

## Punto 6 

Leer un número natural n, leer otro dato de tipo real x y calcular x^n usando ciclos for.

```

n = int(input("Ingrese un numero natural: "))
x = float(input("Ingrese un numero real: "))


def Potencia(n:float, x:int):
  resultado_potencia : int = 1
  for i in range(1,n+1):
    resultado_potencia *= x
  print(f"{x}^{n}={resultado_potencia}")

  print("La potencia de " + str(n) + "es: " + str(resultado_potencia))

```

## Punto 7 

Diseñe un programa que muestre las tablas de multiplicar del 1 al 9

```
def Tablas_de_multiplicar(n:int):
  print("Tabla de multiplicar de " +str(n))
  for i in range(1,11):
    Resultado = n*i
    print(f"{n}*{i}={Resultado}")
  print(n)

for n in range(1, 10):
  Tablas_de_multiplicar(n)

```

## Punto 8

Diseñar una función que permita calcular una aproximación de la función exponencial alrededor de 0 para cualquier valor x (real), utilizando los primeros n términos de la serie de Maclaurin. Nota: use math para traer la función exponencial y mostrar la diferencia entre el valor real y la aproximación.

```
import math 

def aprox_exp(x, n):
    aprox = 0.0        
    for i in range(n):  
        aprox += x**i / math.factorial(i) 
    real = math.exp(x)                    
    error = abs(real - aprox)             
    error_porcentaje = error / real * 100 # Calcula el porcentaje del error

    print(f"Aproximación: {aprox:.6f}") 
    print(f"Valor real:   {real:.6f}")    
    print(f"Diferencia:   {error:.6f}")   
    

    if error_porcentaje <= 0.1:  
        print (f"El porcentaje de error es menor a 0.1%: es de {error_porcentaje:} ") 
    else:
        print (f"El porcentaje de error es mayor a 0.1%: es de {error_porcentaje:} ")

```



## Punto 9 

Diseñar una función que permita calcular una aproximación de la función seno alrededor de 0 para cualquier valor x (real), utilizando los primeros n términos de la serie de Maclaurin. Nota: use math para traer la función seno y mostrar la diferencia entre el valor real y la aproximación.

```

import math as M
def seno(x, n):
    aprox = 0  
    for i in range(n):  
        termino = ((-1) ** i) * (x ** (2 * i + 1)) / math.factorial(2 * i + 1)  
        aprox += termino  
    return aprox  

if __name__ == '__main__':
    x = float(input("Ingresa un valor para x: ")) 
    n = 1
    error = 1 
    while error > 0.001:  # Siempre y cuando el error sea mayor que 0.1
        senoReal = math.sin(x) 
        seno_aproximado = seno(x, n) 
        n += 1  
    print("Se necesita n = {n} para tener un error menor o igual a 0.1%")
    print("Aproximación del seno: {seno_aproximado}")

```


## Punto 10

Diseñar una función que permita calcular una aproximación de la función arcotangente alrededor de 0 para cualquier valor x en el rango [-1, 1], utilizando los primeros n términos de la serie de Maclaurin. Nota: use math para traer la función arctan y mostrar la diferencia entre el valor real y la aproximación.

```
import math
def arctan(x, y):
    aprox = 0
    for i in range(n):
        aprox += ((-1) ** i) * (x ** (2 * i + 1)) / (2 * i + 1)
    return aprox
x = float(input("Ingrese un valor de x (debe estar en el rango [-1, 1]): "))
if x < -1 or x > 1:
    print("Papi/mami por ahi no es ")
    
else:
    n = int(input("Ingrese el número de términos de la serie de Maclaurin a utilizar: "))
    aprox = arctan(x, y)
    valorReal = math.atan(x)
    Diferencia = valorReal - aprox
    print("La aproximación de la función arcotangente para x = " +str(x)+ " utilizando los primeros " +str(y)+ " términos de la serie de Maclaurin es: " +str(aprox))
    print("El valor de la función arcotangente para x = " +str(n)+ " es: " +str(valorReal))
    print("La diferencia entre la aproximación y el valor real es: " +str(Diferencia))

```
