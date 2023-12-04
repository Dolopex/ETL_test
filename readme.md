# Proyecto ETL

Este proyecto realiza la extracción, transformación y carga (ETL) de datos demográficos de ciudades de Estados Unidos y también obtiene información de calidad del aire para esas ciudades.

## Instalación

1. Clona el repositorio:

   ```bash
   git clone https://github.com/Dolopex/ETL_test.git

## Instala las dependencias

pip install -r requirements.txt

## Estructura del Proyecto

Este proyecto realiza la extracción, transformación y carga (ETL) de datos demográficos de ciudades de Estados Unidos y también obtiene información de calidad del aire para esas ciudades.

## Funcionalidades

### 1. Extracción de Datos Demográficos

El archivo `solucion.py` contiene la función `ej_1_cargar_datos_demograficos()`. Esta función realiza las siguientes acciones:

- Descarga datos demográficos de ciudades de Estados Unidos desde [OpenDataSoft](https://public.opendatasoft.com/).
- Realiza una limpieza de los datos eliminando columnas innecesarias y duplicados.
- Crea una base de datos SQLite llamada `datos_demograficos.db`.
- Guarda los datos demográficos en la tabla `demografia` de la base de datos.

### 2. Obtención de Calidad del Aire

El archivo `solucion.py` también contiene la función `ej_2_cargar_calidad_aire(ciudades: Set[str], api_key: str) -> None`. Esta función realiza lo siguiente:

- Toma un conjunto de nombres de ciudades y una clave de API como entrada.
- Realiza llamadas a la [API de Calidad del Aire](https://api.api-ninjas.com/v1/airquality) para cada ciudad utilizando las coordenadas de la ciudad o el nombre de la ciudad.
- Recopila datos sobre la concentración de varios contaminantes y el Índice de Calidad del Aire (AQI) para cada ciudad.
- Guarda la información recopilada en un archivo CSV llamado `ciudades.csv`.

## Configuración y Uso

Antes de ejecutar el proyecto, asegúrate de tener configurada tu API Key en el archivo `solucion.py`:

```python

API_KEY = 'c4jyajWdg1MNjhWvkOyKWg==eJZf9POEDAim3REl'

## Contribuciones
¡Contribuciones son bienvenidas! Si encuentras algún error o tienes sugerencias, por favor abre un problema o envía un pull request.