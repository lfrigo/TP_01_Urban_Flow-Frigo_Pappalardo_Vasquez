## Conclusión - Sprint 2

### Relación entre imágenes y datos

El Sprint 2 nos permitió integrar la evidencia visual (imágenes de
patentes y de vehículos completos) con los registros depurados en
el Sprint 1 del sistema heredado. A continuación se resumen las observaciones
principales de este proceso.

### Resultados obtenidos

A partir del dataset de 110 imágenes (89 recortes de patente y 19
fotos completas) y un dataset de 1713 multas, se obtuvieron los
siguientes resultados:

- **662** multas con imagen relacionada.
- **1051** multas sin imagen relacionada.
- **80** imágenes que no lograron asociarse a ninguna multa.
- **430** multas con estado `IMPAGA`.
- **157** multas pendientes de pago que cuentan con su imágen.

### Observaciones

#### Sobre las imágenes
- La calidad y resolución de las imágenes es variable. Algunos
  recortes de patentes están desenfocados, mal encuadrados o con
  poca iluminación, lo que impacta directamente en el desempeño del
  OCR y en el reconocimiento de las mismas.
- No todas las imágenes corresponden necesariamente a una infracción
  registrada, y eso explica que queden imágenes sin match.

#### Sobre el OCR (EasyOCR)
- El OCR no es 100% preciso. Confunde frecuentemente caracteres
  visualmente similares como `0`-`O`, `1`-`I`-`L`, `5`-`S` y
  `8`-`B`. En la salida del ejercicio 4 se ven casos como
  `BP717` detectado como `BP*717`, o `HF58HXP` como `HF5B HXP`.
- En algunas imágenes el OCR captura caracteres adicionales
  (corchetes, dos puntos, comas, guiones) propios del fondo o de la
  chapa, por ejemplo `BHRP770` detectado como `[BHRP: 770|`.
- Por eso fue necesario normalizar las cadenas y usar un ratio de similitud
  antes de comparar.

#### Sobre el matcheo
- Se utilizó `SequenceMatcher` de `difflib` con un umbral del 80%.
- El cruce muestra que una porción significativa de las multas no tiene
  evidencia visual asociada, lo que afecta la capacidad de validación para esos
  casos.

### Conclusión

La integración de datos administrativos con la evidencia visual, aporta
una capa adicional de validación a las infracciones, pero no la
garantiza por completo. La calidad del cruce depende de tres
factores combinados: la calidad de las imágenes, la precisión del
OCR y el umbral de similitud elegido.

En síntesis, el Sprint 2 confirma que datos e imágenes se
complementan pero ninguno de los dos por sí
solo es suficiente para asegurar la validez de la multa.
## Conclusión - Sprint 2

### Relación entre imágenes y datos

El Sprint 2 nos permitió integrar la evidencia visual (imágenes de
patentes y de vehículos completos) con los registros depurados en
el Sprint 1 del sistema heredado. A continuación se resumen las observaciones
principales de este proceso.

### Resultados obtenidos

A partir del dataset de 110 imágenes (89 recortes de patente y 19
fotos completas) y un dataset de 1713 multas, se obtuvieron los
siguientes resultados:

- **662** multas con imagen relacionada.
- **1051** multas sin imagen relacionada.
- **80** imágenes que no lograron asociarse a ninguna multa.
- **430** multas con estado `IMPAGA`.
- **157** multas pendientes de pago que cuentan con su imágen.

### Observaciones

#### Sobre las imágenes
- La calidad y resolución de las imágenes es variable. Algunos
  recortes de patentes están desenfocados, mal encuadrados o con
  poca iluminación, lo que impacta directamente en el desempeño del
  OCR y en el reconocimiento de las mismas.
- No todas las imágenes corresponden necesariamente a una infracción
  registrada, y eso explica que queden imágenes sin match.

#### Sobre el OCR (EasyOCR)
- El OCR no es 100% preciso. Confunde frecuentemente caracteres
  visualmente similares como `0`-`O`, `1`-`I`-`L`, `5`-`S` y
  `8`-`B`. En la salida del ejercicio 4 se ven casos como
  `BP717` detectado como `BP*717`, o `HF58HXP` como `HF5B HXP`.
- En algunas imágenes el OCR captura caracteres adicionales
  (corchetes, dos puntos, comas, guiones) propios del fondo o de la
  chapa, por ejemplo `BHRP770` detectado como `[BHRP: 770|`.
- Por eso fue necesario normalizar las cadenas y usar un ratio de similitud
  antes de comparar.

#### Sobre el matcheo
- Se utilizó `SequenceMatcher` de `difflib` con un umbral del 80%.
- El cruce muestra que una porción significativa de las multas no tiene
  evidencia visual asociada, lo que afecta la capacidad de validación para esos
  casos.

### Conclusión

La integración de datos administrativos con la evidencia visual, aporta
una capa adicional de validación a las infracciones, pero no la
garantiza por completo. La calidad del cruce depende de tres
factores combinados: la calidad de las imágenes, la precisión del
OCR y el umbral de similitud elegido.

En síntesis, el Sprint 2 confirma que datos e imágenes se
complementan pero ninguno de los dos por sí
solo es suficiente para asegurar la validez de la multa.
