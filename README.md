# Proyecto Juanma (Creditos a Lander y Santiago por la creacion de esta pagina web)


Este proyecto es una aplicación web full-stack que utiliza Docker para su despliegue. Consiste en un frontend desarrollado con Vue.js/Vite y un backend en Node.js con una base de datos MySQL.

## Requisitos Previos

- Docker
- Docker Compose
- Git

## Estructura del Proyecto

```
.
├── Frontend/          # Aplicación frontend (Vue.js/Vite)
├── Backend/           # Servidor backend (Node.js)
└── docker-compose.yml # Configuración de Docker Compose
```

## Configuración y Ejecución

1. Clonar el repositorio:
   ```bash
   git clone <url-del-repositorio>
   cd ProyectoRomito
   ```

2. Iniciar los contenedores con Docker Compose:
   ```bash
   docker-compose up --build
   ```

   Este comando construirá e iniciará tres servicios:
   - Frontend (accesible en http://localhost:5173)
   - Backend (API en http://localhost:5174)
   - Base de datos MySQL (puerto 3306)

3. Para detener los servicios:
   ```bash
   docker-compose down
   ```

## Servicios

### Frontend
- Puerto: 5173
- URL: http://localhost:5173
- Tecnologías: Vue.js, Vite, TypeScript, Tailwind CSS

### Backend
- Puerto: 5174
- URL API: http://localhost:5174/api
- Tecnologías: Node.js, Express

### Base de Datos
- Puerto: 3306
- Base de datos: pelisdb
- Usuario: root
- Contraseña: secret


## Notas Importantes

- La base de datos se inicializa automáticamente con el esquema proporcionado en `Backend/db/database.sql`
- Los datos de la base de datos se persisten en un volumen de Docker
- El frontend está configurado para comunicarse con el backend a través de la URL especificada en las variables de entorno