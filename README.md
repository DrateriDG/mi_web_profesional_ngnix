# Portafolio Web Profesional y Despliegue Contenedorizado

Este repositorio contiene el código fuente y los archivos de configuración para constriur y ejecutar de mi portafolio web profesional. El sitio ha sido diseñado con empresas grandes como publico objetivo, estructurado para exponer mis futuras competencias como Ingeniero de Software Junior ante empresas.

Con el objetivo de aplicar las mejores prácticas de la industria en el ámbito de DevOps y desarrollo web, el proyecto se encuentra completamente contenedorizado y listo para ser distribuido de forma ágil.

---
## Objetivo del Proyecto

El desarrollo de esta pagina web tuvo como objetivo:
1. Construir una interfaz web que se adapata a varios dispositivos, que presente mis futuras competencias tecnicas.
2. Demostrar el dominio en HTML5 Semántico y CSS. Entendiendo como usar los diferentes contenedores y selectores con sus diferentes propiedades.
3. Aprender a utilizar la herramienta de Docker Hub como repositorio para imagenes de paginas web.

---

## Tecnologías Utilizadas

La pagina web usó:

*   **HTML5:** Utilizado para establecer la estructura semántica y la jerarquía de contenidos de cada sección.
*   **CSS:** Crear y alinear los componentes visuales y garantizar la adaptabilidad completa en dispositivos móviles.
*   **Docker:** Herramienta clave para la creación, almacenamiento y control de versiones de las imagenes de la pagina web.
*   **NGINX (Base Alpine):** Servidor web de alta disponibilidad y rendimiento configurado dentro del contenedor. Se seleccionó la distribución *Alpine Linux* debido a su arquitectura ultra ligera y segura.

---

## Estructura del Proyecto

La distribución de los archivos dentro del repositorio está organizada de la siguiente manera:

```text
├── index.html          # Estructura de etiquetas y contenidos del portafolio
├── styles.css           # Estilos visuales, layouts adaptativos y media queries
├── Dockerfile          # Instrucciones y directivas para la construcción de la imagen
├── background.jpg       # Imagen de fondo general de la plataforma
├── presentacion.jpg     # Componente visual para la sección de portada
├── yo.jpeg             # Fotografía de perfil profesional
├── mail_icon.png        # Icono de acceso directo para el correo electrónico
└── linkedin_icon.png    # Icono de acceso directo para la red profesional LinkedIn
```

---

## Instrucciones para Construir y Ejecutar con Docker

Para inicializar este proyecto en un entorno local, asegúrese de tener el motor de Docker activo y ejecute los siguientes comandos en su terminal:

### 1. Construir la Imagen Docker
Sitúese en el directorio raíz del proyecto (donde se encuentra el archivo `Dockerfile`) y ejecute el comando para compilar la imagen:

```bash
docker build -t mi-portafolio-web .
```

*Nota: No olvidar el punto `.` final para especificar el directorio actual.*

### 2. Ejecutar el Contenedor
Una vez compilada la imagen, inicie el contenedor mapeando el puerto `80` nativo del servidor NGINX hacia el puerto que prefiera de su máquina local (en este ejemplo, el puerto `8080`):

```bash
docker run -d -p 8080:80 --name mi-portafolio-en-vivo mi-portafolio-web
```

Tras completar este paso, puede verificar el funcionamiento del portafolio abriendo su navegador e ingresando a la dirección: **`http://localhost:8080`**.

---

## Enlace a Docker Hub

Para facilitar la distribución y evitar el proceso de compilación manual del código fuente, la imagen pública de este portafolio se encuentra alojada en el registro oficial de Docker Hub.

Puede consultar las etiquetas disponibles y la documentación de la imagen en el siguiente enlace:

**[Acceder al repositorio en Docker Hub](https://hub.docker.com/repository/docker/drateridg/web-profesional-nginx/general)**

Para realizar la descarga directa de la imagen mediante la terminal, ejecute el siguiente comando:
```bash
docker pull drateridg/mi-portafolio-web:latest
docker run -d -p 8080:80 --name mi_web_profesional drateridg/portafolio-profesional:latest
```
y puede verificar su funcionamiento con http://localhost:8080/ .
---
Desarrollado por **Edwin David Guachi Cabrera** – *Estudiante de la Universidad de las Fuerzas Armadas ESPEs*.
