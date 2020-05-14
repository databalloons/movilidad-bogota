# movilidad-bogota


### Configuración de entorno de desarrollo
Para poder ejecutar el código es necesario instalar Python (>=3.6) y las siguientes dependencias:
* `geopandas`
* `notebook` (Jupyter Notebook)
* `numpy`
* `pandas`

La manera más sencilla de realizar esta instalación es a través de Conda. Para esto descargue [Miniconda][1] o [Anaconda][2]. [Acá][3] puede encontrar más información sobre la diferencia entre estas y una guía detallada sobre su intalación.

Una vez tenga instalado Conda en su equipo, vaya a la raíz de este proyecto en una terminal y ejecute el siguiente comando para crear un entorno con las dependencias necesarias:

```
conda env create -f environment.yml
```

Una vez creado el entorno `movilidad-bogota`, actívelo ejecutando:

```
conda activate movilidad-bogota
```

Para abrir Jupyter Notebook utilizando el intérprete de Python recién instalado ejecute:

```
jupyter notebook
```

### Descarga de datos
Los links de descarga de los datos originales utilizados en este proyecto se encuentran en la sección **Fuentes de datos**. Sin embargo, una carpeta con todos los datos (de los cuales algunos han sido reestructurados para disminuir espacio de almacenamiento y cumplir con los fines del proyecto) está disponible [acá][4] para su descarga de forma manual. También es posible descargar esta carpeta desde una terminal ejecutando el siguiente comando (desde la raíz del proyecto):

```
curl -L -o {/path_project}/datos.zip "https://drive.google.com/uc?export=download&id=1He-R_menD5nHA-IQXx7jrhIIi-biFhA9"
```

Asegurese que una vez descargados los datos, la estructura de las carpetas del proyecto sea la siguiente:

```
.
├── data
│   └── csv
│       └── ...
│   └── shp
│       └── ...
└── **notebooks**
    └── ...
```

### Fuentes de datos
* csv
    - ViajesEODH_2019<sup>1</sup>
* shp
    - ManzanaEstratificacion<sup>2</sup>
    - ManzanaUsoSuelo<sup>3</sup>
    - ZAT<sup>1</sup>


<sup>1</sup> [Prudencia Bogotá - Encuestas de movilidad][5]

<sup>2</sup> [Ideca - Manzana Estratificación Bogotá D.C.][6]

<sup>3</sup> [Ideca - Usos por manzana Bogotá D.C.][7]




[1]: https://docs.conda.io/en/latest/miniconda.html
[2]: https://www.anaconda.com/products/individual
[3]: https://docs.conda.io/projects/conda/en/latest/user-guide/install/download.html
[4]: https://drive.google.com/open?id=1QLCakladzBUmSZAg6qA5UQ9u8e0pjRiz
[5]: https://www.simur.gov.co/portal-simur/datos-del-sector/encuestas-de-movilidad/
[6]: https://www.ideca.gov.co/recursos/mapas/manzana-estratificacion-bogota-dc
[7]: https://www.ideca.gov.co/recursos/mapas/usos-por-manzana-bogota-dc
