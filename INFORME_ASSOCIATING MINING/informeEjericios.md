
# Escuela Politécnica Nacional

<div align="center">

**Integrantes:**  
Javier Angulo, Jotcelyn Godoy, Javier Quilumba, Cristian Robles, Jonathan Tipán

**Fecha:** 10/07/2026  
**Paralelo:** GR2SW

</div>

---

## 10.6 Aplicación del algoritmo Apriori en Weka a un conjunto de datos del mundo real.

**Objetivo:**  
**Ejecutar el algoritmo Apriori en un conjunto de datos dado (Tabla 10.3) y, por lo tanto, elegir la mejor regla de asociación usando Weka.**

---

1. En un Excel se debe realizar el siguiente formato usando la tabla de transacciones dada.

<p align="center">
  <img src="paso-1.png" alt="Formato en Excel" />
</p>

2. Guardar con el nombre "DailyItem Dataset" en el Escritorio como un archivo CSV (delimitado por comas).

<p align="center">
  <img src="paso-2.png" alt="Guardar archivo CSV" />
</p>

3. En Weka, en el explorador, en la ventana de "Preprocess", buscamos el archivo después de dar clic en "Open file" y lo abrimos.

<p align="center">
  <img src="paso-4.png" alt="Abrir archivo en Weka" />
</p>

**Datos cargados:**

<p align="center">
  <img src="paso-5.png" alt="Datos cargados en Weka" />
</p>

4. Como no se puede aplicar la asociación de datos directamente en datos numéricos, en el botón "Choose" seleccionamos filtros, luego "Unsupervised", entramos a "attribute" y seleccionamos "Numeric to Nominal". Finalmente, se aplican los cambios.

<p align="center">
  <img src="paso-6.png" alt="Aplicar filtro Numeric to Nominal" />
</p>

**Búsqueda de filtro:**

<p align="center">
  <img src="paso-7.png" alt="Búsqueda de filtro en Weka" />
</p>

**Aplicando el filtro obtenemos esto:**

<p align="center">
  <img src="paso-8.png" alt="Resultado del filtro aplicado" />
</p>

5. Eliminamos los atributos que no necesitamos; en este caso se lo hará con "Transaction", primero se selecciona dicho check en el menú de la izquierda y luego se presiona el botón de "Remove".

<p align="center">
  <img src="paso-9.png" alt="Eliminar atributo Transaction" />
</p>

**El atributo "Transaction" eliminado:**

<p align="center">
  <img src="paso-10.png" alt="Atributo Transaction eliminado" />
</p>

6. Una vez "limpios" los datos cargados, seleccionamos la pestaña de "Associate" y, en "Choose", seleccionamos la opción "Apriori" de "associations".

<p align="center">
  <img src="paso-11.png" alt="Seleccionar Apriori en Weka" />
</p>

7. Ahora, para ingresar al editor de objetos generales, se da clic en el campo de "Apriori" y se realizan cambios en algunos campos según lo requerido:

- lowerBoundMinSupport = 0.5
- metricType = Confidence
- minMetric = 0.75
- numRules = 10

Luego se selecciona "OK".

<p align="center">
  <img src="paso-12.png" alt="Configuración de Apriori" />
</p>

8. Finalmente, se selecciona el botón de "Start" y se obtienen los resultados en la pantalla derecha.

<p align="center">
  <img src="paso-13.png" alt="Resultados obtenidos en Weka" />
</p>

9. Ahora podemos interpretar los resultados, observando la imagen respectiva a las reglas encontradas.

<p align="center">
  <img src="paso-14.png" alt="Reglas encontradas en Weka" />
</p>

**Se puede resumir en que la mejor regla encontrada es:**

- Jam -> Cornflakes

El orden dado por el porcentaje de mayor a menor, que en este caso nos arroja que cuando se compra Jam (Mermelada) hay un 100% de confianza (conf: 1) de que también se compre Cornflakes (Hojuelas de maíz), coincidiendo perfectamente con lo estudiado antes de forma manual.

---

## 10.7 Aplicación del Algoritmo Apriori en Weka en un Conjunto de Datos Real Más Grande

**Objetivo:**  
**Ejecutar el algoritmo Apriori en un conjunto de datos (dataset) dado con soporte y confianza predefinidos, y luego interpretar el resultado.**

---

1. En un Excel se debe realizar el siguiente formato y guardarse como un archivo CSV.

<p align="center">
  <img src="image.png" alt="Formato en Excel" />
</p>

2. Guardar con el nombre "DailyItmen2 Dataset" en el Escritorio como un archivo CSV (delimitado por comas).

<p align="center">
  <img src="image-1.png" alt="Guardar archivo CSV" />
</p>

3. En Weka, en el explorador, en la ventana de "Preprocess", buscamos el archivo después de dar clic en "Open file" y lo abrimos.

<p align="center">
  <img src="image-2.png" alt="Abrir archivo en Weka" />
</p>

**Datos cargados:**

<p align="center">
  <img src="image-3.png" alt="Datos cargados en Weka" />
</p>

4. Como no se puede aplicar la asociación de datos directamente en datos numéricos, en el botón "Choose" seleccionamos filtros, luego "Unsupervised" y "Numeric to Nominal". Finalmente, se aplican los cambios.

<p align="center">
  <img src="image-4.png" alt="Aplicar filtro Numeric to Nominal" />
</p>

**Búsqueda de filtro**

<p align="center">
  <img src="image-5.png" alt="Búsqueda de filtro en Weka" />
</p>

**Aplicando el filtro obtenemos esto:**

<p align="center">
  <img src="image-6.png" alt="Resultado del filtro aplicado" />
</p>

5. Eliminamos los atributos que no necesitamos; en este caso se lo hará con "Transaction", primero se selecciona dicho check en el menú de la izquierda y luego se presiona el botón de "Remove".

<p align="center">
  <img src="image-7.png" alt="Eliminar atributo Transaction" />
</p>

**El atributo "Transaction" eliminado**

<p align="center">
  <img src="image-8.png" alt="Atributo Transaction eliminado" />
</p>

6. Una vez "limpios" los datos cargados, seleccionamos la pestaña de "Associate" y, en "Choose", seleccionamos la opción "Apriori" de "association".

<p align="center">
  <img src="image-9.png" alt="Seleccionar Apriori en Weka" />
</p>

7. Ahora, para ingresar al editor de objetos generales, se da clic en el campo de "Apriori" y se realizan cambios en algunos campos:

- lowerCoundMinSupport = 0.5
- metricType = Confidence
- minMetric = 0.75

Luego se selecciona "OK".

<p align="center">
  <img src="image-10.png" alt="Configuración de Apriori" />
</p>

8. Finalmente, se selecciona el botón de "Start" y se obtienen los resultados.

<p align="center">
  <img src="image-11.png" alt="Resultados obtenidos en Weka" />
</p>

9. Ahora podemos interpretar los resultados; observando la imagen respectiva a las reglas encontradas.

<p align="center">
  <img src="image-12.png" alt="Reglas encontradas en Weka" />
</p>

**Se puede resumir en que las mejores reglas son:**

- Cornflake -> Jam
- Jam -> Bread
- Bread -> Jam
- Jam -> Cornflake

El orden dado por el porcentaje de mayor a menor, ordenados de manera descendente.

---

## 10.8

## 10.9