# Reto 7

Estoy tratando de salvar la materia, así que trato de mandar la mayor cantidad de retos que dejé acumulados pensando que no iban a llevar su tiempo (No sé por qué no hay reto 5, no me acuerdo si era aparte o al profe se le pasó)
Bueno o malo, este reto si lo alcancé a adelantar antes de dejarlo de lado y acumularlo con otros 5, así que solo fue terminar otros que me faltaron para completar este repo, a demas que en el proyecto me quedé solito entonces me tocó ponerme modo guerrero.

Ya para iniciar con el reto en sí, nos piden lo siguiente, así que vamos a darle solución (A no ser tan largos los programas, decidí hacerlos en un cuadernillo para que sea más eficiente y más organizado)
Los programas al no ser tan largos y/o complejos, no creo que sean dificiles de entender, sin embargo, daré unas explicaciones breves para cada programita:

1. Números del 1 al 100 y sus cuadrados:

```python
Copy code
for i in range(1, 101):
    print(f"{i} - {i**2}")
````

Utiliza un bucle for para iterar sobre los números del 1 al 100.
Imprime cada número junto con su cuadrado.

2. Números impares del 1 al 999 y números pares del 2 al 1000:

```python
Copy code
print("Impares:")
for i in range(1, 1000, 2):
    print(i)

print("\nPares:")
for i in range(2, 1001, 2):
    print(i)
````
Dos bucles for separados: uno para impares y otro para pares.
El primer bucle imprime números impares desde 1 hasta 999 (incrementando de 2 en 2).
El segundo bucle imprime números pares desde 2 hasta 1000 (incrementando de 2 en 2).

3. Números pares en forma descendente:

```python
Copy code
n = int(input("Ingrese un número natural n ≥ 2: "))
for i in range(n, 1, -2):
    if i % 2 == 0:
        print(i)
````
Toma un número natural n como entrada.
Utiliza un bucle for para imprimir números pares en forma descendente hasta 2 que son menores o iguales a n.

4. Año en el que la población de B superará a A:

```python
Copy code
poblacion_A = 25e6
poblacion_B = 18.9e6
año = 2022

while poblacion_B <= poblacion_A:
    poblacion_A += poblacion_A * 0.02
    poblacion_B += poblacion_B * 0.03
    año += 1

print(f"La población de B superará a la de A en el año {año}")
````
Utiliza un bucle while para simular el crecimiento anual de las poblaciones de los países A y B.
Aumenta las poblaciones en un porcentaje dado anualmente.
Imprime el año en el que la población de B supera a la de A.

5. Factorial de un número natural:

```python
Copy code
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)

n = int(input("Ingrese un número natural: "))
print(f"El factorial de {n} es: {factorial(n)}")
````
Define una función recursiva factorial para calcular el factorial de un número.
Toma un número natural como entrada, calcula su factorial y lo imprime.

6. Adivinar un número:

```python
Copy code
import random

numero = random.randint(1, 100)
intentos = 0
print("Adivina el número entre 1 y 100")

while True:
    intentos += 1
    guess = int(input("Tu suposición: "))
    if guess < numero:
        print("El número es mayor.")
    elif guess > numero:
        print("El número es menor.")
    else:
        print(f"¡Correcto! Lo lograste en {intentos} intentos.")
        break
````
Genera un número aleatorio entre 1 y 100 que el usuario debe adivinar.
Utiliza un bucle while para solicitar al usuario que ingrese suposiciones hasta que adivinen el número.
Proporciona pistas sobre si el número es mayor o menor.

7. Mostrar divisores de un número:

```python
Copy code
n = int(input("Ingrese un número entre 2 y 50: "))

print(f"Divisores de {n}:")
for i in range(1, n + 1):
    if n % i == 0:
        print(i)
````
Toma un número entre 2 y 50 como entrada.
Utiliza un bucle for para encontrar y imprimir todos los divisores del número.

8. Números primos del 1 al 100:

```python
Copy code
def es_primo(num):
    if num < 2:
        return False
    for i in range(2, int(num**0.5) + 1):
        if num % i == 0:
            return False
    return True

print("Números primos del 1 al 100:")
for i in range(1, 101):
    if es_primo(i):
        print(i)
````
Define una función es_primo que verifica si un número es primo.
Utiliza un bucle for para iterar sobre los números del 1 al 100 e imprime los que son primos.

Como dije, explicaciones muy breves, pero espero que se hayan entendio. Gracias por hacer que el reto no fuera tan largo y menos mal ya tenía un avance:,)

Como siempre, gracias por pasar por aquí, espero se haya aprendido algo, ¡muchas gracias!
