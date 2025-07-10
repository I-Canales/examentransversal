productos = {
    '8475HD': ['HP', 15.6,'8GB','DD','1T','intel Core i5','Nvidia GTX1050'],
    '2175HD': ['lenovo', 14,'4GB,DD','SSD','512GB','Intel Core i5', 'Nvidia GTX1050'],
    'JjfFHD': ['asus', 14,'16GB', 'SSD', '256GB', 'Intel Core i7','Nvidia RTX2080 Ti' ],
    'fgdxFHD': ['HP', 15.6,'8GB', 'DD', '1T', 'Intel Core i3', 'integrada'],
    'GF75HD': ['asus', 15.5, '8GB','DD', '1T', 'Intel Core i7', 'Nvidia GTX1050'],
    '123fhd': ['lenovo', 15.6,'6GB','DD', '1T', 'AMD RYZEN 5','INTEGRADA'],
    '342FHD': ['lenovo', 15.6, '8GB', 'DD', '1T, AMD Ryzen 7', 'Nvidia GTX1050'],
    'UWU131HD': ['dell', 15.6,'8GB', 'DD', '1T', 'AMD Ryzen3''Nvidia GTX1050'],
}
stok = {
    '8475HD': [387990,10],
    '2175HD': [327990,4],
    'JjfFHD': [464990,1],
    'fgdxFHD': [664990,21],
    'GF75HD': [749990,2],
    '123fhd': [190890,32],
    '342FHD': [444990,7],
    'UWU131HD': [349990,1],
    'FS1230HD': [249990,0],
}       
def Stok_marca(marca):
    print(f"\nStok de las marcas '{marca}")
    encontrados = False
    for modelo, datos, in productos.items():
        if datos [0].lower() == marca.lower():
         print(f"\n{productos}: {stok[modelo][1]} unidades")
         encontrados = True 
    if not encontrados:
     print("no se encontraron notebooks de ese valor")
def busqueda_precio (p_min, p_max):
   encontrados = []
   for modelo, datos in productos.items():
      precio, cantidad = datos
      if p_min <= precio <= p_max and datos [1] > 0:
         if modelo in productos:
            marca = productos [modelo] [0]
            encontrados.append(f"\n{marca} {modelo}")
   if encontrados: 
    print("no se a encontrado ningun noteboocks con su presupuesto", encontrados)
   else:
      print("no se encuentran notebooks en su rango de precio")
def actualizar_precios(modelo, precio_actualizado):
   if modelo in stok:
      stok[modelo][0] = precio_actualizado 
      return True
   else:
      return False

menu()
                





                




