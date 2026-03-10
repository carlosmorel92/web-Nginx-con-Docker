# Servidor Web Nginx con Docker Compose

## Descripción

Este proyecto consiste en crear un servidor web utilizando **Nginx** ejecutándose en un contenedor Docker mediante **Docker Compose**.
El servidor sirve una página web simple con un mensaje **"Hola mundo"**.

El contenido del sitio web se encuentra en un directorio local (`src`) que está montado como volumen dentro del contenedor.

---

## Estructura del proyecto

```
nginx-docker/
│
├── docker-compose.yml
│
└── src/
    └── index.html
```

---

## Requisitos

Antes de ejecutar el proyecto debes tener instalado:

* Docker
* Docker Compose
* Git (opcional, para control de versiones)

---

## Instalación y ejecución

1. Clonar el repositorio

```bash
git clone https://github.com/TU-USUARIO/nginx-docker-compose.git
```

2. Entrar al directorio del proyecto

```bash
cd nginx-docker-compose
```

3. Ejecutar el contenedor

```bash
docker compose up -d
```

---

## Verificar funcionamiento

Abrir el navegador y acceder a:

```
http://localhost:8080
```

Deberías ver el mensaje:

```
Hola mundo
```

---

## Explicación

El archivo `docker-compose.yml` define un servicio con la imagen oficial de **nginx** y realiza lo siguiente:

* Expone el puerto **8080** del host al **80** del contenedor
* Monta el directorio `src` en `/usr/share/nginx/html`

Esto permite que Nginx sirva el archivo `index.html` desde tu máquina local.

---

## Autor

Proyecto realizado como práctica de Docker Compose.
