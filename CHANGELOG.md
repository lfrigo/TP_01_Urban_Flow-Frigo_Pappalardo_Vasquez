# CHANGELOG

## Día 1 - Inicialización y configuración del entorno
- Clonado del repositorio desde la rama `Sprint_1`.
- Creación de la rama `Sprint_2` a partir de `Sprint_1`.
- Configuración de credenciales de Git mediante secrets de Colab
  (`github_token`, `USER_NAME`, `USER_EMAIL`).
- Variable `desactivar_git_push` para controlar los `git push`.
- Variable `ejecuta_primera_vez` para controlar la creación inicial
  de la rama y la inicialización de DVC.
- Instalación e inicialización de **DVC** para versionado del dataset de imágenes.
- Descarga, descompresión y almacenamiento del dataset de imágenes
  en `urban_flow/data/raw/imgs`.
# CHANGELOG

## Día 2 - Exploración del dataset de imágenes
- Creación de función `leer_imagen` para cargar imágenes en formato
  JPG/PNG/JP2.
- Observamos todas las imágenes disponibles con nombre y tamaño en KB.
- Separación de las imágenes en dos grupos: `plates` (recortes de
  patente) y `completes` (foto completa del vehículo).
- Cálculo de la resolución promedio del dataset.
- Creación de Diccionario `group_images` con campos `filename`, `width`, `height`, `area`, `path` y `patent`.
- Función reutilizable `mostrar_imagenes` que muestra
  8 imágenes aleatorias.
