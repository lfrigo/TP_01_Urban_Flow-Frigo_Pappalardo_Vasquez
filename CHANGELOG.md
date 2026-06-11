## Día 1 - Sprint 3
- Creación de la rama Sprint_3 a partir de Sprint_2.
- Configuración de git y verificación de acceso a los datasets generados.
- Actualización de README.md con el objetivo y contexto del Sprint 3.
## Día 2 - Sprint 3
- Creación del remote local de DVC en /content/remote_dvc.
- Migración de los archivos binarios de git a DVC.
- Subida de los binarios al remote de DVC.
## Día 3 - Sprint 3
- Diseño del modelo lógico de datos basado en el archivo data/processed/speeding_fines_image.csv.
- Identificación y definición de los atributos conceptuales para las entidades: Vehiculo, Multa, Radar y Evidencia.
- Establecimiento de relaciones conceptuales independientes del motor de base de datos (Vehículo-Multa 1:N, Multa-Evidencia 1:1 opcional, Radar-Multa 1:N).
- Definicion de las Clases del modelo lógico.
## Día 4 - Sprint 3
- Implementación de la función `procesar_fila_csv` para la lectura de datos estructurados.
- Mapeo y transformación de registros tipo diccionario provenientes del CSV hacia las Clases lógicas definidas.
- Validamos la función `procesar_fila_csv`.
## Día 5 - Sprint 3
- Diseño del modelo relacional en base al modelo de datos del ejercicio anterior.
- Implementación de los modelos utilizando el ORM de SQLAlchemy.
- Configuración de claves primarias y definición de relaciones entre tablas.
- Sobrescritura del método `__repr__` en cada modelo para mejorar la legibilidad del código.
## Día 6 - Sprint 6
- Configuración de la ruta del Dataset.
- Creación y configuración de la base de datos `transito` utilizando SQLAlchemy.
- Automatización de la creación de tablas a partir de los modelos definidos previamente.
- Mapeo de filas del CSV a objetos del dominio (procesar_fila_csv).
- Migración de los datos desde el CSV y validación de registros insertados.
- Versionado de la base de datos relacional con DVC.
## Día 7 - Sprint 3
- Consultas sobre la base de datos transito con el ORM de SQLAlchemy:
  top 10 patentes, multas sin evidencia, radares más activos,
  reincidentes por período y porcentaje de confirmación visual.
