## Conclusión:
Se identifica que el Dataset original presentaba importantes problemas en la calidad de datos, ya que se trataba de un Dataset con datos Heredados.

Se pueden mencionar los siguientes inconvenientes encontrados en los datos: diferentes tipos de formatos en la fecha y en la hora, como también valores inválidos; errores en las patentes por su no existencia o con caracteres que fueran difíciles de identificar; también registros incompletos con valores nulos en datos relevantes para la identificación de la multa.

Para poder realizar un análisis estadístico, se realizó una normalización del Dataset:
- Las “fechas” se llevaron todas al formato YYYY-MM-DD y las inválidas a la fecha ‘1932-01-01’.
- Las “horas” se convirtieron al formato de 24hs y a las inválidas se les asignó “’00:00”
- En “patentes” y “ubicación” se convirtieron a mayúsculas quitando caracteres especiales.
- En caso de patentes erróneas se completaron los datos con “No disponible”.
- Se descartaron los registros que no representan infracciones reales según el 5% de tolerancia sobre la velocidad máxima permitida.

A través del análisis estadístico se puede observar patrones de comportamiento de los conductores, como el caso que una patente “WEFLYN” es la que tiene alrededor de 40 multas o que la hora de mayores multas es 00:00hs (caso que se explicará más adelante) seguida por las 09:04 o que el mes de mayor incidencia de multas es Enero.

Sin embargo, se detectó que este análisis estadístico tiene anomalías, ya que la fecha 1932-01-01 (Enero) y la hora 00:00, no necesariamente reflejan un comportamiento real de los conductores, sino que son consecuencia del mismo proceso de limpieza y normalización.

Se puede concluir que el proceso de preparación y limpieza de datos es la etapa crítica que puede alterar la interpretación de los resultados. Si bien el archivo creado a partir de la limpieza y normalización de los datos sería apto para el nuevo sistema, tanto la fecha del 01/01/1932 y la hora 00:00 nos indican una pérdida de información notoria. De todas maneras, se puede identificar quienes son los infractores más frecuentes, sin importar la fecha y la hora de la infracción realizada.
