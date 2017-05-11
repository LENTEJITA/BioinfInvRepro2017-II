# Unidad 7: Análisis de genética de poblaciones y filogenias

## 7.1. Bioconductor y paquetes bioinformáticos en R

Los paquetes son un grupo de funciones que alguien desarrolla en torno a un tema específico. CRAN alberga muchos paquetes de R, algunos de ellos útiles para bioinformática, como [adegenet](http://adegenet.r-forge.r-project.org/) y [ape](https://cran.r-project.org/web/packages/ape/ape.pdf). Puedes ver una lista de más paquetes relacionados con genética estadística en [CRAN Task Statistical Genetics](https://cran.r-project.org/web/views/Genetics.html).

Otra opción para encontrar paquetes útiles es googlear "R package" + keywords de tu tema de interés, por ejemplo "metabarcoding".

También existen repositorios de paquetes especializados en un área, por ejemplo bioinformática.

**Bioconductor** es un repositorio de paquetes de R especializaos en en análisis de datos genómicos y de secuenciación masiva. 

![logo_bioconductor.gif](logo_bioconductor.gif)

### Generalidades de Bioconductor

#### [Página principal de Bioconductor](https://www.bioconductor.org/)

#### [Paquetes de Bioconductor](https://www.bioconductor.org/packages/release/BiocViews.html#___Software)

Como los paquetes de Bioconductor están escritos en el lenguaje de R, muchos tendrán tipos de objetos particulares al paquete y funciones nuevas, pero con tener las bases de R que hemos visto estarás listoa para aprenderlo. 

La mejor manera de conocer qué hace y  usar un paquete es seguir un tutorial o vignette.

Por ejemplo esta de [ggtree](https://www.bioconductor.org/packages/release/bioc/vignettes/ggtree/inst/doc/ggtree.html)  y esta de [SNPRelate](http://corearray.sourceforge.net/tutorials/SNPRelate/).


#### [Workflows](https://www.bioconductor.org/help/workflows/)

Para algunas tareas comunes en análisis genéticos, como [Variant calling](https://www.bioconductor.org/help/course-materials/2014/BioC2014/Lawrence_Tutorial.pdf).


#### [Cursos y conferencias de Bioconductor](https://www.bioconductor.org/help/course-materials/)

En particular yo recomiendo el curso online [Bioconductor for Genomic Data Science](http://kasperdanielhansen.github.io/genbioconductor/) de Kasper D. Hansen que incluye videos y código con notas en R y html. 

#### Instalar Bioconductor y sus paquetes

1) Tener instalado R

2) Instalar bioconductor (`source` al script `biocLite.R` que nos permitirá instalar paquetes de Bioconductor).

```
source("https://bioconductor.org/biocLite.R")
biocLite()
```
(Si lo anterior manda algún error intenta http:// en vez de  https://)

3) Utilizar la función `biocLite` para instalar los paquetes deseados. Ejemplo:

```
biocLite("ggtree")
```

Nota: algunos paquetes necesitan pasos extra de instalación, como jalar algo de GitHub, pero esto será indicado en la documentación del paquete.

#### Cómo citar R y Bioconductor

Citar R:

```
citation("base")
```

Citar Bioconductor:

```
citation("Biobase")
```

Citar un paquete en particular:

```
citation("NombrePaquete")
```
(o lo que loas autoreas especifiquen en su sitio web)


## 7.2. Population Genomics with R - special issue of Molecular Ecology Resources 

Recientemente Molecular Ecology Resources publicó el special issue Population Genomics with R especialmente sobre population genomics with R. El cual incluye revisiones, paquetes nuevos y estudios de caso. 

Revisemos la [Tabla de Contenido](http://onlinelibrary.wiley.com/doi/10.1111/men.2017.17.issue-1/issuetoc).  

y la Introducción:

[Paradis E, Gosselin T, Grünwald NJ et al. (2017) Towards an integrated ecosystem of R packages for the analysis of population genetic data. Molecular Ecology Resources, 17, 1–4.](
http://onlinelibrary.wiley.com/doi/10.1111/1755-0998.12577/full)


## 7.3. Methods in population genomics list

Los análisis de genómica de poblaciones van mucho más allá de R, y hay muchos programas para hacer análisis muy específicos. 

[Yann Burgeouis](http://www.yannbourgeois.com/) sacó el fua y creo esta Lista de Métodos de genómica de poblaciones: [methodspopgen.com](http://methodspopgen.com/). Donde recopila métodos para inferir estructura, detectar selección e inferir la historia de la población. 

# 7.4. ¿Qué software de todo eso me sirve? 

#### Ejercicios  

**Ejercicio 1** explora los paquetes de Bioconductor, CRAN, el número especial de MER y methodspopgen.com de acuerdo a tu tema. Menciona tres que creas te serán útiles y explóralos con mayor profundidad.

**Ejercicio 2** hagan equipos conforme a su tipo de datos y/o tema de investigación y discutan los paquetes que encontraron. Enlisten y describan para qué utilizarían los 3 que consideren más útiles. Hagan un pull resquest (por equipo) para actualizar este .md del repositorio en la parte de abajo ("Resultados ejercicio software interesante por equipos").

**Ejercicio 3**: 

1. Escoge uno de los paquetes que tu equipo eligió en el ejercicio pasado. 
2. Busca un tutorial, ayuda o vignette de ese paquete y síguelo con tus datos propios o con datos parecidos a los que tendrás que ya se encuentren publicados. 
3. Si es un paquete de R o Bioconductor ytiliza knitr para crear un "notebook" de lo que realizaste. 
4. Sube el código (.R, .sh, etc) y si aplica el notebook (.pdf) a tu cuenta de github. Será necesario enviar el link via ClassMarker.

Puedes apoyarte con loas integrantes de tu equipo del ejercicio pasado pero los resultados se entregan de forma individual y deben ser diferentes datos de input. 

## Resultados ejercicio software interesante por equipos

Utilizar el siguiente formato para ponder sus resultados:


**Equipo tal**
Integrantes: Perengana, Fulana y Sutano
* Paquete 1 (con link). Explicación para qué lo ocuparían y qué input requiere. 
* Paquete 2. Idem
* Paquete 3. Idem

**Phylo/Metabar**
Integrantes Nancy Bárcenas, Gerardo Torres, Víctor Taracena  y D. Jossue Jiménez 
* [phangorn](https://cran.r-project.org/web/packages/phangorn/index.html). La función phyDat sería útil para tranformar mis datos ("fasta") en uno admitido por phangorn ("phyDat").Se pueden realizar análisis filogenéticos de verosimilitud máxima y máxima pársimonia. Lo usaría tambien  para hacer comparación de diferentes modelos de sustitucion de aminoácidos. Tiene varias opciones para editar los árboles generados. Te permite exportar en formato "nexus".
* [muscle](https://bioconductor.org/packages/release/bioc/html/muscle.html). Efectúa alineamientos múltiples de secuencias de DNA, RNA y aminoácidos mediante un algoritmo iterativo, en el cuál primero se calculan alineamientos pareados a los cuáles se asignan *scores*, con los cuáles se construye una matriz para la inferencia de árboles en los que se evalúa el mejor alineamiento. El input y el output son secuencias .fasta
* [phyloseq](https://www.bioconductor.org/packages/release/bioc/html/phyloseq.html). Sirve para cargar tablas de OTUs sin importar en qué software procesé
Los datos crudos para obtener la tabla (DADA2, UPARSE, QIIME, mothur, BIOM, PyroTagger, RDP, etc.)

Me permite asociar datos, como parámetros ecológicos y ambientales de la localidad, la lista de taxa de mis OTUs, entre otros. 

Utiliza los siguientes input files: 

  |input file| phyloseq function|
  |------------|----------------|
  |.biom|import.biom()|
  |.tre|read.tree()|
  |map.txt|import_qiime_sample_data()|

La usaríamos para generar el archivo que después será ingresado a otros análisis (filogenéticos, genética de poblaciones...)

Requiere un formato del input "phyDat", si no se tiene, phangorn cuenta funciones para tranformar matrices y dataframe al formato "phyDat"

**Equipo Campechano**
Integrantes: Nelly, Tania, Sebastian y Madisson
* GENESIS [link](https://www.bioconductor.org/packages/release/bioc/html/GENESIS.html) Programa para estimar y contabilizar estructura poblacional, pedigree, coeficientes de parentezco, endogamia --> Es util para hacer PCA y detectar estructura poblacional *Input:* PLINK .bed, .bim, y .fam
* genfilter [link](https://www.bioconductor.org/packages/release/bioc/html/genefilter.html) Programa con métodos de filtrado genes obtenidos de NGS --> Es util para detectar si hay genes cerca de algún gen de interés detectado (para hacer perfiles de expresión,descartar genes ligados), o hacer ANOVA. *Input:* matriz de microarreglos o datos de RNAseq.
* funciSNP [link](https://www.bioconductor.org/packages/release/bioc/html/FunciSNP.html) Programa que integra información de estudios de asociación genómica (GWAS) para identificar SNP candidatos funcionales en regiones codificantes y no codificantes --> Es util para relacionar SNPś candidatos con caractres fisiológicos y funcionales *Input:* .bed


**RAD_team**
Integrantes: Carmina Martinez GOnzalez, Israel Moreno Contreras.
* Paquete 1: [**GENESIS**](https://www.bioconductor.org/packages/release/bioc/html/GENESIS.html). Análisis de estructura genética y relaciones de parentesco entre los individuos (ver si los individuos de mi muestra son primos, hermanos o qué relación tienen entre ellos). Para este programa se requiere que los archivos estén en formato PLINK o GDS.

* Paquete 2: [**poppr**](https://cran.r-project.org/web/packages/poppr/index.html). Medir diversidad genotípica y distancias genéticas de entre las poblaciones. Para este programa se requiere usar formato de GenAlEx en csv. 

* Paquete 3: [**genetics**](https://cran.r-project.org/web/packages/genetics/index.html). Saber si mis muestras se encuentran o no en equilibrio Hardy-Weinberg. Para este programa se requiere que los archivos estén en formato Pop, pedigree o market. 

**Equipo cochis** María Josefina Contreras y Mariana Pérez Rivera

*Los paquetes que necesitaremos son:*

-- **Paquete 1. MSA** (Multiple Sequence Alignment )
 https://https://www.bioconductor.org/packages/release/bioc/html/msa.html

 
 La ventaja es que alinea con los algoritmos de ClustalW, ClustalOmega y Muscle en un solo paquete. Se usaría para el análisis de las secuencias obtenidas con base en la de referencia. No requiere paquetes adicionales. 

El input es en formato FASTA



--**Paquete 2. ggtree**
https://www.bioconducor.org/packages/release/bioc/html/ggtree.html


Para la edición de los árboles filogenéticos, manipulación de clados y darles formato más chulo

newick, nexus, NHX, phylip y jplace

# 7.5 Ejemplo estadísticos básicos genética de poblaciones

SNPStats, Hierfstat y plink

# 7.6 Ejemplo PCA, estructura poblacional

SNPRelate, admixture


# 7.7 Ejemplo filogenias con Phytools

[phytools: Phylogenetic Tools for Comparative Biology (and Other Things)](https://cran.r-project.org/web/packages/phytools/index.html) es un paquete de R desarrollado por [Lian Revell](http://faculty.umb.edu/liam.revell/) que consta de decenas de funciones para analizar y graficar árboles filogenéticos. El paquete cuenta con un excelente blog: [http://blog.phytools.org/](http://blog.phytools.org/), que vale la pena pasar las tardes leyendo.

Vamos a ver unos ejemplos de uso tomado de su blog en [estas notas](Prac_Uni7/bin/Ejemplo_phytools.Rmd).



