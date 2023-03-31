# BIBLIOTECA
Libros = [
    ("Harry Potter y la piedra filosofal", "J.K Rowling", "HPJK1997", 1997, 25000, 9000),
    
    ("Los Juegos Del Hambre", "Suzanne Collins", "JHSC2008", 2008, 27000, 12000),
   
     ("El Hobbit", "J.R.R. Tolkien", " EHJR1937", 1937, 35000, 15000),
   
     ("Hamlet", "William shakespeare", "HWS1589", 1589, 26000, 13000)
]

def es_buena_opcion(libro):
    if Libro[5] >= 100:
        ganancia = Libro[4] - 14000
        if Libro[5] > 800:
            ganancia *= 1.1
        return ganancia > 0
    else:
        return False

mejor_Libro = None
for Libro in Libros:
    if es_buena_opcion(Libro):
        if mejor_Libro is None or Libro[4] < mejor_Libro[4]:
            mejor_Libro = Libro

if mejor_Libro is not None:
    print(f"El mejor Libro para ser vendido es '{mejor_Libro[0]}' de {mejor_Libro[1]} con código {mejor_Libro[2]}, publicado en {mejor_Libro[3]} y un precio de {mejor_Libro[4]} pesos.")
    
else:
    print("Ninguno de los libros es la mejor opción para ser vendido.")
