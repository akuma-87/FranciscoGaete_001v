# FranciscoGaete_001v
#FranciscoGaete_001v

productos = {'8475HD': ['HP', 15.6, '8GB', 'DD', '1T', 'Intel Core i5', 'Nvidia GTX1050'],
             '2175HD': ['Acer', 14, '4GB', 'SSD', '512GB', 'Intel Core i5', 'Nvidia GTX1050'],
             'JjfFHD': ['Asus', 14, '16GB', 'SSD', '256GB', 'Intel Core i7', 'Nvidia RTX2080Ti'],
             'fgdxFHD': ['HP', 15.6, '12GB', 'DD', '1T', 'Intel Core i3', 'integrada'],
             'GF75HD': ['Asus', 15.6, '12GB', 'DD', '1T', 'Intel Core i7', 'Nvidia GTX1050'],
             '123FHD': ['Acer', 14, '6GB', 'DD', '1T', 'AMD Ryzen 5', 'integrada'],
             '342FHD': ['Acer', 15.6, '8GB', 'DD', '1T', 'AMD Ryzen 7', 'Nvidia GTX1050'],
             'UWU131HD': ['Dell', 15.6, '8GB', 'DD', '1T', 'AMD Ryzen 3', 'Nvidia GTX1050']}

stock = {'8475HD': [387990,10], '2175HD': [327990,4], 'JjfFHD': [424990,1],'fgdxFHD': [664990,21],
         '123FHD': [290890,32], '342FHD': [444990,7],
         'GF75HD': [749990,2], 'UWU131HD': [349990,1], 'FS1230HD': [249990,0], 
          }






def Stock_marca():
    try:
        marca = input("Ingrese marca a consultar: ")
        if marca == "":
            for marca in range(productos):
                print(f"El stock es de: {marca}")
        else:
            print("Debe ingresar una marca que corresponda..")
    except Exception as e:
        print("Debe ingresar una marca existente!!")


def Busqueda_por_precio():
    while True:
        try:
            p_min = int(input("Ingrese precio mínimo: "))
            if p_min < 0:
                print("debe ingresar un numero mayor a cero")        
            p_max = int(input("Ingrese precio máximo: "))
            if p_max < 0:
                print("debe ingresar un valor mayor a cero")
            if p_min in stock:
                if p_max in stock:
                    for i in range(stock):
                        print(f"los notebooks entre los precios consultas son: {i}")
            else:
                print("Debe ingresar valores enteros!!")
        except Exception as e:
            print("ingrese un valor que corresponda...",e)

def eliminar_producto():
    try:
        modelo = input("Ingrese modelo a actualizar: ")
        for modelo in len(range(productos)):
            if modelo == productos:
                del productos.append()
                print("Producto eliminado!!")
    except Exception as e:
        print("Debe ingresar un producto existente!!")
        


def salir():
    print("programa finalizado.")
    exit()

#main
while True:
        try:
            print("\n*** MENU PRINCIPAL ***")
            print("1. Stock marca.")
            print("2. Búsqueda por precio.")
            print("3. Eliminar producto.")
            print("4. Salir.")
            op = input("Ingrese una opcion: ")
            if op == "1":
                Stock_marca()
            elif op == "2":
                Busqueda_por_precio()
            elif op == "3":
                eliminar_producto()
            elif op == "4":
                salir()
            else:
                print("Debe ingresar una opcio del 1-4..")
        except Exception as e:
            print("Debe ingresar numeros enteros",e)

