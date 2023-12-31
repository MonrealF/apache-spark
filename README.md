¿Por qué usar Docker?
Instalar Docker puede proporcionar varios beneficios, y su utilidad dependerá de las necesidades
específicas de tu entorno de desarrollo o despliegue. Aquí hay algunas razones por las que podría
ser beneficioso instalar Docker.
VENTAJAS DE DOCKER EN EL ÁMBITO DE LIBRERIAS E INSTALACIONES.
Docker encapsula librerías y entornos en contenedores, lo que asegura que las aplicaciones se
ejecuten de manera consistente en diferentes entornos. Esto facilita la portabilidad y evita
problemas de dependencias.
Es decir; podemos compartir fácilmente el entorno de trabajo completo, incluyendo las librerías y
configuraciones necesarias, permitiendo a otros replicar exactamente el mismo entorno.
Ya que Docker permite gestionar versiones específicas de librerías y entornos. Puedes especificar
versiones exactas de las librerías requeridas, evitando conflictos entre versiones y garantizando la
consistencia en el desarrollo.
En este caso, al ser una serie de instalaciones tan complejas, se opto por instalar apache spark
dentro de un Docker para facilitar su portabilidad y manejo dentro de la clase de Big Data.# apache-spark


Requisitos para instalar Docker según el SO.
Para instalar Docker en tu sistema, debes asegurarte de que tu máquina cumpla con los requisitos
mínimos del sistema. Aquí hay pautas generales, aunque los detalles pueden variar según el
sistema operativo:
Requisitos del Sistema:
Linux:
1. Sistema Operativo:
- Docker es compatible con varias distribuciones de Linux. Algunas de las distribuciones más
comunes son Ubuntu, CentOS, Debian, Fedora, y más.
2. Arquitectura:
- La mayoría de las arquitecturas x86_64 son compatibles. Asegúrate de que tu hardware sea
compatible con la versión de Docker que deseas instalar.
3. Kernel de Linux:
- Docker requiere un kernel de Linux 3.10 o superior.
Windows:
1. Sistema Operativo:
- Docker Desktop para Windows requiere Windows 10 Pro o Enterprise (64-bit) con Hyper-V
habilitado. Para versiones anteriores, puedes usar Docker Toolbox.
2. Procesador:
- Debe admitir la virtualización de hardware con Hyper-V.
macOS:
1. Sistema Operativo:
- Docker Desktop para Mac requiere macOS 10.13 o superior.
2. Procesador:
- Debe ser un modelo compatible con la virtualización de hardware.
Otros Requisitos:
Recursos del Sistema:
RAM:
- Se recomienda tener al menos 2 GB de RAM dedicada a Docker, aunque más es beneficioso.
ESPACIO EN DISCO.
Asegúrate de tener suficiente espacio en disco disponible para almacenar las imágenes de los
contenedores y otros datos relacionados con Docker.
Instalación de Docker:
1. Descarga Docker:
- Visita el sitio web oficial de Docker para descargar la versión correspondiente a tu sistema
operativo: [Docker Download](https://www.docker.com/products/docker-desktop)
2. Instalación:
- Sigue las instrucciones específicas para tu sistema operativo para completar la instalación.
3. Configuración:
- Dependiendo del sistema operativo, puede que necesites realizar configuraciones adicionales.
Por ejemplo, en Windows, debes habilitar Hyper-V.
4. Verificación:
- Después de la instalación, verifica que Docker esté funcionando ejecutando comandos como
`docker --version` y `docker run hello-world


Para poder usarlo requerimos de los siguientes pasos.
• Clonar o descargar el repositorio.
Clona el repositorio desde GitHub en tu máquina local usando Git o descarga el código
como un archivo ZIP y extrae su contenido en la carpeta de tu preferencia.
Se recomienda crear una carpeta de fácil acceso en la raíz del sistema o en una carpeta
relacionada a la materia.
(Asegurate de tener Docker Desktop instalado.)
• Abrir la terminal.
Abre PowerShell, CMD o la terminal de tu preferencia en Windows.
• Navegar al directorio del Dockerfile.
Usa el comando ‘cd’ para moverte al directorio donde está ubicado el Dockerfile en tu
sistema.
(Usa el comando ‘DIR’ para ver los archivos existentes en tu carpeta actual).
• Construir la imagen del DockerFile.
Ejecuta el comando ‘docker build’ seguido de la ruta del Dockerfile en tu repositorio.
Por ejemplo:
docker build -t nombre_imagen:etiqueta_ruta -f nombre_archivo_dockerfile .
Reemplaza nombre_imagen con el nombre que desees darle a la imagen, etiqueta_ruta
con una etiqueta opcional para identificar la versión de la imagen,
nombre_archivo_dockerfile con el nombre del archivo Dockerfile si no se llama Dockerfile,
y asegúrate de incluir el punto (.) al final para indicar el contexto actual.
• Ejecutar el contenedor basado en la imagen creada.
Una vez que la imagen se ha construido correctamente, puedes ejecutar un contenedor
basado en ella con el comando docker run. Por ejemplo:
docker run -it --rm nombre_imagen:etiqueta_ruta
Esto iniciará un contenedor interactivo basado en la imagen que construiste.
Recuerda reemplazar nombre_imagen, etiqueta_ruta, nombre_archivo_dockerfile según
corresponda en tu caso.
