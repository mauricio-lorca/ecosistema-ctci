# Estructura - Relaciones entre actores

En esta carpeta, se encuentra el código y los datos empleados para el análisis de relaciones entre actores del ecosistema, tomando como base las colaboraciones en proyectos financiados por ANID y CORFO.

## Fuentes

- Los datos de ANID fueron extraídos desde el [repositorio GitHub de ANID de Colaboración Institucional](https://github.com/ANID-GITHUB/Colaboracion_Institucional)

- Los datos de CORFO fueron solicitados vía Ley de Transparencia, pero toman como base lo ya disponibilizado en [DataInnovación](https://datainnovacion.cl/). Así, los datos solicitados vía Ley de Transparencia enriquecen dicha base de datos con información sobre las colaboraciones; es decir, qué instituciones formaron parte en cada proyecto.

- Los datos necesarios para caracterizar las instituciones fueron extraídos desde fuentes abiertas de internet: [PortalChile](https://www.portalchile.org/) y [Registro19862](https://www.registros19862.cl/).

## Estructura

Se presentan tres subdirectorios:

1. **Datos**: Contiene los datos principales empleados en este análisis, tanto de ANID (desde el repositorio GitHub( y CORFO (DataInnovación y solicitud vía Ley de Transparencia).

2. **Resultados**: Contiene los archivos con resultados obtenidos. Varios de los archivos son bases de datos intermedias, pero pueden resultar de interés los archivos `data_anid_final.xlsx` y `data_corfo_final.xlsx`. Estos archivos son las bases de datos finales, sobre las cuales se realizó el análisis de redes: cada uno de estos archivos ha sido limpiado y enriquecido mediante un proceso semiautomático. De esta forma, en cada fila (que corresponde a una institución participante de un proyecto, ya sea de ANID o CORFO) se buscó incluir información que caracteriza a la institución, como el tipo de institución (Institución Privada Sin Fines de Lucro, Estado, Internacional, Institución de Educación Superior, Empresa) y un nombre "canónico"; es decir, un nombre limpio y estandarizado, obtenido al hacer el cruce con el RUT. Se debe mencionar, de todas formas, que al utilizar el nombre canónico se puede perder información: así, por ejemplo, centros de investigación que funcionan bajo el RUT de una universidad, tendrán como nombre canónico el nombre de dicha universidad y no el nombre del centro.

3. **Notebooks**: Contiene los códigos utilizados tanto para la creación de las bases de datos como para el análisis de redes. Estos archivos están en formato `.ipynb` correspondiente a notebooks de Python; aun más, estos notebooks fueron ejecutados en la plataforma de Google Colab, por lo cual muchas de las rutas hacen referencia a unidades compartidas en dicha plataforma. Es menester destacar que, si bien los archivos fueron limpiados, comentados y ordenados, aún asi este código debe ser entendido de manera primordialmente referencial: no son _scripts_ para ejecutar y replicar instantáneamente el análisis, sino que son archivos que muestran el proceso llevado a cabo, con los problemas que fueron apareciendo y cómo estos se fueron subsanando. Así, pueden ser utilizados como referencia para llevar a cabo un análisis análogo con bases de datos similares (o más recientes), pero no como un software que tomará un _input_ y entregará un _output_ listo para ser empleado.
