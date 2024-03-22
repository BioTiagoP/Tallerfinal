# <p align="center"><strong>Taller Final</strong></p>
## Integrantes: 
### Olmedo Lemache Valeria Lizeth
### Páez Andrade Marco Santiago
### Rodriguez Errais Carla Jazmín
## Tema:
### 16S Microbial analysis with Nanopore data
## Problema

<div style="text-align: justify">
Dado que los microorganismos constituyen la forma de vida más abundante y ubicua del planeta; y, en este contexto, el suelo representa el reservorio más importante de diversidad microbiana (i.e. 1 g de suelo contiene más de 10E7  células procariotas) es indiscutible su contribución significativa en el funcionamiento de los ecosistemas y los servicios que estos proveen (Kanchan et al., 2020; Mocali & Benedetti, 2010; Romero et al., 2023).
La intensificación del uso de la tierra para fines agrícolas ha comprometido al microbioma del suelo, por lo que se han desarrollado diversas herramientas metagenómicas con el fin de comprender la composición taxonómica, rasgos funcionales e interacciones de estas comunidades biológicas (Romero et al., 2023; Wooley & Ye, 2010).
En este estudio se plantea analizar varias muestras obtenidas del suelo por metodología de secuenciación Minion Oxford-Nanopore, de la rizósfera y microbiota general (secuencias 16s ribosomal) para observar la diversidad taxonómica, con ello se pretende identificar si existen diferencias a breves rasgos y aplicar varias herramientas biotecnológicas que han facilitado investigaciones exhaustivas de comunidades microbianas completas (Leite et al., 2022; Zhang et al., 2021).
</div>

## Antecedentes 

<div style="text-align: justify">
Los suelos sanos son un elemento esencial para mantener el equilibrio ecológico del planeta. Las comunidades bacterianas presentes en el suelo brindan una multitud de servicios ecosistémicos que afectan directa e indirectamente el funcionamiento general del medio ambiente del suelo. Esto ha dado lugar a que muchos estudios describan variaciones en la composición de la comunidad bacteriana y sus roles funcionales (Fierer & Jackson 2006, Hermans et al. 2016 ). 
La diversidad bacteriana del suelo es inmensa y su composición y diversidad pueden verse influenciadas por una amplia gama de factores bióticos y abióticos. Entre las variables que se correlacionan con cambios en la composición de la comunidad bacteriana del suelo se encuentran el pH, la relación carbono-nitrógeno, el contenido de humedad y la temperatura del suelo (Buckley & Schmidt 2002).
Por otro lado, muchas especies de microorganismos establecen relaciones simbióticas complejas con organismos vegetales. La fracción del sustrato que se ve directamente influenciada por las secreciones de las raíces y los microorganismos asociados se conoce como rizosfera. Así, por ejemplo, bacterias del género Bacillus, Pseudomonas o Burkholderia aparecen asociadas a las raíces de las plantas, protegiéndolas de microorganismos patógenos (Das et al. 2023, Gallardo 2024).
La alteración de las poblaciones microbianas precede muchas veces a cambios en las propiedades físicas y químicas de los suelos, por lo que monitorear su estado y estudiar la composición de la comunidad bacteriana o la abundancia relativa de taxones individuales como indicadores del estado de los ambientes puede servir para predecir su evolución futura, permitiendo desarrollar estrategias para mitigar los daños a los ecosistemas (Fierer & Jackson 2006).
Los avances en las tecnologías de secuenciación han abierto la posibilidad de utilizar el estudio de taxones presentes en comunidades bacterianas como indicadores del estado del suelo. La plataforma MinION (Oxford Nanopore Technologies) ofrece una posibilidad única de realizar la caracterización microbiana del suelo gracias a su capacidad de secuenciación de lectura larga (Brown et al. 2017). Mientras que la secuenciación del gen 16S rRNA ha demostrado ser un enfoque excelente para identificar comunidades bacterianas beneficiosas y patógenas en sistemas multipatógeno-huésped (Das et al. 2023).
</div>

## Objetivos

<div style="text-align: justify">

1) Emplear la plataforma Galaxy para explorar la diversidad taxonómicas de las muestras de suelo obtenidas a partir de secuencias propias del tutorial 8
2) Identificar los cambios taxonómicos de las poblaciones microbianas de rizósfera y general a partir de su interacción con las raíces de las plantas
</div>
   
