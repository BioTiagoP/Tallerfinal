# <p align="center"><strong>Taller Final</strong></p>
## Integrantes: 
### Olmedo Lemache Valeria Lizeth
### Páez Andrade Marco Santiago
### Rodriguez Errais Carla Jazmín
## Tema:
### 16S Microbial analysis with Nanopore data
## Problema

Dado que los microorganismos constituyen la forma de vida más abundante y ubicua del planeta; y, en este contexto, el suelo representa el reservorio más importante de diversidad microbiana (i.e. 1 g de suelo contiene más de 107  células procariotas) es indiscutible su contribución significativa en el funcionamiento de los ecosistemas y los servicios que estos proveen (Kanchan et al., 2020; Mocali & Benedetti, 2010; Romero et al., 2023). 
La intensificación del uso de la tierra para fines agrícolas ha comprometido al microbioma del suelo, por lo que se han desarrollado diversas herramientas metagenómicas con el fin de comprender la composición taxonómica, rasgos funcionales e interacciones de estas comunidades biológicas (Romero et al., 2023; Wooley & Ye, 2010).
En este estudio se plantea analizar varias muestras obtenidas del suelo por metodología de secuenciación Minion Oxford-Nanopore, de la rizósfera y microbiota general (secuencias 16s ribosomal) para observar la diversidad taxonómica, con ello se pretende identificar si existen diferencias a breves rasgos y aplicar varias herramientas biotecnológicas que han facilitado investigaciones exhaustivas de comunidades microbianas completas (Leite et al., 2022; Zhang et al., 2021)


## Antecedentes 

Los suelos sanos son un elemento esencial para mantener el equilibrio ecológico del planeta. Las comunidades bacterianas presentes en el suelo brindan una multitud de servicios ecosistémicos que afectan directa e indirectamente el funcionamiento general del medio ambiente del suelo. Esto ha dado lugar a que muchos estudios describan variaciones en la composición de la comunidad bacteriana y sus roles funcionales (Fierer & Jackson 2006, Hermans et al. 2016 ). 
La diversidad bacteriana del suelo es inmensa y su composición y diversidad pueden verse influenciadas por una amplia gama de factores bióticos y abióticos. Entre las variables que se correlacionan con cambios en la composición de la comunidad bacteriana del suelo se encuentran el pH, la relación carbono-nitrógeno, el contenido de humedad y la temperatura del suelo (Buckley & Schmidt 2002).
Por otro lado, muchas especies de microorganismos establecen relaciones simbióticas complejas con organismos vegetales. La fracción del sustrato que se ve directamente influenciada por las secreciones de las raíces y los microorganismos asociados se conoce como rizosfera. Así, por ejemplo, bacterias del género Bacillus, Pseudomonas o Burkholderia aparecen asociadas a las raíces de las plantas, protegiéndolas de microorganismos patógenos (Das et al. 2023, Gallardo 2024)
La alteración de las poblaciones microbianas precede muchas veces a cambios en las propiedades físicas y químicas de los suelos, por lo que monitorear su estado y estudiar la composición de la comunidad bacteriana o la abundancia relativa de taxones individuales como indicadores del estado de los ambientes puede servir para predecir su evolución futura, permitiendo desarrollar estrategias para mitigar los daños a los ecosistemas (Fierer & Jackson 2006).
Los avances en las tecnologías de secuenciación han abierto la posibilidad de utilizar el estudio de taxones presentes en comunidades bacterianas como indicadores del estado del suelo. La plataforma MinION (Oxford Nanopore Technologies) ofrece una posibilidad única de realizar la caracterización microbiana del suelo gracias a su capacidad de secuenciación de lectura larga (Brown et al. 2017). Mientras que la secuenciación del gen 16S rRNA ha demostrado ser un enfoque excelente para identificar comunidades bacterianas beneficiosas y patógenas en sistemas multipatógeno-huésped (Das et al. 2023)

## Objetivos

1) Emplear la plataforma Galaxy para explorar la diversidad taxonómicas de las muestras de suelo obtenidas a partir de secuencias propias del tutorial 8
2) Identificar los cambios taxonómicos de las poblaciones microbianas de rizósfera y general a partir de su interacción con las raíces de las plantas
   
## Flujo de trabajo
![Flujo de trabajo](https://github.com/BioTiagoP/Tallerfinal/blob/main/workflow_grupo3.drawio-1.png)
## Resultados

## Conclusiones
* Se pudo utilizar la plataforma galaxy para analizar estado de salud de las muestras de suelo obtenidas a partir de secuencias propias del tutorial 8, se encontró complicaciones en el desarrollo de la actividad al momento de ejecutar las herramientas internas, sobre todo en la extracción del flujo de trabajo. Sin embargo, tras volver a ejecutar las herramientas se pudo obtener lo necesitado. Finalmente se pudo obtener en formato .png una imagen con el diagrama de flujo a partir del uso de la aplicación Diagrams de Google

* Se pudo identificar los cambios de de las poblaciones microbianas a partir de su interacción con las raíces de las plantas, EDITAREDITAREDITAREDITAREDITAREDITAREDITAREDITAR

* Se obtuvo un gráfico circular de comunidades bacterianas tras asignar la clasificación taxonómica a partir de la herramienta Kraken2  


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

