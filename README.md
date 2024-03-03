# Analisis-FutbolData

Este repositorio contiene un script en Python que realiza un análisis de datos sobre el ranking de clubes de fútbol.

## Requisitos

Para ejecutar este script, necesitarás tener instalado lo siguiente:

- Python 3.x
- pandas
- pymongo

Puedes instalar las dependencias usando pip:

```bash
pip install pandas pymongo
```

## Descripción de los Scripts:

1. Ranking de equipos de futbol:
El script realiza las siguientes tareas:

1. Lee un archivo CSV que contiene el ranking de clubes de fútbol.
2. Elimina filas duplicadas del DataFrame.
3. Reemplaza los valores nulos en columnas numéricas por la media de cada columna.
4. Calcula el máximo, mínimo y promedio del ranking de los equipos.
5. Convierte el DataFrame a un diccionario para facilitar su inserción en MongoDB.
6. Conecta con una instancia local de MongoDB.
7. Inserta el diccionario en una colección llamada 'RankingDeEquipos' en la base de datos 'FutbolData'.
8. Cierra la conexión con MongoDB.

2. Ranking de jugadores de futbol:
1. Realiza las mismas opearaciones cambiando el csv por el que contiene la informacion de los jugadores.
2. Inserta el diccionario en una coleccion llamada 'RankingDeJugadores' en la base de datos FutbolData.

3. Inserción de datos:
1.Conexión a MongoDB Local: El script se conecta a dos bases de datos locales de MongoDB (basededatos1 y basededatos2) y a sus respectivas colecciones (coleccion1 y coleccion2).
2.Conexión a MongoDB Atlas: Se establece una conexión con MongoDB Atlas utilizando las credenciales proporcionadas en la URL de conexión.
3.Copia de datos: Se copian todos los documentos de las colecciones locales a una única colección en MongoDB Atlas.
4.Cierre de Conexiones: Finalmente, se cierran todas las conexiones establecidas.
   
