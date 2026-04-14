# Expresión diferencial de genes entre diferentes tipos de cáncer de pulmón


## Creación de la carpeta Data y de todas las carpetas que esta contiene:
- Raw_Data, para los datos crudos, incluyendo una carpeta para el control y una para cada tipo de tumor: ADC (adenocarcinoma), SCC (carcinoma epidermoide), LCC (cáncer de pulmón de células grandes) y SCLC (cáncer de pulmón de células pequeñas). Dentro de cada uno hay 4 archivos que se corresponden a las dos lecturas de dos conjuntos de datos. 
- Processed_data, para los datos procesados. Estructura de carpetas igual que la anterior, pero con archivos diferentes, uno que hace referencia al conteo de la expresión genética y otro que normaliza los datos. Además, se incluyen las dos matrices que aúnan todos los datos, antes y después de normalizar.
- Metadata: contiene dos archivos, uno que da información sobre las muestras y otro sobre el proceso experimental.
- External_data: contiene el genoma de referencia y un archivo de anotaciones.
## Creación de la carpeta Resultados y de todas las carpetas que esta contiene:
Esta carpeta contendrá todos los análisis de los datos obtenidos y almacenados en la carpeta **Data**. Su objetivo es organizar los resultados en diferentes niveles, facilitando la trazabilidad y la interpretación del estudio.
### Tablas
Esta carpeta contiene los datos organizados de forma tabular tras el preprocesamiento. Incluye: matrices de expresión génica, tablas con las muestras clasificadas según el tipo tumoral y los datos preparado para el posterior análisis estadístico.
Representan la base del análisis ya que permiten trabajar con los datos de forma ordenada, asegurando una correcta clasificación.
### Estadístico
Contiene los resultados de los análisis estadísticos, como por ejemplo: p-value de comparaciones entre grupos, valores ajustados, expresión media, variabilidad de grupo, etc. 
Permite evaluar de forma significativa las diferencias observadas en la expresión de los diferentes genes en los diferentes tipos de cáncer del estudio, asegurando asíi que los resultados no son debidos al azar.
### Comparación
Contiene los resultados de las comparaciones entre los diferentes tipos tumorales. incluye: análisis entre pares de grupos y resúmenes de genes con los cambios más relevantes.
Permite analizar contrastes directos e identificar diferencias moleculares entre los tipos de cancer. 
### Finales
Contiene los resultados finales tras filtrado, validación e integración de los resultados anteriores. 
Incluye lista definitiva de los genes con expresión diferencial, resultados depurados y relevantes; además de tablas finales para su inlusión en informes o artículos para publicación.
En esta sección se recogen únicamente los resultados más relevantes y significativos para la correcta interpretación biológica. 
