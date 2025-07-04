# LTI - Talent Tracking System | EN

This project is a full-stack application with a React frontend and an Express backend using Prisma as an ORM. The frontend is started with Create React App, and the backend is written in TypeScript.

## Explanation of Directories and Files

- `backend/`: Contains the server-side code written in Node.js.
  - `src/`: Contains the source code for the backend.
    - `index.ts`: The entry point for the backend server.
    - `application/`: Contains the application logic.
    - `domain/`: Contains the business logic.
    - `infrastructure/`: Contains code that communicates with the database.
    - `presentation/`: Contains code related to the presentation layer (such as controllers).
    - `routes/`: Contains the route definitions for the API.
    - `tests/`: Contains test files.
  - `prisma/`: Contains the Prisma schema file for ORM.
  - `tsconfig.json`: TypeScript configuration file.
- `frontend/`: Contains the client-side code written in React."
  - `src/`: Contains the source code for the frontend.
  - `public/`: Contains static files such as the HTML file and images.
  - `build/`: Contains the production-ready build of the frontend.
- `.env`: Contains the environment variables.
- `docker-compose.yml`: Contains the Docker Compose configuration to manage your application's services.
- `README.md`: This file contains information about the project and instructions on how to run it.

## Project Structure

The project is divided into two main directories: `frontend` and `backend`.

### Frontend

The frontend is a React application, and its main files are located in the src directory. The public directory contains static assets, and the build directory contains the production build of the application.

### Backend

The backend is an Express application written in TypeScript. The src directory contains the source code, divided into several subdirectories:

- `application`: Contains the application logic.
- `domain`: Contains the domain models.
- `infrastructure`: Contains code related to the infrastructure.
- `presentation`: Contains code related to the presentation layer.
- `routes`: Contains the application routes.
- `tests`: Contains the application tests.

The `prisma` directory contains the Prisma schema.

## First steps

To get started with this project, follow these steps:

1. Clone the repository.
2. Install the dependencies for the frontend and backend:

```sh
cd frontend
npm install

cd ../backend
npm install
```
3. Build the backend server:
```sh
cd backend
npm run build
```
4. Start the backend server:
```sh
cd backend
npm start
```
5. In a new terminal window, build the frontend server:
```sh
cd frontend
npm run build
```
6. Start the frontend server:
```sh
cd frontend
npm start
```

The backend server will be running at http://localhost:3010 and the frontend will be available at http://localhost:3000.

## Docker and PostgreSQL

This project uses Docker to run a PostgreSQL database. Here's how to set it up:

Install Docker on your machine if you haven't done so already. You can download it from here.
Navigate to the root directory of the project in your terminal.
Run the following command to start the Docker container:

```sh
docker-compose up -d
```
This will start a PostgreSQL database in a Docker container. The -d flag runs the container in detached mode, which means it runs in the background.

To stop the Docker container, run the following command:

```sh
docker-compose down
```
To generate the database using Prisma, follow these steps:

```sh
npx prisma migrate dev
npx prisma db seed
```

Once you have completed all the steps, you should be able to save new candidates, both via web and via API, view them in the database, and retrieve them using GET by ID.

```sh
curl -X GET http://localhost:3010/candidates/1
```

--------------------------------------------

# LTI - Sistema de Seguimiento de Talento | ES

Este proyecto es una aplicación full-stack con un frontend en React y un backend en Express usando Prisma como un ORM. El frontend se inicia con Create React App y el backend está escrito en TypeScript.

## Explicación de Directorios y Archivos

- `backend/`: Contiene el código del lado del servidor escrito en Node.js.
  - `src/`: Contiene el código fuente para el backend.
    - `index.ts`: El punto de entrada para el servidor backend.
    - `application/`: Contiene la lógica de aplicación.
    - `domain/`: Contiene la lógica de negocio.
    - `infrastructure/`: Contiene código que se comunica con la base de datos.
    - `presentation/`: Contiene código relacionado con la capa de presentación (como controladores).
    - `routes/`: Contiene las definiciones de rutas para la API.
    - `tests/`: Contiene archivos de prueba.
  - `prisma/`: Contiene el archivo de esquema de Prisma para ORM.
  - `tsconfig.json`: Archivo de configuración de TypeScript.
- `frontend/`: Contiene el código del lado del cliente escrito en React.
  - `src/`: Contiene el código fuente para el frontend.
  - `public/`: Contiene archivos estáticos como el archivo HTML e imágenes.
  - `build/`: Contiene la construcción lista para producción del frontend.
- `.env`: Contiene las variables de entorno.
- `docker-compose.yml`: Contiene la configuración de Docker Compose para gestionar los servicios de tu aplicación.
- `README.md`: Este archivo, contiene información sobre el proyecto e instrucciones sobre cómo ejecutarlo.

## Estructura del Proyecto

El proyecto está dividido en dos directorios principales: `frontend` y `backend`.

### Frontend

El frontend es una aplicación React y sus archivos principales están ubicados en el directorio `src`. El directorio `public` contiene activos estáticos y el directorio `build` contiene la construcción de producción de la aplicación.

### Backend

El backend es una aplicación Express escrita en TypeScript. El directorio `src` contiene el código fuente, dividido en varios subdirectorios:

- `application`: Contiene la lógica de aplicación.
- `domain`: Contiene los modelos de dominio.
- `infrastructure`: Contiene código relacionado con la infraestructura.
- `presentation`: Contiene código relacionado con la capa de presentación.
- `routes`: Contiene las rutas de la aplicación.
- `tests`: Contiene las pruebas de la aplicación.

El directorio `prisma` contiene el esquema de Prisma.

## Primeros Pasos

Para comenzar con este proyecto, sigue estos pasos:

1. Clona el repositorio.
2. Instala las dependencias para el frontend y el backend:
```sh
cd frontend
npm install

cd ../backend
npm install
```
3. Construye el servidor backend:
```sh
cd backend
npm run build
```
4. Inicia el servidor backend:
```sh
cd backend
npm start
```
5. En una nueva ventana de terminal, construye el servidor frontend:
```sh
cd frontend
npm run build
```
6. Inicia el servidor frontend:
```sh
cd frontend
npm start
```

El servidor backend estará corriendo en http://localhost:3010 y el frontend estará disponible en http://localhost:3000.

## Docker y PostgreSQL

Este proyecto usa Docker para ejecutar una base de datos PostgreSQL. Así es cómo ponerlo en marcha:

Instala Docker en tu máquina si aún no lo has hecho. Puedes descargarlo desde aquí.
Navega al directorio raíz del proyecto en tu terminal.
Ejecuta el siguiente comando para iniciar el contenedor Docker:
```sh
docker-compose up -d
```

Para detener el contenedor Docker, ejecuta el siguiente comando:
```sh
docker-compose down
```

Para generar la base de datos utilizando Prisma, sigue estos pasos:

```sh
npx prisma migrate dev
npx prisma db seed
```

Una vez has dado todos los pasos, deberías poder guardar nuevos candidatos, tanto via web, como via API, verlos en la base de datos y obtenerlos mediante GET por id.

```sh
curl -X GET http://localhost:3010/candidates/1
```

