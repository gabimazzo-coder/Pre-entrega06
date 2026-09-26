# Pre-entrega06
# Analizador de Datos del Clima con DuckDB

Este proyecto contiene un script en [Python / SQL] que utiliza **DuckDB** para procesar, limpiar y analizar un conjunto de datos climáticos de manera eficiente. El proceso incluye la carga de datos como tablas virtuales, la limpieza de valores nulos y la generación de métricas agregadas.

## 🚀 Requisitos Previos

Antes de ejecutar el script, hay que asegurarse  de tener instalado lo siguiente:

* **Python 3.8+** 
* **DuckDB** 

Yo igualmente usé GoogleColab

## 📂 Estructura del Proyecto

* `main.py` (o `query.sql`): Script principal que ejecuta el pipeline de datos.
* `agd_i_ppt_pais_por_prov_2010_2024.csv`: Archivo de origen con los datos de temperatura y estaciones 
* `README.md`: Documentación del proyecto.

## ⚙️ Funcionalidades del Script

El archivo realiza de forma secuencial las siguientes operaciones:

1. **Carga y Registro Virtual**: Lee el archivo fuente de datos directamente y lo registra como una tabla virtual en DuckDB, optimizando el uso de memoria.
2. **Limpieza de Datos**: Identifica y maneja los valores nulos (`NULL`) en las columnas de temperatura, reemplazando los valores NULL con el promedio de esa misma columna
3. **Análisis Agregado**: Calclula y genera métricas clave:
   * Promedios de temperatura mensuales.
   * Máximos históricos de temperatura registrados por cada estación.

## 💻 Instrucciones de Uso

1. Clona o descarga este repositorio en tu máquina local.
2. Coloca tu archivo de datos en la raíz del proyecto.
3. Ejecuta el script con el siguiente comando:

```bash
python main.py
```


## 📊 Ejemplo de Resultados

Al finalizar la ejecución, el script mostrará en la consola o exportará un resumen con la siguiente estructura:

* **Promedios Mensuales**: `[Año-Mes | Temperatura Promedio]`
* **Máximos Históricos**: `[Estación | Temperatura Máxima | Fecha]`
