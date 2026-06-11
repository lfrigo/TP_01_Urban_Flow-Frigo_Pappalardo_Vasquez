
# Sprint 1
## Objetivo
Aplicar los conocimientos adquiridos para el versionado de código, la organización, limpieza del código y la utilización de pandas.

## Contexto
La localidad llamada Vaalserberg de Bélgica se encuentra en la zona fronteriza y limita con los paises de Países Bajos y Alemania. Esta localidad cuenta con un sistema de radares urbanos para la detección de infracciones por exceso de velocidad. Los registros históricos provienen de sistemas heredados, el cuál presenta errores de formato, faltante de datos generando registros inconsistentes en el nuevo sistema.

## Introducción
Debemos analizar y depurar los datos de los sistemas heredados, para obtener información relevante sobre las infracciones y de está forma en el futuro poder incorporarlos al nuevo sistema sin inconsistencias.

## Dataset
El dataset contiene información histórica de multas por exceso de velocidad y presenta errores que deberán ser tratados para evitar inconsistencias.
[Dataset Urban Flow](https://raw.githubusercontent.com/HAD141/datasets/refs/heads/main/TrabajosPracticos/urban_flow/speeding_fines.csv)

# Sprint 2
## Objetivo
El objetivo principal de este sprint es aplicar los conocimientos adquiridos en el tratamiento y verificación de imágenes, la programación limpia y estructurada, y la integración de herramientas de versionado de datos.

## Contexto
Los radares urbanos de la localidad de Vaalserberg generan registros administrativos de multas de forma automática,
y las cámaras asociadas registran la evidencia visual que acompaña y valida cada infracción.
Sin embargo, los datos provenientes de sistemas heredados e integraciones técnicas plantean desafíos específicos:
* No todas las multas tienen una imagen asociada.
* No todas las imágenes corresponden realmente a una infracción.
* Pueden existir errores automáticos en la detección de caracteres.

## Introducción
El trabajo actual consiste en desarrollar un sistema que determine de manera automatizada qué multas disponen de una evidencia visual válida.
Para ello, se clasifican las imágenes según sus resoluciones en grupos de capturas completas ("completes")
y recortes de patentes ("plates"), y se realiza un proceso de lectura de caracteres mediante OCR para contrastar
la patente detectada visualmente contra los registros depurados en el Sprint 1.

## Dataset
Para este sprint se integran y complementan dos fuentes de información fundamentales:
1. **Dataset procesado en el Sprint 1:** Contiene el histórico de infracciones por exceso de velocidad depurado de inconsistencias administrativas.
2. **Dataset de imágenes:** Compuesto por los archivos fotográficos de evidencia capturados por los radares.

* [Dataset de imágenes de patentes](https://github.com/HAD141/datasets/raw/refs/heads/main/TrabajosPracticos/urban_flow/urban_flow_plates.zip)

# Sprint 3
## Objetivo
Aplicar los conocimientos adquiridos, versionando los datos según su tipo. Se
migra la información procesada a una base de datos relacional (SQLAlchemy) y se
vincula con una base de datos vectorial (ChromaDB + OpenCLIP).

## Introducción y contexto
Con el avance de los Sprint, se puede inferir que ya no es viable trabajar
únicamente con archivos CSV. En este sprint, se incorpora como solución la
utilización de base de datos relacional, ORM mediante SQLAlchemy, control de
versiones de datos con DVC y la preparación para búsquedas avanzadas por imagen.
