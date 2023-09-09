# Docker_simpliApi
Configuración de Docker Compose para Aplicaciones Multiplataforma

Este archivo Docker Compose se utiliza para implementar y orquestar tres servicios en contenedores Docker separados. Estos servicios son:
Servicio de Base de Datos (db)
Imagen: PostgreSQL (última versión)
Volúmenes: Permite persistir los datos de la base de datos en la carpeta local ./data/db.
Variables de Entorno:
 para las contraseñas de la base de datos:

markdown

# Docker Compose para Aplicaciones Multiplataforma

Este repositorio contiene un archivo Docker Compose que facilita la implementación de tres aplicaciones diferentes en contenedores Docker separados. Estas aplicaciones son:

1. **Base de Datos PostgreSQL**: Una instancia de PostgreSQL utilizada para almacenar datos relacionados con las aplicaciones.

2. **Aplicación Core en Node.js**: Una aplicación en Node.js que forma parte del núcleo de nuestra aplicación y ofrece servicios web.

3. **Script de Orden por Voz en FastAPI**: Un servicio de procesamiento de órdenes por voz implementado con FastAPI en Python.

## Requisitos previos

Antes de comenzar, asegúrate de tener Docker y Docker Compose instalados en tu sistema. Puedes encontrar instrucciones sobre cómo hacerlo en [el sitio web oficial de Docker](https://docs.docker.com/get-docker/) y [la documentación de Docker Compose](https://docs.docker.com/compose/install/).

## Configuración de Contraseñas de la Base de Datos

**Nota importante**: Para mantener las contraseñas de la base de datos seguras, debes crear un archivo `.env` en el mismo directorio que este archivo README y definir las variables de entorno para las contraseñas en ese archivo. Aquí hay un ejemplo de cómo debe verse el archivo `.env`:

```dotenv
POSTGRES_DB=bills_db
POSTGRES_USER=bills_user
POSTGRES_PASSWORD=Mathi142014

Las variables POSTGRES_DB, POSTGRES_USER, y POSTGRES_PASSWORD deben contener los valores correspondientes a tu configuración.
Uso

    Clona este repositorio en tu máquina local:

    bash

git clone https://github.com/tu-usuario/tu-repositorio.git

Navega al directorio raíz del repositorio clonado:

bash

cd tu-repositorio

Crea el archivo .env y define las variables de entorno para las contraseñas de la base de datos, como se explicó anteriormente.

Ejecuta el siguiente comando para iniciar las aplicaciones en contenedores:

bash

docker-compose up -d

Esto creará y ejecutará los contenedores necesarios en segundo plano. Puedes verificar el estado de los contenedores con docker ps.

Accede a las aplicaciones a través de los siguientes enlaces:

    Base de Datos PostgreSQL: No tiene una interfaz web, pero se utiliza para almacenar datos.
    Aplicación Core en Node.js: http://localhost:8000
    Script de Orden por Voz en FastAPI: http://localhost:8001

Cuando hayas terminado de usar las aplicaciones, puedes detener y eliminar los contenedores con el siguiente comando:

bash

    docker-compose down

Recuerda que debes mantener el archivo .env seguro y no compartirlo públicamente para proteger tus contraseñas de la base de datos. ¡Disfruta explorando estas aplicaciones en contenedores Docker!
