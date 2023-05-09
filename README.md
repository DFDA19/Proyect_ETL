#ETL de gatos#

Este proyecto consiste en la extracción, transformación y carga de datos de diferentes sitios web relacionados con gatos. El objetivo es obtener información sobre diferentes razas de gatos y almacenarla en una tabla en una base de datos SQL.

Extracción
Se han utilizado diferentes técnicas de scraping para extraer información sobre razas de gatos de los siguientes sitios web:

Links del web scrapping primera fuente

'https://www.expertoanimal.com/razas-de-gatos.html'

'https://www.expertoanimal.com/razas-de-gatos_2.html'

links segunda fuente

'https://www.purina.com/cats/cat-breeds/chartreux'

https://www.purina.com/cats/cat-breeds/cornish-rex

https://www.purina.com/cats/cat-breeds/european-burmese

https://www.purina.com/cats/cat-breeds/japanese-bobtail

https://www.purina.com/cats/cat-breeds/havana-brown

https://www.purina.com/cats/cat-breeds/korat

https://www.purina.com/cats/cat-breeds/laperm

https://www.purina.com/cats/cat-breeds/ocicat

https://www.purina.com/cats/cat-breeds/peterbald

https://www.purina.com/cats/cat-breeds/pixiebob

https://www.purina.com/cats/cat-breeds/ragamuffin

https://www.purina.com/cats/cat-breeds/selkirk-rex

https://www.purina.com/cats/cat-breeds/singapura

https://www.purina.com/cats/cat-breeds/somali

https://www.purina.com/cats/cat-breeds/tonkinese

https://www.purina.com/breeds/toyger-cat-breed

https://www.purina.com/cats/cat-breeds/turkish-van

##La información extraída se compone de los siguientes campos:##

#breed: nombre de la raza del gato
#short_descr: descripción breve de la raza
#href: URL a la página con información detallada sobre la raza
#img_url: URL de la imagen de la raza

##Transformación##
Una vez que se han extraído los datos de los diferentes sitios web, se han combinado en un único DataFrame utilizando Python y la librería Pandas. Se han eliminado las filas duplicadas y se han limpiado los campos.

##Carga##
Finalmente, se ha cargado el DataFrame en una tabla de una base de datos MySQL utilizando la librería mysql-connector-python de Python. La tabla se ha creado previamente en la base de datos y se ha definido su estructura.

##Configuración##
Para poder ejecutar el código es necesario tener instalado Python 3 y las siguientes librerías de Python:

pandas
mysql-connector-python

Además, se deben configurar las variables de conexión a la base de datos MySQL en el archivo config.py.

##Ejecución##
Para ejecutar el ETL se debe correr el archivo main.py. El código extraerá la información de los diferentes sitios web, la combinará en un único DataFrame, limpiará y transformará los datos y finalmente cargará el DataFrame en la tabla de la base de datos MySQL.

Se recomienda ejecutar el ETL periódicamente para actualizar los datos en la tabla de la base de datos.