
# PROYECTO INDIVIDUAL ML OPS 

![imagen_portada](https://github.com/DavidssonGon/PI_ML_OPS_STEAM_DSFT17/blob/main/steam.png)

## Introducción 

En este repositorio se encuentra el proceso de la realización de un proyecto de ciencia de datos en diferentes etapas, así que procederé a introducirme. Soy Davidsson Gonzalez y actualemente me encuentro cursando la carrera Data Science en modalidad Full Time en la academia Soy Henry. 

Lo que se nos plantea es ponernos en los zapatos de un Data Scientist en una gran compañía en la industria de los video juegos, en este caso STEAM, donde en nuestros primeros días de trabajo se nos pide solucionar un problema de negocio el cual consiste en crear un sistema de recomendación de video juegos para los usuarios finales, esta es la idea general del fin que busca el proyecto. 

## Procesos 

El objetivo que se nos define con el requerimiento general se define en un MVP (Minimum Viable Product) para llegar a esto se tendrá que cumplir con varios puntos importantes. 

El primero seria las transformaciones o mejor descrito como ETL donde se tendrá que cargar los datos que se nos proporciona, interpretarlos y empezar a tomar decisiones para sus trasformaciones ya que lo que se busca con este proceso principalmente es ir limpiando los datos de la información que no se considera necesaria para llegar a los objetivos. 

Dentro de esta primera etapa entra un primer punto importante a destacar y es lo que se denomina como **“Feature Engineering”** ya que en el Data Set dataset user_reviews se incluyen reseñas de juegos hechas por distintos usuarios, en base a estas reseñas se crea un nuevo campo que tendrá el nombre de “sentiment_analysis” y en el cual por medio de un proceso de NLP (Natural Language Processing) se le asigna un valor numérico dependiendo de si la reseña es negativa, neutra o positiva. Hasta este punto se puede confluir una etapa inicial de ETL ya que en este proyecto se implementaron procesos de ETL en más de una etapa. 

Una vez se tenían unos datos más limpios y de mayor calidad se empieza el proceso de Análisis de datos exploratorios o EDA, en esta ocasión se buscó principalmente identificar los datos atípicos, las frecuencias y graficar las tendencias ya que no se contaba con muchas variables numéricas, sino que en su mayoría eran categóricas incluso algunas que se componían de números como los años. Esta parte fue sumamente importante no solo para enriquecerse en el conocimiento que aportan los datos en su conjunto, sino que esclarece la necesidad de seguir limpiando los datos para los procesos posteriores además de las relaciones que los diferentes Data Sets podrían tener. 

La siguiente etapa yo la denomine ETL2 por que en esta, aunque ya se tienen unos datos más tratables decido realizar procesos específicos para responder a las necesidades que van a tener las funciones de consulta que siguen, así pues más allá de eliminar unos pocos outliers lo interesante estuvo en hacer la relaciones entre los diferentes Data Sets ya que en este proceso se perdían cierta cantidad de filas pero al realizar diferentes filtrados para llegar a un Data Set que respondiera a una consulta especifica se garantiza una mayor performance en la consulta en cuanto al consumo de recursos y no se tendría que estar adaptando la consulta al Data Set sino que se realizaría una consulta adaptada a cada Data Set. 

Lo que parecía el proceso más demandante para el objetivo del MVP se pudo sortear de una manera más directa gracias a que ya se tenía casi listo el Data Set para cada consulta donde cada una haría simplemente un proceso de filtrado a partir de un parámetro ya definido en los requerimientos, lo cual hizo este proceso un poco más guiado en lo que se quería específicamente para poder cumplirlo. 

Pero la gran excepción a lo anterior seria la función que requeriría un proceso de ML (Machine Learning) basado en un proceso llamado **“la similitud del coseno”** el cual es muy usado para proceso de comparar textos, en este caso sería necesario para un sistema de recomendación de juegos. La complicación en este punto se encontró en que mi Data Set contenía una cantidad de géneros así que después de probar varias cosas para reducir el tamaño que me representaba esa cantidad de géneros para el proceso lo que hice fue tomar solamente los 50 géneros más frecuentes en los datos por lo cual este proceso causo también en que se redujeran las filas pero al final se pudo implementar una función que entregaba muy bueno resultados y en especial haciéndolo  de una manera rápida y sin consumir muchos recursos. 

Para este punto que ya se estaba entrando en el proceso de **“Deployment”** decidí implementar la función de ML por fuera del deployment para generar así un Data Set especifico donde ya está la relación del input con la respuesta de esa función. Esta idea ayuda a ilustrar el camino que tome para implementar la API pues cree un archivo a parte donde están las funciones que realice y luego las llamo desde el archivo **“main.py”**, pues aparte de que es un proceso que hace ver el código más ordena facilita el hecho de tener diferentes Data Sets cada uno para cada función. 

El proceso del deployment se me complico al principio primero con la instalación de las librerías en la máquina virtual, pero después al momento de ejecutar los commits desde render.com pues el tema de los **“requeriments”** me daba problemas con las versiones de cada librería así que opte por dejar solo las 4 librerías que podía necesitar y no especificar versiones, de esta manera ya podía tener mi API funcionando. 

## Conclusión 

Gracias a este proyecto y su intensidad junto con lo que implicaba ilustra bastante como podría ser tener un cargo de tal responsabilidad en una empresa, pero además en la parte técnica ayuda a interiorizar los conceptos generales junto con las técnicas específicas y procesos necesarios para solucionar los problemas que se le exigen a un científico de datos. 

Los procesos con respecto a los datos van cogiendo forma y aunque la manera como se trataron en este proyecto parecía estar un poco ya que siempre se le estaban haciendo algo a estos recae con mucho sentido al entender la idea general de la transversalidad de este MVP en cuanto a diferentes perfiles de la ciencia de datos, lo más importante a destacar me parece es la implementación de la API en la web gracias render ya que destaca todo este proyecto por su funcionalidad y puesta en marcha.

### Instancias del proyecto

El proyecto se puede analizar en este orden: 

- [ETL](https://github.com/DavidssonGon/PI_ML_OPS_STEAM_DSFT17/blob/main/ETL.ipynb)
- [EDA](https://github.com/DavidssonGon/PI_ML_OPS_STEAM_DSFT17/blob/main/EDA.ipynb)
- [ETL2](https://github.com/DavidssonGon/PI_ML_OPS_STEAM_DSFT17/blob/main/ETL2.ipynb)
- [Funciones_consulta](https://github.com/DavidssonGon/PI_ML_OPS_STEAM_DSFT17/blob/main/Funciones_consulta.ipynb)

Deployment de la API:

- [Repositorio](https://github.com/DavidssonGon/PI_ML_OPS_API)
- [API funcionando](https://consultas-db-steam.onrender.com/)

Video:
- [Link](https://drive.google.com/file/d/1O0JXnJU83pY3ZnwriXfyqKwPVVlBg7di/view?usp=drive_link)

---