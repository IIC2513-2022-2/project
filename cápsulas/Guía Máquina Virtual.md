# Guía Máquina Virtual

Para usuarios de Windows, recomendamos para el proyecto el uso de Ubuntu montado sobre una máquina virtual. En esta guía vamos a cubrir su instalación y configuración.
Para esto, ocuparemos el software de virtualización VirtualBox. 

## Instalaciones previas
En primer lugar, debes descaragar [VirtualBox](https://www.virtualbox.org/) y la imagen de [Ubuntu](https://ubuntu.com/download/desktop) (versión 22.04).  

## Guía instalación y configuración
A continuación, recomendamos seguir la siguiente [guía de instalación de Ubuntu en VirtualBox](https://es.wikihow.com/instalar-Ubuntu-en-VirtualBox). Hay algunas
imágenes que se encuentran desactualizadas, pero es muy cercano a lo que aparecerá.

Se pueden cambiar los parámetros que vienen por default para aumentar el desempeño (en particular la cantidad de memoria asignada a la RAM). Sin embargo, 
se debe tener en cuenta no aumentarlo a niveles que afecten al sistema operativo host (en este caso Windows). 

## Siguientes pasos 
Finalmente, se debe realizar el set up del ambiente de desarrollo en Ubuntu. Para esto, hay que instalar el editor de código, git y las demás 
dependencias que se abordarán en las siguientes cápsulas. 

Es importante notar que aunque estas dependencias estén instaladas en Windows, para poder ser usadas en Ubuntu, deben volver a ser instaladas en este sistema operativo.

## Links útiles 

- Para poder hacer copy paste desde Windows a Ubuntu y visceversa - [Why doesn't clipboard sharing work ...](https://superuser.com/questions/1318231/why-doesnt-clipboard-sharing-work-with-ubuntu-18-04-lts-inside-virtualbox-5-1-2)
