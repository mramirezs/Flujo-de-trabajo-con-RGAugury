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
