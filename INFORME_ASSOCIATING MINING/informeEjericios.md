
# Escuela Politécnica Nacional

Integrantes:
Javier Angulo, Jotcelyn Godoy, Javier Quilumba, Cristian Robles, Jonathan Tipán

Fecha: 10/07/2026
Paralelo: GR2SW

## 10.6

## 10.7 Aplicación del Algoritmo Apriori en Weka en un Conjunto de Datos Real Más Grande

**Objetivo:**
**Ejecutar el algoritmo Apriori en un conjunto de datos (dataset) dado con soporte y confianza predefinidos, y luego interpretar el resultado.**

1. En un Excel se debe realizar el siguiente formato y guardarse como un csv.
![alt text](image.png)
2. Guardar con el nombre 'DailyItmen2 Dataset' en el Escritorio como un archivo csv (delimitado por comas)
![alt text](image-1.png)
3. En Weka en el explorador, la ventana de 'Preprocess' buscamos el archivo luego de darle click al 'Open file' y lo abrimos
![alt text](image-2.png)
Datos cargados:
![alt text](image-3.png)
4. Como no se puede aplicar la asociación de datos directamente en datos numéricos, así que en el botón 'Choose' seleccionamos filtros, no supervisados (unsupervised) y 'Numeric to Nominal filter'. Finalmente se aplican los cambios.
![alt text](image-4.png)
Búsqueda de filtro
![alt text](image-5.png)
Aplicando el filtro obtenemos esto:
![alt text](image-6.png)
5. Eliminamos los atributos que no necesitamos; en este caso se lo hará con 'Transaction', primero se selecciona dicho check en el menú de la izquierda y luego presionamos el botón de 'Remove'
![alt text](image-7.png)
El atributo 'Transaction' eliminado
![alt text](image-8.png)
6. Una vez 'limpios' los datos cargados, seleccionamos la pestaña de 'Associate' y en 'Choose' seleccionamos la opción 'Apriori' de 'association'
![alt text](image-9.png)
7. Ahora, para ingresar al editor de objetos generales, se da un click en el campo de 'Apriori' y se realizan cambios en algunos campos:
* lowerCoundMinSupport = 0.5
* metricType = Confidence
* minMetric = 0.75
Y se selecciona 'OK'
![alt text](image-10.png)
8. Finalmente se selecciona el botón de 'Start' y se obtienen los resultados
![alt text](image-11.png)
9. Ahora podemos interpretar los resultados:
Observando la imagen respectivamente a las reglas encontradas
![alt text](image-12.png)
Se puede resumir en que las mejores reglas son:
Cornflake -> Jam
Jam -> Bread
Bread -> Jam
Jam -> Cornflake
El orden dado por el porcentaje de mayor a menor ordenados de manera descendente

## 10.8

## 10.9