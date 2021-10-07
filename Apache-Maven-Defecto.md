# Instalación de Apache Maven por defecto en Ubuntu

Para realizar la instalación debemos ir a la terminal de nuestro sistema operativo **(CTRL+ALT+T)** y escribir lo siguiente para poder actualizar la descarga de los paquetes de las fuentes configuradas:  
```
sudo apt-get update
```

<img src="https://github.com/GraceCaraballoP/Instalaci-n-de-Apache-Maven-por-defecto-en-Ubuntu/blob/main/Captura1.png">    

Ahora con la siguiente instrucción descargará e instalará el paquete de Apache Maven por defecto:  
```
sudo apt install maven
```

<img src="https://github.com/GraceCaraballoP/Instalaci-n-de-Apache-Maven-por-defecto-en-Ubuntu/blob/main/Captura2.png">  

La instalación tardará un par de minutos.  
<img src="https://github.com/GraceCaraballoP/Instalaci-n-de-Apache-Maven-por-defecto-en-Ubuntu/blob/main/Captura3.png">  

Una vez hecho esto la instalación debe de haber finalizado correctamente, para comprobarlo ejecutaremos el comando:  

```
mvn -version
```

Donde como vemos en la imagen siguiente nos dice que la versión que tenemos es la **3.6.3**.  

<img src="https://github.com/GraceCaraballoP/Instalaci-n-de-Apache-Maven-por-defecto-en-Ubuntu/blob/main/Captura4.png">  

Como vemos en la imagen anterior la instalación se ha terminado con éxito. 
