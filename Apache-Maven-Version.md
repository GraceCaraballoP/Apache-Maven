# Instalación de Apache Maven seleccionando la versión en Ubuntu

Comenzaremos accediendo a la página de Apache y comprobando cual es la última versión de Maven disponible. 

https://downloads.apache.org/maven/maven-3/

<img src="https://github.com/GraceCaraballoP/Instalaci-n-de-Apache-Maven-seleccionando-la-versi-n-en-Ubuntu/blob/main/Captura1.png">  

Seguidamente iremos a la terminal de nuestro sistema operativo **(CTRL+ALT+T)** y descargaremos la última versión disponible de Apache Maven en el directorio /tmp para ello escribiremos lo siguiente:  
```
wget https://www.apache.org/dist/maven/maven-3/3.8.2/binaries/apache-maven-3.8.2-bin.tar.gz -P /tmp
```

<img src="https://github.com/GraceCaraballoP/Instalaci-n-de-Apache-Maven-seleccionando-la-versi-n-en-Ubuntu/blob/main/Captura2.png">  

Una vez finalizada la descarga extraemos el fichero en el directorio */opt* lo haremos con la siguiente instrucción:  
```
sudo tar xf /tmp/apache-maven-*.tar.gz -C /opt
```

<img src="https://github.com/GraceCaraballoP/Instalaci-n-de-Apache-Maven-seleccionando-la-versi-n-en-Ubuntu/blob/main/Captura3.png">  

Crearemos con la siguiente instrucción un enlace que apunte al directorio de instalación de Maven, para poder tener control sobre las versiones e actualizaciones de Maven:  
```
sudo ln -s /opt/apache-maven-3.8.2 /opt/maven
```

<img src="https://github.com/GraceCaraballoP/Instalaci-n-de-Apache-Maven-seleccionando-la-versi-n-en-Ubuntu/blob/main/Captura4.png">  

Deberemos establecer las variables de entorno, para ello crearemos un archivo llamado *mavenenv.sh* en el directorio */etc/profile.d/* con nuestro editor de textos, lo haremos con la siguiente instrucción:  
```
sudo nano /etc/profile.d/maven.sh
```

<img src="https://github.com/GraceCaraballoP/Instalaci-n-de-Apache-Maven-seleccionando-la-versi-n-en-Ubuntu/blob/main/Captura5.png">
 
Una vez dentro del archivo debemos escribir lo siguiente:

```
export M2_HOME=/opt/maven  
export MAVEN_HOME=/opt/maven  
export PATH=${M2_HOME}/bin:${PATH} 
```  

Tras escribir lo anterior guardaremos y cerraremos el archivo.  
<img src="https://github.com/GraceCaraballoP/Instalaci-n-de-Apache-Maven-seleccionando-la-versi-n-en-Ubuntu/blob/main/Captura6.png">  

Ahora debemos hacer que el archivo anterior sea ejecutable, para ello escribiremos lo siguiente:  
```
sudo chmod +x /etc/profile.d/maven.sh
```

<img src="https://github.com/GraceCaraballoP/Instalaci-n-de-Apache-Maven-seleccionando-la-versi-n-en-Ubuntu/blob/main/Captura7.png"> 
 
Seguidamente cargaremos las variables de entorno anteriormente escritas a través del comando *source*:  
```
source /etc/profile.d/maven.sh
```

<img src="https://github.com/GraceCaraballoP/Instalaci-n-de-Apache-Maven-seleccionando-la-versi-n-en-Ubuntu/blob/main/Captura8.png"> 

Con esto quedaría finalizada la instalación, pero verificaremos para ver si se ha instalado correctamente con el código siguiente:  
```
mvn –version
```

<img src="https://github.com/GraceCaraballoP/Instalaci-n-de-Apache-Maven-seleccionando-la-versi-n-en-Ubuntu/blob/main/Captura9.png">  

Como vemos en la imagen anterior la instalación se ha terminado con éxito. 
