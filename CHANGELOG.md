# CHANGELOG

## Día 1
- Creación del Repositorio en rama main. Creación de la rama Sprint_1. Modificación de la rama default a Sprint_1.
- Otorgar permisos de colaboradores a los integrantes del grupo.
- Configuración de la variable desactivar_git_push.
- Configuración de git en el proyecto local.
- Creación de la estructura de directorios.
- Modificación de README.md.
- Creación de CHANGELOG.md.
## Día 2
- Descarga del dataset speeding_fines.csv y copia en directorio urban_flow/data/raw.
- Análisis de los datos del dataset: head, dtypes, info y isnull.
## Día 3
- Normalización de fechas y horas.
- Normalización de ubicaciones.
- Normalización de patentes completando errores con pd.NA
- Eliminar filas que posean valores relevantes para las multas y que se encuentren vacios.
- Detectar y eliminar los outliers.
- Crear la columna exceso_velocidad_real y calcularla.
- Crear la columna exceso_velocidad y calcularla.
- Eliminar las filas que no cometieron infracciones según el exceso de velocidad.
- Guardar el dataset limpio en urban_flow/data/interim/speeding_fines.csv
## Día 4

- Control del dataset antes de comenzar a analizarlo. Para evitar errores al momento de usar la clase FineAnalyzer.
- Revisar que estén las columnas a analizar, que no haya nulos y los tipos de datos.
- El DataFrame utilizado es el que se ha normalizado y limpiado en los puntos anteriores
- Se define la clase FineAnalyzer y se encapsula para evitar acceso externos
- Se crean siguientes métodos y se invocan cada uno de ellos para el análisis de datos
    - Ranking de las patentes más multadas (top 5). Debe retornar un DataFrame ordenado de mayor a menor y el índice debe comenzar desde 1, con las columnas de patentes y cantidad..
    - Ranking de los horarios donde se producen más multas (top 5). Debe retornar un DataFrame ordenado de mayor a menor y el índice debe comenzar desde 1, con las columnas de hora y cantidad.
    - Exceso promedio de velocidad. Debe retorna un flotante.
    - Exceso real promedio de velocidad . Debe retorna un flotante.
    - Contabilizar la cantidad de multas por cada ubicación. Debe retornar un DataFrame ordenado por ubicación mostrando la ubicación y la cantidad.
