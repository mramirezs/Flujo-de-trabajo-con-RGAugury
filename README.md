# Flujo-de-trabajo-con-RGAugury

1. Preparativos del Sistema
a) Actualiza el sistema e instala las librerías esenciales
Ejecuta los siguientes comandos para actualizar el sistema e instalar las librerías y dependencias básicas:

´´´
sudo apt-get update
sudo apt-get upgrade
´´´

# Instalar librerías necesarias para GD
sudo apt-get install zlib1g-dev libpng-dev libfreetype6-dev libgd-dev

# Para ejecutar programas de 32-bit (por ejemplo, phobius) en un sistema de 64 bits:
sudo apt-get install libstdc++6:i386

2. Instalación de Software Esencial
a) BLAST+
Descarga el paquete BLAST+ adecuado (archivo x64-linux.tar.gz) desde el sitio NCBI y extrae el contenido en un directorio accesible para todos los usuarios, por ejemplo /opt/blast:

cd /tmp
wget ftp://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/LATEST/ncbi-blast-*-x64-linux.tar.gz
tar -xzvf ncbi-blast-*-x64-linux.tar.gz
sudo mv ncbi-blast-* /opt/blast

b) HMMER3
Descárgalo desde hmmer.org y compílalo/instálalo (o instala desde repositorio si existe):

cd /tmp
wget http://eddylab.org/software/hmmer/hmmer-3.3.2.tar.gz
tar -xzvf hmmer-3.3.2.tar.gz
cd hmmer-3.3.2
./configure --prefix=/opt/hmmer3
make
sudo make install

c) Java (JDK 11 para Interproscan; JDK 1.8 si se requiere en otro componente)
Si Java 11 es el requerido para InterProScan, instálalo (o bien descarga el JDK de Oracle/OpenJDK):

bash
Copy
sudo apt-get install openjdk-11-jdk

d) pfam_scan Package
Descarga el paquete desde pfam_scan o el repositorio oficial. Coloca el script pfam_scan.pl en un directorio incluido en el PATH (por ejemplo, /opt/pfam_scan):

git clone https://github.com/aziele/pfam_scan

# Asegúrate de que pfam_scan.pl tenga permisos de ejecución:
sudo chmod +x pfam_scan.pl

e) Phobius 1.01
Descarga el paquete Phobius y colócalo en un directorio accesible (por ejemplo, /opt/phobius1.01):

wget https://software.sbc.su.se/files/phobius101_linux.tgz
tar -xzvf phobius101_linux.tgz
cd phobius

i) InterProScan
Descárgalo desde el sitio de InterPro y extrae el paquete en un directorio accesible (por ejemplo, /opt/interproscan):

cd /tmp
wget http://ftp.ebi.ac.uk/pub/software/unix/iprscan/5/5.72-103.0/interproscan-5.72-103.0-64-bit.tar.gz
unzip interproscan-5.x-xx-xx.zip
sudo mv interproscan-5.x-xx-xx /opt/interproscan
