
## Conclusión - Sprint 3
En este sprint se profesionalizó la solución migrando los datos procesados a
una base de datos relacional gestionada con el ORM de SQLAlchemy. Se diseñó un
modelo lógico de dominio (Vehiculo, Multa, Radar y Evidencia) y su modelo
relacional correspondiente, respetando las relaciones uno a muchos entre
vehículo/radar y multas, y la relación opcional uno a uno entre multa y
evidencia.

Sobre esa base se implementaron consultas que responden preguntas de negocio
(patentes más multadas, radares más activos, reincidencia por período y
porcentaje de confirmación visual). Además, se integró una base de datos
vectorial (ChromaDB con OpenCLIP) que permite identificar un vehículo a partir
de la imagen de su patente por similitud, vinculando así el dato visual con el
dato estructurado.

Finalmente, se incorporó el versionado de datos con DVC, separando los archivos
binarios (gráficos y bases de datos) del control de versiones de git, lo que
deja el proyecto preparado para escalar en volumen y para búsquedas avanzadas.
