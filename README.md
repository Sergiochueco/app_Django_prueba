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
