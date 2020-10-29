#Comandos de la Práctica 01
## Luis Angel Mancilla Galván


# Parte I.
**Rspuesta 1:**

MSAG@MSAG-PC ~
$ mkdir GenomicaComputacional

MSAG@MSAG-PC ~
$ dir
GenomicaComputacional  muse

MSAG@MSAG-PC ~
$ rmdir muse

MSAG@MSAG-PC ~
$ dir
GenomicaComputacional

MSAG@MSAG-PC ~
$ cd GenomicaComputacional

MSAG@MSAG-PC ~/GenomicaComputacional
$ mkdir lmancilla_p01

MSAG@MSAG-PC ~/GenomicaComputacional
$ cd lmancilla_p01

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01
$ touch comandos_p01.md

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01
$ dir
comandos_p01.md

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01
$


#Parte II.
##Crear directorios y mover los mismos

MSAG@MSAG-PC ~/GenomicaComputacional
$ cd lmancilla_p01

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01
$ dir
comandos_p01.md

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01
$ mkdir data filtered raw_data metal scripts figures archive

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01
$ dir
archive  comandos_p01.md  data  figures  filtered  metal  raw_data  scripts

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01
$ mv filtered MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/data
mv: no se puede efectuar `stat' sobre 'MSAG@MSAG-PC': No such file or directory

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01
$ dir
archive  comandos_p01.md  data  figures  metal  raw_data  scripts

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01
$ mv raw_data MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/data

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01
$ dir
archive  comandos_p01.md  data  figures  metal  scripts


#
#LA razon de por que usamos directorios especificos, es para llevar un orden, 
#data contiene los datos crudos geneticos, meta es para metadatos.
#bin o scribs guadra los scrips necesarios para el análisis de datos
#figures codigo para hacer figuras y finalmente archive es un directorio propio, se ponen scribs y resultados.

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01
$ cd scripts

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/scripts
$ touch delay.sh

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/scripts
$ nano delay.sh

echo "Despues de la practica I, necesito un descanso de exactamente 30s"
#Sleep tiempo de espera en segundos
sleep 30
echo "Ya estoy listo"
## si llegas a equivocarte puedes usar los comandos usando pid o kill

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/scripts
$ which bash
/usr/bin/bash



##Parte III. __/20
#generar archivo SarsCov--2 txt con el resumen y opinion del video. dentro de meta

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/meta
λ touch SarsCov-2.txt

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/meta
λ nano SarsCov-2.txt
# por ser texto plano, no se necesito saltos
#El virus es una novedosa sepa, que lo conforma un conjunto de proteínas, una de las principales son las S1, 
#S2 y no tienen conexión con algún receptor del cuerpo en la piel, necesita pasar por una capacitación de incisión, 
#el análisis genómico fue fácil, esto permitió identificar zonas para atacar con fármacos, por distintas estrategias, 
#RNA pequeños de unión, rnasas, o bloqueadores de la conexión de virulencia, las instituciones participando en la 
#vacuna son muchas, hablan de una vacuna con pedazos del virus que emula al mismo mediante saponinas, usadas para que 
#perdure la inmunidad. Otras opciones son usar virus ya conocidos, modificados, para estimular la respuesta inmune. 
#El virus seguirá causando muerte pues el desarrollo de vacunas aun es incierto y de tiempo largo. 


MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01
λ cd meta

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/meta
λ touch SarsCov-2_Spike.txt

MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/meta
λ nano SarsCov-2_Spike.txt

##De Estructura función y evolución de las proteínas de pico de coronavirus.
#El coronavirus es un conjunto de RNA y diversas proteínas, que son de importancia por que forman parte de cápside 
#que le confieren resistencia del miedo y es el primer contacto para establecer el contagio mediante 
#el receptor superficial. Una novedad es las distintas conformaciones de S2, esto va a promover y mediar la virulencia. 

#ya descargados los datos de sec de los NCBI, se movieron a data/raw_data del genoma
MSAG@MSAG-PC ~
λ mv /c/Users/MSAG/Downloads/Genomica/splike_c.faa /c/Users/MSAG/Downloads/Genomica/sarscov2_genome.fasta

MSAG@MSAG-PC ~
λ mv /c/Users/MSAG/Downloads/Genomica/sequence.gff3 /c/Users/MSAG/Downloads/Genomica/sarscov2_genome.gff3

#ahora bajando las proteinas c, b y a
#Renombrar el archivo usando mv
MSAG@MSAG-PC ~
λ mv /c/Users/MSAG/Downloads/Genomica/sequence.fasta  /c/Users/MSAG/Downloads/Genomica/splike_c.faa

MSAG@MSAG-PC ~
λ mv /c/Users/MSAG/Downloads/Genomica/sequence1.fasta  /c/Users/MSAG/Downloads/Genomica/splike_b.faa

MSAG@MSAG-PC ~
λ mv /c/Users/MSAG/Downloads/Genomica/sequence2.fasta  /c/Users/MSAG/Downloads/Genomica/splike_a.faa


#Ahora con el comando mv mover los archivos a data \ raw_data
MSAG@MSAG-PC ~/downloads
λ cd genomica
MSAG@MSAG-PC ~/downloads/genomica
λ dir
genoma2.fasta               sarscov2_genome.fasta  splike_a.faa  splike_c.faa             SRR10971381_R2.fastq.gz sarscov2_assembly.fasta.gz  sarscov2_genome.gff3   splike_b.faa  SRR10971381_R1.fastq.gz
MSAG@MSAG-PC ~/downloads/genomica
λ mv genoma2.fasta               sarscov2_genome.fasta  splike_a.faa  splike_c.faa             SRR10971381_R2.fas tq.gz sarscov2_assembly.fasta.gz  sarscov2_genome.gff3   splike_b.faa  SRR10971381_R1.fastq.gz /c/Users/MSAG/Geno micaComputacional/lmancilla_p01/data/raw_data



##  Parte IV. __ / 20
#creando ligas suaves de splike_c.faa, splike_b.faa y splike_a.faa
MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/data/raw_data
λ ln -s splike_c.faa sfsplike_c.faa
MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/data/raw_data
λ  ln -s splike_b.faa l
MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/data/raw_data
λ  ln -s splike_a.faa sfsplike_a.faa
#los cambio a data/filtered 
MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/data/raw_data
λ mv sfsplike_a.faa sfsplike_b.faa sfsplike_c.faa /c/Users/MSAG/GenomicaComputacional/lmancilla_p01/data/filtered 
λ cd ..
MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/data
λ cd filtered
#cambiando de directorio y creando glycoproteins.faa
MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/data/filtered
λ touch glycoproteins.faa
# head + numero de lineas + archivo |tee archivo destino
MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/data/filtered
λ  head -1 sfsplike_b.faa | tee comandos_p01.md
>pdb|6VXX|B Chain B, SARS-CoV-2 spike glycoprotein
MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/data/filtered
λ  head -1 sfsplike_a.faa | tee comandos_p01.md
>pdb|6VXX|A Chain A, SARS-CoV-2 spike glycoprotein
MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/data/filtered 
#cadena 1= pdb|6VXX|A Chain A, SARS-CoV-2 spike glycoprotein
#cadena 2= pdb|6VXX|B Chain B, SARS-CoV-2 spike glycoprotein
#cadena 3= pdb|6VXX|C Chain C, SARS-CoV-2 spike glycoprotein

#acomodar en el glicoproteinas, sabiendo que son solo 2 lineas es facil copiarlo todo con "head"
MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/data/filtered
λ head -n 2 ~/sfsplike_a.faa > ~/glycoproteins.faa


#abrir archivos comprimidos- solo visualizarlos con el comando gunzip -l [ARCHIVO]
MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/data/raw_data
λ gunzip -l SRR10971381_R1.fastq
         compressed        uncompressed  ratio uncompressed_name
            7599271            35300869  78.5% SRR10971381_R1.fastq
MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/data/raw_data
λ gunzip -l SRR10971381_R2.fastq
         compressed        uncompressed  ratio uncompressed_name
            7594918            35240197  78.4% SRR10971381_R2.fastq
MSAG@MSAG-PC ~/GenomicaComputacional/lmancilla_p01/data/raw_data
λ gunzip -l sarscov2_assembly.fasta
         compressed        uncompressed  ratio uncompressed_name
              11785               38667  69.6% sarscov2_assembly.fasta
