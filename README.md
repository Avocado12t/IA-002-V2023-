# IA-002-V2023-
Tarea Inteligencia Artificial 

Ejercicio 1

# Solicitar al usuario dos números
numero1 = float(input("Ingrese el primer número: "))
numero2 = float(input("Ingrese el segundo número: "))

# Calcular la suma de los dos números
suma = numero1 + numero2

# Mostrar el resultado
print("La suma de", numero1, "y", numero2, "es:", suma)

Ejercicio 2 

# Solicitar al usuario un número
numero = int(input("Ingrese un número entero positivo: "))

# Verificar si el número es válido
if numero < 0:
    print("El número debe ser positivo.")
elif numero == 0:
    print("El factorial de 0 es 1.")
else:
    factorial = 1
    for i in range(1, numero + 1):
        factorial *= i
    print("El factorial de", numero, "es:", factorial)

Ejercicio 3

# Función para buscar la posición de un número en la lista
def buscar_posicion(lista, objetivo):
    for i in range(len(lista)):
        if lista[i] == objetivo:
            return i
    return -1

# Solicitar al usuario una lista de números
numeros = input("Ingrese una lista de números separados por espacios: ").split()

# Convertir los elementos de la lista a números enteros
numeros = [int(numero) for numero in numeros]

# Solicitar al usuario el número objetivo
objetivo = int(input("Ingrese el número objetivo: "))

# Buscar la posición del número objetivo en la lista
posicion = buscar_posicion(numeros, objetivo)

# Mostrar el resultado
if posicion != -1:
    print("El número objetivo", objetivo, "se encuentra en la posición", posicion)
else:
    print("El número objetivo", objetivo, "no se encuentra en la lista.")

Ejercicio 4

def es_palindromo(cadena):
    # Eliminar espacios y convertir todo a minúsculas
    cadena = cadena.replace(" ", "").lower()

    # Verificar si la cadena es un palíndromo
    if cadena == cadena[::-1]:
        return True
    else:
        return False

# Solicitar al usuario una cadena de texto
texto = input("Ingrese una cadena de texto: ")

# Verificar si es un palíndromo
if es_palindromo(texto):
    print("La cadena es un palíndromo.")
else:
    print("La cadena no es un palíndromo.")
