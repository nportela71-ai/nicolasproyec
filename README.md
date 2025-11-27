donaciones = []

def registrar_donacion():
    nombre = input("nombre donante: ")
    articulo = input("comida para gaticos: ")
    cantidad = int(input("cantidad (numero): "))

 donacion ={
        "nombre": nombre,
        "articulo": articulo,
        "cantidad":cantidad
    }

    donaciones.append(donacion)
    print("donacion exitosa")


def mostrar_donaciones():
    if (donaciones) == 0:
        print("no hay donacion exitosa")
        return
    
    print("lista de donaciones:")
    for d in donaciones:
        print(f"{d["nombre"]} dono {d["cantidad"]} {d["articulo"]}")

def buscar_nombre():
            nombre = input("nombre del donante de:")
            encontrado = False

            for d in donaciones:
                if d["nombre"].lower() == nombre.lower():
                    print(f"{d["nombre"]} dono {d["cantidad"]} {d["articulo"]}")
                    encontrado = True

                    if not encontrado:
                        print("no se encontraron donaciones de {nombre}.")

def total_articulo():
                    total = 0
                    for d in donaciones:

                        total += d["cantidad"]

                    print(f"total de articulos donados: {total}")
while True: 
    print(" sistema de donaciones para gaticos")
    print("1. registrar donacion")
    print("2. mostrar donaciones")
    print("3. buscar donantes por nombre")
    print("4. total de donaciones")
    print("5. salir")

    opcion = input("seleccione una opcion (1,2,3,4,5):")
    if opcion == "1":
        registrar_donacion()
    elif opcion == "2":
        mostrar_donaciones()
    elif opcion == "3":
        buscar_nombre()
    elif opcion == "4":
        total_articulo()
    elif opcion == "5":
        print("gracias por usar el sistema de donaciones para gaticos. !adios!")
        break
    else:
        print("opcion invalida. por favor intente de nuevo.")
                    
