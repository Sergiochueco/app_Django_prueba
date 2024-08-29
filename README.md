Primero de todo debemos crear un entorno virtual para instalar nuestros paquetes independientemente de los que podamos tener en nuestro sistema, para ello utilizaremos el siguiente comando en la consola de git bash:

> python -m env "nombre del entorno" 

Por ejemplo: 

<pre><code>python -m env E_1</code></pre>

Después debemos activar el entorno, para ello debemos estar en la carpeta general del proyecto y en la consola de git bash escribiremos:

>source "nombre del entorno"/Scripts/activate 

Por ejemplo: 

<pre><code>source E_1/Scripts/activate</code></pre>

![(https://github.com/Sergiochueco/app_Django_prueba/blob/main/assets/create_activate_VE.PNG)](https://github.com/Sergiochueco/app_Django_prueba/blob/main/assets/create_activate_ve.png)

**pip freeze** lo utilizamos para comprobar que dependencias tenemos instaladas en nuestro entorno. Si es la primera vez que lo creamos debería de estar vacío

Siguiente paso es instalar Django desde nuestra terminal de git bash donde estamos trabajando:

>[!NOTE]
> Al instalar las dependencias con las que queremos trabajar deberemos tener activado nuestro entorno virtual.

<pre><code>pip install Django</code></pre>

![(https://github.com/Sergiochueco/app_Django_prueba/blob/main/assets/create_activate_VE.PNG)](https://github.com/Sergiochueco/app_Django_prueba/blob/main/assets/install_Django.PNG)

Comprobamos las dependencias que tenemos instaladas:

<pre><code>pip freeze</code></pre>

![(https://github.com/Sergiochueco/app_Django_prueba/blob/main/assets/create_activate_VE.PNG)](https://github.com/Sergiochueco/app_Django_prueba/blob/main/assets/pip_freeze.PNG)


Si queremos salir de nuestro entorno virtual, simplemente utilizamos el siguiente comando:


<pre><code>deactivate</code></pre>

![(https://github.com/Sergiochueco/app_Django_prueba/blob/main/assets/create_activate_VE.PNG)](https://github.com/Sergiochueco/app_Django_prueba/blob/main/assets/deactivate.PNG)



Una vez tenemos inicializado todo esto, ya podemos pasar al siguiente paso, inicializar el proyecto de Django. Para ello en mi caso he creado las carpetas de **src**, dentro de ella **proyecto** y he navegado hasta ella con el comando:

<pre><code>mkdir src</code></pre>
<pre><code>cd src</code></pre>
<pre><code>mkdir proyecto</code></pre>
<pre><code>cd src</code></pre>


Una vez dentro de está última, escribimos la siguiente línea para empezar el proyecto:

<pre><code> django-admin startproject proyecto </code></pre>

Lo que escribímos después de **startproject** es el nombre de otra carpeta que se creará con la inicialización del proyecto dentro

