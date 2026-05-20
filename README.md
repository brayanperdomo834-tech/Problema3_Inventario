# Matriz del inventario
inventario = [
    [701, "Micrófono", 4, 11],
    [702, "Smartwatch", 17, 12],
    [703, "Ordenador", 3, 7],
    [704, "Switch de Red", 23, 12],
    [705, "SSD NVMe", 2, 8]
]

# Función para calcular la cifra total del producto solicitado
def calcular_stock(stock_actual, stock_minimo):

    if stock_actual < stock_minimo:
        cifra = stock_minimo - stock_actual
    else:
        cifra = 0

    return cifra


# Mostrar resultados
print("LISTA DE PROVISIONES\n")

for producto in inventario:

    codigo = producto[0]
    nombre = producto[1]
    stock_actual = producto[2]
    stock_minimo = producto[3]

    cantidad_stock = calcular_stock(stock_actual, stock_minimo)

    print("Producto:", nombre)
    print("Cantidad sugerida:", cantidad_stock)
    print("----------------------")
