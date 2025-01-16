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
