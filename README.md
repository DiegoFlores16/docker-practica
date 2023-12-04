# Dockerización de Aplicación NestJS y GitHub Actions

## Descripción
Este repositorio demuestra cómo Dockerizar una aplicación NestJS y configurar un flujo de trabajo en GitHub Actions para construir y desplegar contenedores de Docker.

## Pasos por seguir

### 1. Crear Repositorio

Crea un repositorio público o privado en GitHub. [Enlace al Repositorio](https://github.com/DiegoFlores16/docker-practica)
![Alt text](img/image1.png)

### 2. Preparar el Código Fuente

Luego solo realizamos el commit del código a utilizar
![Alt text](img/image2.png)

### 4. Configurar Secrets en GitHub

Crea los secrets DOCKER_USER y DOCKER_PASSWORD en la sección de Secrets de tu repositorio en GitHub.
![Alt text](img/image3.png)
![Alt text](img/image4.png)
![Alt text](img/image5.png)


### 5. Configurar Token de Docker Hub

Utiliza tu usuario y clave (token) de Docker Hub para llenar los secrets DOCKER_USER y DOCKER_PASSWORD.
Crea un Token en Docker (con el nombre Github-Actions) y copia este Token generado en el secret DOCKER_PASSWORD.
![Alt text](img/image6.png)
![Alt text](img/image7.png)
![Alt text](img/image8.png)


#### 6. Dockerizar la Aplicación, Verificar Construcción y Funcionamiento

Dockeriza tu aplicación NestJS (preferiblemente un servicio REST o GraphQL sin dependencias).
Asegúrate de que la imagen puede ser compilada con el siguiente comando:
bash
docker login
docker build -t byotony/webhooks:latest .
Verifica el funcionamiento de la aplicación.
![Alt text](img/image9.png)
![Alt text](img/image10.png)


Tambien hacemos el push

![Alt text](img/image11.png)

Y ya para terminar hacemos el commit para que se hagan los builds automáticamente cuando realizemos un commit nuevo al repositorio.

![Alt text](img/image12.png)

### 7. Crear Action Docker Image
Configura un flujo de trabajo en GitHub Actions para generar la imagen Docker utilizando el archivo docker-image.yml.

![Alt text](img/image13.png)


# Evidencias

Ya tenemos el actions creado para realizar builds automáticos.
![Alt text](img/image14.png)


