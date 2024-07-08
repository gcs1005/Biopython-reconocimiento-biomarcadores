# Biopython-reconocimiento-biomarcadores

![800px-Biopython_logo](https://github.com/gcs1005/Biopython-reconocimiento-biomarcadores/assets/99986046/9f2b6182-117e-4c43-b78e-f8291c2f0e24)

Repositorio desarrollado por Gabriel Collado Santamaría para el Trabajo Final de Grado del Análisis bioinformático para la detección de biomarcadores del cáncer empleando Biopython. 
Tutorizado por Rubén Ruiz González (departamento de digitalización) y Antonia Maiara Marques do Nascimento (departamento de Biotecnología y Ciencias de los alimentos).



**ABSTRACT**

El cáncer de mama es un problema socio-sanitario de primer nivel en todo el del mundo. Se trata del cáncer con mayor incidencia en mujeres, llevándose a su vez la vida de 685.000 personas en el mundo y 6.608 personas tan solo en España para el año 2022. 

Ante esta evidente necesidad, y debido al compromiso de todo profesional sanitario, en este proyecto se pretendió diseñar un esquema de procesado de datos genéticos basado en la detección de biomarcadores característicos en el cáncer de mama.

A través de la base de datos de NCBI y la aplicación del paquete de Biopython, se pudieron realizar sobre un notebook de Jupyter diferentes alineamientos pareados y múltiples, entre patológicos y controles empleando los algoritmos Muscle y Clustal.
 
Gracias a dicho procesado bioinformático, y a pesar de las diversas dificultades experimentadas respecto a las condiciones presentadas por los datos, tuvo lugar al reconocimiento de mutaciones distintivas en aquellos genes vinculados con la patología. Entre ellas se destacan las sustituciones de un simple nucleótido; T>A para BRCA1, A>T para BRCA2, C>T para el exón 5 de TP53 y G>A para el exón 8 del mismo.

Los resultados han podido demostrar la gran aplicabilidad del paquete de Biopython como herramienta bioinformática para la detección de biomarcadores en el cáncer, una vez que se ha podido detectar mutaciones para los genes (BRCA1, BRCA2, PIK3CA y TP53) en células caracterizadas anteriormente como patológicas o normales para el cáncer de mama. Además, este trabajo, sienta las bases para futuros proyectos bioinformáticos de interés, y determina la importancia de la obtención de unos datos de calidad en etapas iniciales.




**CONTENIDO DEL REPOSITORIO**

Los directorios que contienen los datos y los notebooks necesarios para evaluar el trabajo elaborado, presenta la siguiente estructura:

-Algoritmos de MSA: directorio en el cual se recogen los directorios de ambos algoritmos de alineamiento múltiple. 
 -ClustalOmega: Uno de ellos con todos los archivos que conforman el software del algoritmo al completo.
  -Muscle: Otro únicamente contiene el archivo ejecutable.
    
    
-clustal: en él se encuentra el software completo de Clustal, uno de los algoritmos de alineamiento múltiple empleados en el notebook de Python, Reconocimiento de biomarcadores con Biopython. 

    
-muscle: en él se encuentra el archivo ejecutable de Muscle, otro de los algoritmos de alineamiento múltiple empleados en el notebook de Python, Reconocimiento de biomarcadores con Biopython.

    
-Datos: directorio encargado de almacenar los datos brutos y procesados utilizados para el proyecto.

    -Datos pacientes enfermos: carpeta que incluye las secuencias patológicas en bruto repartidas en cuatro archivos de formato \texttt{fasta}. Cada uno de ellos, correspondiente a cada uno de los genes: BRCA1,BRAC2,PIK3CA y TP53.
            
    -Datos pacientes sanos: carpeta que incluye las secuencias control en bruto repartidas en cinco archivos de formato fasta. Cada uno de ellos, correspondiente a cada uno de los exones de los genes a estudio: exón 5 para BRCA1, exones 2 y 11 para BRAC2, y, por último, exones 5 y 8 para TP53.
            
    -Secuencias control filtradas: carpeta que incluye las secuencias secuencias control ya procesadas, listas para el análisis conveniente. El conjunto de estas, está formado por cinco archivos de formato fasta de menor tamaño y mismo nombre que los originales.
            
    -Secuencias patológicas filtradas: directorio que contiene las secuencias patológicas ya procesadas en formato fasta. Hasta ocho archivos se llegan a incluir en este directorio, uno por cada uno de los exones de mayor frecuencia a estudiar, dos por cada gen: 5 y 19 de BRCA1, 2 y 11 de BRCA2, 9 y 20 de PIK3CA; y 5 y 8 de TP53.
            
    -Tablas variantes: este directorio comprende dos archivos de extensión csv, Tabla variantes BRCA2 y PIK3CA. Cada uno de ellos engloba las variantes existentes documentadas en gnomAD para un gen en concreto.
    
    
-Documentación: directorio donde se encuentran los artículos considerados para la elaboración del proyecto. Hayan sido utilizados como fuente de inspiración o base teórica.

    
-Imágenes: comprende las imágenes utilizadas en el desarrollo de la memoria y los anexos.

    
-Resultados: directorio que integra los alineamientos y secuencias consenso obtenidas de la ejecución del notebook Reconocimiento de biomarcadores con Biopython.ipynb.

    -Alineamiento secuencias control: fichero que incluye los alineamientos mediante Clustal y Muscle de las secuencias controles filtradas.
            
       -Resultados alineamiento clustal: abarca cuatro ficheros de extensión .afa, que contienen los alineamientos Clustal correspondientes a los exones pertenecientes a las secuencias controles filtradas.
                    
       -Resultados alineamiento muscle: abarca cuatro ficheros de extensión .afa, que contienen los alineamientos Muscle correspondientes a los exones pertenecientes a las secuencias controles filtradas.
                    
              
    -Alineamiento secuencias patológicas: carpeta con los alineamientos de las secuencias patológicas procesadas de Clustal y Muscle.

        -Resultados alineamiento clustal: recoge ocho ficheros de extensión .afa, cada uno de ellos, por cada exón de los cuatro genes a analizar. Contienen los alineamientos Clustal de las secuencias patológicas seleccionadas.
                    
        -Resultados alineamiento muscle: recoge ocho ficheros de extensión .afa, cada uno de ellos, por cada exón de los cuatro genes a analizar. Contienen los alineamientos Muscle de las secuencias patológicas seleccionadas.
        
                    
    -Secuencias consenso: engloba todas las secuencias consenso de Clustal y Muscle, para patológicos y controles, conseguidas de la ejecución del notebook.
        
        -Secuencias consenso controles: directorio con las secuencias consenso provenientes de Clustal y Muscle relativas a las secuencias controles.
        
            -Clustal: contiene cuatro archivos .fasta correspondientes a las secuencias consenso control de Clustal.
                            
            -Muscle:contiene cuatro archivos .fasta correspondientes a las secuencias consenso control de Muscle.
            
                        
        -Secuencias consenso patológicas: carpeta dónde se incluyen las secuencias consenso provenientes de Clustal y Muscle relativas a las secuencias patológicas.
         
            -Clustal: fichero poseedor de las siete secuencias consenso procedentes de los alineamientos Clustal de cada uno de los exones patológicos.
                            
            -Muscle:fichero poseedor de las siete secuencias consenso procedentes de los alineamientos Muscle de cada uno de los exones patológicos.

    
-Reconocimiento de biomarcadores con Biopython.ipynb: notebook de Python que recoge el desarrollo del proyecto en su totalidad. Desde los filtrados de secuencias, hasta la ejecución de los alineamientos y análisis de resultados.
