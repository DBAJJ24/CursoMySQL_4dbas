# CursoMySQL_4dbas
Herramientas y literatura sobre el curso UDEMY MySQL 4 DBA's

ISO: Centos 7 minimal edition
http://atl.mirrors.clouvider.net/CentOS/7.9.2009/isos/x86_64/CentOS-7-x86_64-Minimal-2009.iso

Software Instalado: VirtualBox / VMware WorkStation

MySQL Community Edition 8
https://downloads.mysql.com/archives/get/p/23/file/mysql-8.0.20-1.el7.x86_64.rpm-bundle.tar

Instalacion Centos 7

el disco realiza la instalacion minima por lo que hay que instalar ciertos paquetes antes de iniciar, asi que, una vez terminada la instalacion basica:

1.- primero actualizamos el sistema
sudo yum update && yum upgrade
2.- instalamos la paqueteria en caso de que falte
sudo yum install bzip2 tar rar zip net-tools gcc make perl wget
3.- creamos un directorio para montar la imagen de las utilerias de vbox
sudo mkdir /media/cdrom
4.- instalamos epel
sudo yum install epel-release
5.- agregamos los encabezados del kernel
-- primero validamos: ls -ltra /usr/src/kernel
-- la lista esta en cero
yum install -y kernel-devel
-- reiniciamos
6.- montamos el disco
sudo mount -t iso9660 -o loop /dev/sr0 /media/cdrom
-- ejecutamos:
/media/cdrom/./BVoxLinuxAdditions.run
7.-deshabilitar selinux
-- por comodidad deshabilitaremos selinux para poder modificar la configuracoin default de la carpeta de datos de mysql asi como el contexto de operacion del mismo


Listo !
tenemos el sistema con lo suficiente para poder isntalar un servidor dedicado de base de datos.

ahora la instalacion del motor de base de datos
yum remove mariadb-libs


mysql-community-common-8.0.20-1.el7.x86_64.rpm
mysql-community-libs-8.0.20-1.el7.x86_64.rpm
mysql-community-client-8.0.20-1.el7.x86_64.rpm
mysql-community-server-8.0.20-1.el7.x86_64.rpm





