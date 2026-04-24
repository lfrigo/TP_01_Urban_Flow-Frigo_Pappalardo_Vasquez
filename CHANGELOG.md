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
