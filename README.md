# Programa 1: Búsqueda en una matriz bidimensional

def buscar_valor(matriz, valor):
    for i in range(len(matriz)):
        for j in range(len(matriz[i])):
            if matriz[i][j] == valor:
                return (i, j)
    return None

# Matriz 3x3 de ejemplo
matriz = [
    [5, 8, 3],
    [6, 9, 1],
    [4, 2, 7]
]

valor_a_buscar = int(input("Ingrese el valor a buscar: "))
resultado = buscar_valor(matriz, valor_a_buscar)

if resultado:
    print(f"El valor {valor_a_buscar} se encuentra en la posición {resultado}.")
else:
    print(f"El valor {valor_a_buscar} no se encuentra en la matriz.")

# Programa 2: Ordenación de una fila específica

def ordenar_fila(matriz, fila):
    matriz[fila].sort()
    return matriz

# Matriz 3x3 de ejemplo
matriz = [
    [5, 8, 3],
    [6, 9, 1],
    [4, 2, 7]
]

fila_a_ordenar = int(input("Ingrese el índice de la fila a ordenar (0-2): "))
matriz_ordenada = ordenar_fila(matriz, fila_a_ordenar)

print("Matriz ordenada:")
for fila in matriz_ordenada:
    print(fila)
