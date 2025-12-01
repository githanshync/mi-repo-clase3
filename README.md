# mi-repo-clase3
Tarea 3 curso docker kubernetes

**Curso:** Docker & Kubernetes - Clase 3

**Estudiante:** Hans Nava

Mi-repo-clase3 es un entorno que muestra una web estática en Nginx y permite administrar una base de datos Postgresql desde pgAdmin, todo con docker compose.

## Stack

- **App:** Nginx
- **Base de datos:** PostgreSQL

## Ejecución

1. Clonar:
   ```bash
   git clone https://github.com/githanshync/mi-repo-clase3.git
   cd mi-repo-clase3

2. Levantar servicios:
   ```bash
   docker compose up -d

![Docker Images](screenshots/docker-compose-up-d.png)

3.Acceder:

Mi Web: http://localhost:8082

![Docker Images](screenshots/web1.png)

Pgadmin: http://localhost:8083

![Docker Images](screenshots/web2.png)

### 4. Cómo Probar

## Verificación

1. Servicios corriendo:
   ```bash
   docker compose ps

![Docker Images](screenshots/docker-ps.png)

2. Acceder a la web: http://localhost:8082

3. Verificar volumen persiste:
   ```bash
   docker compose down
   docker compose up -d
   docker volume ls
   
![Docker Images](screenshots/volumen-persiste.png)

### 5. Capturas de Pantalla

## Screenshots

### Servicios corriendo
![compose ps](screenshots/docker-ps.png)

### API funcionando
![API](screenshots/web1.png)

![API](screenshots/web2.png)

## Conceptos Docker

- Docker Compose con 3 servicios
- Red custom: `mi-repo-clase3_backend` y `mi-repo-clase3_frontend`
- Volumen: `mi-repo-clase3_db_data` (persistencia)
- Variables de entorno: POSTGRES_USER, POSTGRES_PASSWORD y POSTGRES_DB
  
## Opcional:

docker network ls mostrando la red custom

![network](screenshots/docker-network-ls.png)

docker exec haciendo ping entre servicios

![servicios](docker-compose-exec-pgadmin-ping-db.png)

![servicios](curl-pgadmin.png)
