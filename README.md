# Test Manager Library - Infraestructura

Entorno Docker completo para orquestar la API (Laravel), la Base de Datos (PostgreSQL) y el Frontend (React).

## Requisitos previos
- Docker Desktop (Windows/Mac) o Docker Engine (Linux).
- Puertos libres: 8000, 5173, y 5432.

## Cómo arrancar la aplicación completa
Ejecuta el siguiente comando en la raíz de esta carpeta:

\\\ash
docker compose up -d --build
\\\

Este comando inicializa todo con 0 intervención manual:
1. \db\: Inicia PostgreSQL y lo deja listo para recibir conexiones.
2. \pi\: Instala las librerías de PHP, genera las claves de encriptación y JWT, ejecuta las migraciones de Base de Datos y siembra los datos semilla (Administrador y Categorías), para luego exponer el puerto 8000.
3. \pp\: Inicia el cliente React en el puerto 5173 apuntando automáticamente al API.
