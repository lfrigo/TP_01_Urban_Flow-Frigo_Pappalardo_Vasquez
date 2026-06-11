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
## Día 8 - Sprint 3
- Creación de la base de datos vectorial patente_vectorial con ChromaDB y OpenCLIP.
- Almacenamiento del id del vehículo junto al vector de su imagen.
- Desarrollo del script de búsqueda por aproximación (búsqueda vectorial) para la identificación de vehículos.
- Versionado de la base vectorial con DVC.
## Día 9 - Sprint 3
- Implementación de la función principal `buscar_patente_imagen`.
- Configuración de la función para procesar una imagen de entrada, generar su vector de características y realizar la búsqueda por aproximación en la base vectorial.
- Integración de la consulta con la base de datos relacional para recuperar y retornar la totalidad de los datos del vehículo identificado.
## Día 10 - Sprint 3
- Redacción de la conclusión y análisis del proyecto integrador.
- Análisis del trabajo desarrollado, destacando la sinergia entre bases de datos relacionales y vectoriales.
- Evaluación del impacto del ORM SQLAlchemy, BD Vectorial ChromaDB y los modelos de Embeddings (OpenClip) en la resolución de problemas de analítica y reconocimiento visual de tránsito.
