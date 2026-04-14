# Expresión diferencial de genes entre diferentes tipos de cáncer de pulmón


## Creación de la carpeta Data y de todas las carpetas que esta contiene:
- Raw_Data, para los datos crudos, incluyendo una carpeta para el control y una para cada tipo de tumor: ADC (adenocarcinoma), SCC (carcinoma epidermoide), LCC (cáncer de pulmón de células grandes) y SCLC (cáncer de pulmón de células pequeñas). Dentro de cada uno hay 4 archivos que se corresponden a las dos lecturas de dos conjuntos de datos. 
- Processed_data, para los datos procesados. Estructura de carpetas igual que la anterior, pero con archivos diferentes, uno que hace referencia al conteo de la expresión genética y otro que normaliza los datos. Además, se incluyen las dos matrices que aúnan todos los datos, antes y después de normalizar.
- Metadata: contiene dos archivos, uno que da información sobre las muestras y otro sobre el proceso experimental.
- External_data: contiene el genoma de referencia y un archivo de anotaciones.
## Creación de la carpeta Scripts y de todas las carpetas que esta contiene:
Esta carpeta contiene los archivos necesarios para llevar a cabo el análisis completo de los datos de expresión génica: desde el procesamiento hasta la generación de resultados. El objetivo es garantizar la reproducibilidad del análisis y permitir reconstruir los resultados obtenidos.
- main: es el archivo principal del proyecto. Actúa como punto de entrada del pipeline y coordina la ejecución de los distintos módulos en el orden adecuado (lectura de datos, preprocesamiento, normalización, análisis diferencial y generación de resultados).
- preprocesamiento: aquí se encuentran los scripts para la limpieza, organización y preparación del raw data. Incluye la lectura de los datos y su manipulación inicial para prepararlos para el análisis. Se hace un control de calidad de los datos para descartar secuencias de baja calidad y eliminar datos duplicados, cómo detectar y corregir posibles errores. Incluye trimming (filtrado) de los datos. El preprocesamiento también incluye el formateo de los datos y la unión de los distintos datasets según el tipo de tumor. Por último, se realiza la identificación de genes altamente variables.
- normalizacion: incluye los scripts dedicados a la normalización de los datos de expresión génica, así como el escalado y la transformación de estos. Esto sirve para hacer comparables las muestras y reducir efectos técnicos.
expresion_diferencial: esta carpeta contiene los scripts para el análisis de expresión diferencial y la comparación entre los distintos tipos de cáncer de pulmón.
- estadistica: aquí se encuentran todos los scripts para el análisis estadístico de los datos. Esta carpeta contiene únicamente el código. Los resultados generados se encuentran en la carpeta “resultados”.
- graficos: al igual que en la carpeta “estadistica”, aquí se incluye únicamente el código necesario para generar las diferentes representaciones gráficas. Los gráficos finales se almacenan en la carpeta “resultados”.
- help_funciones: aquí se incluyen funciones reutilizables, que fueron utilizados en distintas partes del análisis. Ayuda a evitar duplicaciones, reducir posibles errores en el código y mejorar la organización general del proyecto.

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
