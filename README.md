# Biopython-reconocimiento-biomarcadores

Repositorio desarrollado por Gabriel Collado Santamaría para el Trabajo Final de Grado del Análisis bioinformático para la detección de biomarcadores del cáncer empleando Biopython. 
Tutorizado por Rubén Ruiz González (departamento de digitalización) y Antonia Maiara Marques do Nascimento (departamento de Biotecnología y Ciencias de los alimentos).

Los directorios que contienen los datos y los notebooks necesarios para evaluar el trabajo presentado presenta la siguiente estructura:

  -Algoritmos de MSA: directorio en el cual se recogen los directorios de ambos algoritmos de alineamiento múltiple. 
  
      -ClustalOmega: Uno de ellos con todos los archivos que conforman el \textit{software} del algoritmo al completo.
            
            \item \textbf{Muscle}: Otro únicamente contiene el archivo ejecutable.
        \end{itemize}
    
    \item \textbf{clustal}: en él se encuentra el software completo de \texttt{Clustal}, uno de los algoritmos de alineamiento múltiple empleados en el \textit{notebook} de \texttt{Python}, \textit{Reconocimiento de biomarcadores con Biopython}.
    
    \item \textbf{muscle}: en él se encuentra el archivo ejecutable de \texttt{Muscle}, otro de los algoritmos de alineamiento múltiple empleados en el \textit{notebook} de \texttt{Python}, \textit{Reconocimiento de biomarcadores con Biopython}.
    
    \item \textbf{Datos}: directorio encargado de almacenar los datos brutos y procesados utilizados para el proyecto.
        \begin{itemize}
            \item \textbf{Datos pacientes enfermos}: carpeta que incluye las secuencias patológicas en bruto repartidas en cuatro archivos de formato \texttt{fasta}. Cada uno de ellos, correspondiente a cada uno de los genes: \textit{BRCA1,BRAC2,PIK3CA} y \textit{TP53}.
            
            \item \textbf{Datos pacientes sanos}: carpeta que incluye las secuencias control en bruto repartidas en cinco archivos de formato \texttt{fasta}. Cada uno de ellos, correspondiente a cada uno de los exones de los genes a estudio: exón 5 para \textit{BRCA1}, exones 2 y 11 para \textit{BRAC2}, y, por último, exones 5 y 8 para \textit{TP53}.
            
            \item \textbf{Secuencias control filtradas}: carpeta que incluye las secuencias secuencias control ya procesadas, listas para el análisis conveniente. El conjunto de estas, está formado por cinco archivos de formato \texttt{fasta} de menor tamaño y mismo nombre que los originales.
            
            \item \textbf{Secuencias patológicas filtradas}: directorio que contiene las secuencias patológicas ya procesadas en formato \texttt{fasta}. Hasta ocho archivos se llegan a incluir en este directorio, uno por cada uno de los exones de mayor frecuencia a estudiar, dos por cada gen: 5 y 19 de \textit{BRCA1}, 2 y 11 de \textit{BRCA2}, 9 y 20 de \textit{PIK3CA}; y 5 y 8 de \textit{TP53}.

            
            \item \textbf{Tablas variantes}: este directorio comprende dos archivos de extensión \texttt{csv}, Tabla variantes \textit{BRCA2} y \textit{PIK3CA}. Cada uno de ellos engloba las variantes existentes documentadas en \textit{gnomAD}  para un gen en concreto.
            
        \end{itemize}
    
    
    \item \textbf{Documentación}: directorio donde se encuentran los artículos considerados para la elaboración del proyecto. Hayan sido utilizados como fuente de inspiración o base teórica.
    
    \item \textbf{Imágenes}: comprende las imágenes utilizadas en el desarrollo de la memoria y los anexos.
    
    \item \textbf{Resultados}: directorio que integra los alineamientos y secuencias consenso obtenidas de la ejecución del \textit{notebook} \textit{Reconocimiento de biomarcadores con Biopython.ipynb}.
    
        \begin{itemize}
            \item \textbf{Alineamiento secuencias control}: fichero que incluye los alineamientos mediante \texttt{Clustal} y \texttt{Muscle} de las secuencias controles filtradas.
            
                \begin{itemize}
                    \item \textbf{Resultados alineamiento clustal}: abarca cuatro ficheros de extensión \texttt{.afa}, que contienen los alineamientos \texttt{Clustal} correspondientes a los exones pertenecientes a las secuencias controles filtradas.
                    
                    \item \textbf{Resultados alineamiento muscle}:
                    abarca cuatro ficheros de extensión \texttt{.afa}, que contienen los alineamientos \texttt{Muscle} correspondientes a los exones pertenecientes a las secuencias controles filtradas.
                    
                \end{itemize}
                
            \item \textbf{Alineamiento secuencias patológicas}: carpeta con los alineamientos de las secuencias patológicas procesadas de \texttt{Clustal} y \texttt{Muscle}.
            
                \begin{itemize}
                    \item \textbf{Resultados alineamiento clustal}: recoge ocho ficheros de extensión \texttt{.afa}, cada uno de ellos, por cada exón de los cuatro genes a analizar. Contienen los alineamientos \texttt{Clustal} de las secuencias patológicas seleccionadas.
                    
                    \item \textbf{Resultados alineamiento muscle}: recoge ocho ficheros de extensión \texttt{.afa}, cada uno de ellos, por cada exón de los cuatro genes a analizar. Contienen los alineamientos \texttt{Muscle} de las secuencias patológicas seleccionadas.
                    
                \end{itemize}
                
            \item \textbf{Secuencias consenso}: engloba todas las secuencias consenso de \texttt{Clustal} y \texttt{Muscle}, para patológicos y controles, conseguidas de la ejecución del \textit{notebook}.
            
                \begin{itemize}
                    \item \textbf{Secuencias consenso controles}: directorio con las secuencias consenso provenientes de \texttt{Clustal} y \texttt{Muscle} relativas a las secuencias controles.
                    
                        \begin{itemize}
                            \item \textbf{Clustal}: contiene cuatro archivos \texttt{fasta} correspondientes a las secuencias consenso control de \texttt{Clustal}.
                            
                            \item \textbf{Muscle}:contiene cuatro archivos \texttt{fasta} correspondientes a las secuencias consenso control de \texttt{Muscle}.
                        \end{itemize}
                        
                    \item \textbf{Secuencias consenso patológicas}: carpeta dónde se incluyen las secuencias consenso provenientes de \texttt{Clustal} y \texttt{Muscle} relativas a las secuencias patológicas.
                    
                        \begin{itemize}
                            \item \textbf{Clustal}: fichero poseedor de las siete secuencias consenso procedentes de los alineamientos \texttt{Clustal} de cada uno de los exones patológicos.
                            
                            \item \textbf{Muscle}:fichero poseedor de las siete secuencias consenso procedentes de los alineamientos \texttt{Muscle} de cada uno de los exones patológicos.
                        \end{itemize}
                        
                \end{itemize}
                
        \end{itemize}
    
    \item \textbf{Reconocimiento de biomarcadores con Biopython.ipynb}: \textit{notebook} de \texttt{Python} que recoge el desarrollo del proyecto en su totalidad. Desde los filtrados de secuencias, hasta la ejecución de los alineamientos y análisis de resultados.