## Flujo de trabajo
![Flujo de trabajo](https://github.com/BioTiagoP/Tallerfinal/blob/main/imagenes/workflow_grupo3.drawio-1.png)

## Proceso

### Obtención de datos

Las secuencias corresponden a metagenomas obtenidos a partir de muestras de rizosfera asociada a plantas de granada (Punica granatum) y suelo a dos niveles de profundidad (0-5 cm/10-15cm) 

### Linea de comando
carmin@carmin-virtualbox:~/Descargas$ wget https://www.bioinformatics.babraham.ac.uk/projects/fastqc/fastqc_v0.12.1.zip #Descargar link de fastqc 
carmin@carmin-virtualbox:~/Descargas$ ls #muestra contenido del directorio
fastqc_v0.12.1.zip  jdk-22_linux-x64_bin  jdk-22_linux-x64_bin.deb 
carmin@carmin-virtualbox:~/Descargas$ unzip fastqc_v0.12.1.zip #Descomprime carpeta descargada
carmin@carmin-virtualbox:~/Descargas$ ls #muestra contenido del directorio
FastQC  fastqc_v0.12.1.zip  jdk-22_linux-x64_bin  jdk-22_linux-x64_bin.deb
carmin@carmin-virtualbox:~/Descargas$ ls FastQC/ #muestra contenido carpeta
cisd-jhdf5.jar  fastqc_icon.ico  INSTALL.txt 	LICENSE_JHDF5.txt  org     	RELEASE_NOTES.txt  uk
Configuration   Help         	jbzip2-0.9.jar  LICENSE.txt    	README.md   run_fastqc.bat
fastqc      	htsjdk.jar   	LICENSE     	net            	README.txt  Templates
carmin@carmin-virtualbox:~/Descargas$ chmod +x FastQC/fastqc #otorga permisos de ejecución
carmin@carmin-virtualbox:~/Descargas$ FastQC/fastqc --version #muestra la versión de FastQC instalado
FastQC v0.12.1
carmin@carmin-virtualbox:~/Descargas$ ls #descargamos las secuencias de interés en un archivo .zip
drive-download-20240321T031648Z-001.zip  FastQC  fastqc_v0.12.1.zip  jdk-22_linux-x64_bin  jdk-22_linux-x64_bin.deb
carmin@carmin-virtualbox:~/Descargas$ unzip drive-download-20240321T031648Z-001.zip
Archive:  drive-download-20240321T031648Z-001.zip #descomprime carpeta de secuencias
  inflating: bulk_top.fastq     	 
  inflating: bulk_bottom.fastq  	 
  inflating: rhizosphere_bottom.fastq  
  inflating: rhizosphere_top.fastq   
carmin@carmin-virtualbox:~/Descargas$ FastQC/fastqc #ejecuta el programa FASTQC en una nueva ventana
carmin@carmin-virtualbox:~/Descargas$ ls #descargamos los reportes del FASTQC en formato .html
bulk_bottom.fastq    	bulk_top_fastqc.zip                  	jdk-22_linux-x64_bin.deb    	rhizosphere_top_fastqc.html
bulk_bottom_fastqc.html  drive-download-20240321T031648Z-001.zip  rhizosphere_bottom.fastq    	rhizosphere_top_fastqc.zip
bulk_bottom_fastqc.zip   FastQC                               	rhizosphere_bottom_fastqc.html
bulk_top.fastq       	fastqc_v0.12.1.zip                   	rhizosphere_bottom_fastqc.zip
bulk_top_fastqc.html 	jdk-22_linux-x64_bin                 	rhizosphere_top.fastq
carmin@carmin-virtualbox:~/Descargas$ mkdir Reportes #creamos una nueva carpeta llamada “Reportes” para organizar los archivos .html 
carmin@carmin-virtualbox:~/Descargas$ mv bulk_bottom_fastqc.html ~/Descargas/Reportes/ #mover archivo .html a la carpeta Reportes 
carmin@carmin-virtualbox:~/Descargas$ mv bulk_top_fastqc.html ~/Descargas/Reportes/ #mover archivo .html a la carpeta Reportes 
carmin@carmin-virtualbox:~/Descargas$ mv rhizosphere_bottom_fastqc.html ~/Descargas/Reportes/ #mover archivo .html a la carpeta Reportes 
carmin@carmin-virtualbox:~/Descargas$ mv rhizosphere_top_fastqc.html ~/Descargas/Reportes/ #mover archivo .html a la carpeta Reportes 
carmin@carmin-virtualbox:~/Descargas$ ls Reportes/ #muestra contenido de la carpeta Reportes
bulk_bottom_fastqc.html  bulk_top_fastqc.html  rhizosphere_bottom_fastqc.html  rhizosphere_top_fastqc.html


## Resultados

![Bulky Soil Bottom](https://github.com/BioTiagoP/Tallerfinal/blob/main/imagenes/bulkybot.png)
<p align="center"><strong>Figura 1.</strong> Taxonomía de muestra de suelo de 10-15cm de profundidad</p>

En la figura se puede observar que el filo más abuntante es Proteobacteria 67%; Bacteroidetes con un 6%; Firmicutes 13%; Actinobacterias con 12%; Planctomycetes 0.6 % y Acidobacterias 0.1 % con un total de 2638 lecturas diferentes

![Bulky Soil Top](https://github.com/BioTiagoP/Tallerfinal/blob/main/imagenes/bulkytop.png)
<p align="center"><strong>Figura 2.</strong> Taxonomía de muestra de suelo de 0-5cm de profundidad</p>

En la figura se puede observar que el filo más abuntante es Proteobacteria 63%; Bacteroidetes con un 9%; Firmicutes 14%; Actinobacterias con 12%; Planctomycetes 0.8 % y Acidobacterias 0.2 % con un total de 3164 lecturas diferentes

![Rhizosphere Bottom](https://github.com/BioTiagoP/Tallerfinal/blob/main/imagenes/rizobot.png)
<p align="center"><strong>Figura 3.</strong> Taxonomía de muestra de suelo de 10-15cm de profundidad</p> 

En la figura se puede observar que el filo más abuntante es Proteobacteria 42%; Bacteroidetes con un 30%; Firmicutes 10%; Actinobacterias con 9%; Planctomycetes 6 % y Acidobacterias 0.8 % con un total de 1558 lecturas diferentes.

![Rhizosphere Top](https://github.com/BioTiagoP/Tallerfinal/blob/main/imagenes/rizotop.png)
<p align="center"><strong>Figura 4.</strong> Taxonomía de muestra de rizósfera de 0-5cm de profundidad</p> 

En la figura se puede observar que el filo más abuntante es Proteobacteria 41%; Bacteroidetes con un 30%; Firmicutes 10%; Actinobacterias con 9%; Planctomycetes 8 % y Acidobacterias 1 % con un total de 1315 lecturas diferentes.

## Conclusiones

* Se pudo utilizar la plataforma galaxy para explorar la diversidad taxonómicas de las muestras de suelo obtenidas a partir de secuencias propias del tutorial 8 y se pudo obtener en formato .png una imagen con el diagrama de flujo a partir del uso de la aplicación Diagrams de Google
  
* Se logró identificar cambios taxonómicos de las poblaciones microbianas puesto que se pudo observar diferentes taxones

* Se obtuvo cuatro gráficos circular de comunidades bacterianas tras asignar la clasificación taxonómica a partir de la herramienta Kraken2  

## Referencias Bibliográficas 
*Cristóbal Gallardo, 16S Microbial analysis with Nanopore data (Galaxy Training Materials). https://training.galaxyproject.org/training-material/topics/microbiome/tutorials/nanopore-16S-metagenomics/tutorial.html Online; accessed Tue Mar 19 2024

*Hiltemann, Saskia, Rasche, Helena et al., 2023 Galaxy Training: A Powerful Framework for Teaching! PLOS Computational Biology 10.1371/journal.pcbi.1010752

*Batut et al., 2018 Community-Driven Data Analysis Training for Biology Cell Systems 10.1016/j.cels.2018.05.012

*Kanchan, S., Sinha, R., Chaudière, J., & Kesheri, M. (2020). COMPUTATIONAL METAGENOMICS: CURRENT STATUS AND CHALLENGES. En Nova Science Publisher (Ed.), Recent Trends in Computational Omics. Nova Science Publisher.

*Leite, M. F. A., Van Den Broek, S. W. E. B., & Kuramae, E. E. (2022). Current Challenges and Pitfalls in Soil Metagenomics. Microorganisms, 10(10), 1900. https://doi.org/10.3390/microorganisms10101900 

*Mocali, S., & Benedetti, A. (2010). Exploring research frontiers in microbiology: the challenge of metagenomics in soil microbiology. Research In Microbiology, 161(6), 497-505. https://doi.org/10.1016/j.resmic.2010.04.010

*Romero, F., Hilfiker, S., Edlinger, A., Held, A., Hartman, K., Labouyrie, M., & Van Der Heijden, M. G. A. (2023). Soil microbial biodiversity promotes crop productivity and agro-ecosystem functioning in experimental microcosms. Science Of The Total Environment, 885, 163683. https://doi.org/10.1016/j.scitotenv.2023.163683 

*Wooley, J., & Ye, Y. (2010). Metagenomics: Facts and Artifacts, and Computational Challenges. Journal Of Computer Science And Technology, 25(1), 71-81. https://doi.org/10.1007/s11390-010-9306-4 

*Zhang, L., Chen, F., Zeng, Z., Xu, M., Sun, F., Liu, Y., Bi, X., Lin, Y., Gao, Y., Hao, H., Yi, W., Li, M., & Xie, Y. (2021). Advances in Metagenomics and Its Application in Environmental Microorganisms. Frontiers In Microbiology, 12. https://doi.org/10.3389/fmicb.2021.766364

