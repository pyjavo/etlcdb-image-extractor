# Notas sobre etlcdb-image-extractor

Hace uso de esta herramienta https://github.com/choo/fsutils/blob/master/fsutils.py

pero no me confío en lo que contenga el egg, por lo que copio y pego el código acá mismo en el proyecto


## Instalación
ModuleNotFoundError: No module named 'yaml'
-----pip install pyyaml

ERROR: No matching distribution found for fsutils-1-0-0 (unavailable)
------fsutils==1.1.3

Couldn't install Pillow==6.2.0
------Pillow==8.4.0



fsutils==1.1.3
msgpack==1.0.2
Pillow==8.4.0
PyYAML==6.0


## notas

-En la carpeta de /etlcdb-image-extractor/etl_data/images/ETL9G los hiraganas están desde 0x3042 hasta 0x3093'

- Segun http://etlcdb.db.aist.go.jp/specification-of-etl-9

```
ETL9B_1 contiene los hiragana
record index (dummy record as 0)= 1
metadata and JIS code in hex = (1, 9250, ‘A.HI’) 0x2422


extracted 12144 images from file ./etl_data/ETL9G/ETL9G_01.
completed! extracted 12144 images.
```


- Segun http://etlcdb.db.aist.go.jp/specification-of-etl-8


```
pendiente de analizar ...
```


## Correr


Luego de descargar el dataset se lleva a la carpeta /etl_data/. Por ejemplo: `/etl_data/ETL8G`

Luego se corre con el comando
```
python etl_extractor.py
```

Y esto imprime
```
extraction of data set "ETL1" start.
Dataset ETL1 does not exist, so skip extracting this dataset
extraction of data set "ETL2" start.
Dataset ETL2 does not exist, so skip extracting this dataset
extraction of data set "ETL3" start.
Dataset ETL3 does not exist, so skip extracting this dataset
extraction of data set "ETL4" start.
Dataset ETL4 does not exist, so skip extracting this dataset
extraction of data set "ETL5" start.
Dataset ETL5 does not exist, so skip extracting this dataset
extraction of data set "ETL6" start.
Dataset ETL6 does not exist, so skip extracting this dataset
extraction of data set "ETL7" start.
Dataset ETL7 does not exist, so skip extracting this dataset
extraction of data set "ETL8G" start.
extracted 4780 images from file ./etl_data/ETL8G/ETL8G_01.
completed! extracted 4780 images.
******************************* 


.....


extracted 153916 images from file ./etl_data/ETL8G/ETL8G_33.
completed! extracted 153916 images.
******************************* 

extraction of data set "ETL9G" start.
Dataset ETL9G does not exist, so skip extracting this dataset
```

Al final se revisa en /etl_data/images/ETL8G/ las imágenes generadas



