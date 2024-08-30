# Crear y activar entorno virtual

Primero de todo debemos crear un entorno virtual para instalar nuestros paquetes independientemente de los que podamos tener en nuestro sistema, para ello utilizaremos el siguiente comando en la consola de git bash:

> python -m env "nombre del entorno" 

Por ejemplo: 

<pre><code>python -m env E_1</code></pre>

Después debemos activar el entorno, para ello debemos estar en la carpeta general del proyecto y en la consola de git bash escribiremos:

>source "nombre del entorno"/Scripts/activate 

Por ejemplo: 

<pre><code>source E_1/Scripts/activate</code></pre>

![(create_activate_virtual_environment)](https://github.com/Sergiochueco/app_Django_prueba/blob/main/assets/create_activate_ve.png)

# Ver las dependencias/librerías o paquetes instalados en el entorno

**pip freeze** lo utilizamos para comprobar que dependencias tenemos instaladas en nuestro entorno. Si es la primera vez que lo creamos debería de estar vacío

Siguiente paso es instalar Django desde nuestra terminal de git bash donde estamos trabajando:

>[!NOTE]
> Al instalar las dependencias con las que queremos trabajar deberemos tener activado nuestro entorno virtual.

<pre><code>pip install Django</code></pre>

![(install Django)](https://github.com/Sergiochueco/app_Django_prueba/blob/main/assets/install_Django.PNG)

Comprobamos las dependencias que tenemos instaladas:

<pre><code>pip freeze</code></pre>

![(pip_freeze)](https://github.com/Sergiochueco/app_Django_prueba/blob/main/assets/pip_freeze.PNG)


# Desactivar entorno virtual

Si queremos salir de nuestro entorno virtual, simplemente utilizamos el siguiente comando:


<pre><code>deactivate</code></pre>

![(deactivate virtual environment)](https://github.com/Sergiochueco/app_Django_prueba/blob/main/assets/deactivate.PNG)



Una vez tenemos inicializado todo esto, ya podemos pasar al siguiente paso, inicializar el proyecto de Django. Para ello en mi caso he creado las carpetas de **src**, dentro de ella **proyecto** y he navegado hasta ella con el comando:

<pre><code>mkdir src</code></pre>
<pre><code>cd src</code></pre>


# Inicializar proyecto

Una vez dentro de está última, escribimos la siguiente línea para empezar el proyecto:

<pre><code> django-admin startproject proyecto </code></pre>

Lo que escribímos después de **startproject** es el nombre de otra carpeta que se creará con la inicialización del proyecto dentro

Volvemos a navegar hasta esta nueva carpeta que hemos creado al inciar el proyecto y entonces corremos el servidor para crear una BBDD sqlite3 y poder ver nuestro proyecto ya en un servidor local.

## Correr el servidor en local

<pre><code> python manage.py runserver </code></pre>

Si queremos poder acceder como administradores será importante que corramos el comando **migrate**:

<pre><code> python manage.py migrate </code></pre>

Volveríamos a correr el servidor y entonces deberíamos ver la siguiente pantalla:

![(admin_interface)](https://github.com/Sergiochueco/app_Django_prueba/blob/main/assets/interfaz_admin.PNG)

# Creacion del usuario administrador del proyecto

Una vez aquí para obtener las credenciales para poder acceder, desde la consola crearemos el primer usuario:

<pre><code>python manage.py createsuperuser</code></pre>



> [!WARNING]
> Si te arroja el siguiente error: 
>Superuser creation skipped due to not running in a TTY. You can run `manage.py createsuperuser` in your project to create one manually.

La solución sería copiar este código en la consola:

<pre><code>winpty python manage.py createsuperuser</code></pre>

![(create superuser)](https://github.com/Sergiochueco/app_Django_prueba/blob/main/assets/superuser.PNG)


Donde introducirás tu usuario que será el administrador y la contraseña. No te preocupes si no ves que la contraseña va marcando los carácteres, es normal. Vas escribiendo pero en pantalla sale como si no estuvieras escribiendo nada. No te preocupes, escribe tu contraseña, dale a ENTER y te volverá a pedir la confirmación de esta.

Después de esto deberemos volver a correr el servidor como he comentado anteriormente para ver los cambios y poder acceder.


# Crear app

Una vez llegado hasta aquí deberemos crear la app donde vamos a crear nuestro proyecto. Para ello debemo escribir en consola el siguiente comando:


<pre><code>python manage.py startapp base</code></pre>

>[!NOTE]
> base será la carpeta donde se guardará esta app, así que verás en tu repositorio una carpeta nueva llamada base, puede ponerle el nombre que quieras.

Ahora deberemos conectar el servidor con la app. 

1. Accedemos al archivo **settings.py** en nuestra carpeta proyecto
2. En INSTALLED_APPS, deberemos escribir una línea de código más: "base.apps.Baseconfig",

>[!NOTE]
> Donde base es el nombre de la carpeta que hemos creado, si fuese "sitio" entonces el código sería "sitio.apps", y Baseconfig lo sacamos de la clase que viene por defecto en apps.py.

De ahora en adelante el contenido dependerá del proyecto a realizar para ello te recomiendo que te descargues este repositorio para utilizarlo como base y vayas cambiando aquello que necesites.

<pre><code>git clone git@github.com:Sergiochueco/app_Django_prueba.git</code></pre>

:bell: :hammer_and_wrench: En construcción, se irá actualizando este repo para tener el proyecto completo y lo puedas descargar como guía.


¡Cualquier sugerencia o cambio puedes escribirme en el correo [sergiochuecomedina@gmail](mailto:sergiochuecomedina@gmail.com?subject=[GitHub]%20Buenas%20Sergio)!


