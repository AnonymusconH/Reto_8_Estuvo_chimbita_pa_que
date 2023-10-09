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
