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
