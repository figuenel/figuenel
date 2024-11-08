import math

# Función para sumar
def suma(a, b):
    return a + b

# Función para restar
def resta(a, b):
    return a - b

# Función para multiplicar
def multiplicacion(a, b):
    return a * b

# Función para dividir
def division(a, b):
    if b != 0:
        return a / b
    else:
        return "Error: División por cero"


# Función para mostrar el menú
def menu():
    print("Operaciones matemáticas disponibles:")
    print("1. Sumar")
    print("2. Restar")
    print("3. Multiplicar")
    print("4. Dividir")
    print("5. Salir")

# Función principal
def calculadora():
    while True:
        menu()
        opcion = input("Elige una operación (1-5): ")
        

        if opcion == '5':
            print("Gracias por usar la calculadora. ¡Adiós!")
            break
        
        if opcion in ['1', '2', '3', '4', ]:
            # Pedir los números al usuario
            try:
                a = float(input("Introduce el primer número: "))
                b = float(input("Introduce el segundo número: ")) if opcion != '5' else None
            except ValueError:
                print("Error: Por favor ingresa números válidos.")
                continue

            # Realizar la operación correspondiente
            if opcion == '1':
                print(f"{a} + {b} = {suma(a, b)}")
            elif opcion == '2':
                print(f"{a} - {b} = {resta(a, b)}")
            elif opcion == '3':
                print(f"{a} * {b} = {multiplicacion(a, b)}")
            elif opcion == '4':
                print(f"{a} / {b} = {division(a, b)}")
      
            
        else:
            print("Opción no válida. Por favor, elige una opción entre 1 y 5.")

# Ejecutar la calculadora
calculadora()
