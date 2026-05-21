# AS25_Praqctica

# Sistema Web Desplegado en AWS EC2 con Docker

## Integrante

- Cristhian Julian

---

# Descripción del Proyecto

Sistema web agroexportador desarrollado con:

- Frontend Angular
- Backend Spring Boot
- Base de datos SQL Server

La aplicación fue desplegada utilizando Docker y AWS EC2 en una arquitectura distribuida de 3 servidores independientes.

---

# Arquitectura Utilizada

| Servidor | Servicio |
|---|---|
| EC2 #1 | SQL Server |
| EC2 #2 | Backend Spring Boot |
| EC2 #3 | Frontend Angular |

Comunicación realizada mediante IPs públicas AWS.

---

# Tecnologías Utilizadas

## Frontend
- Angular
- TypeScript
- NGINX
- Docker

## Backend
- Spring Boot
- Java
- Maven
- Docker

## Base de Datos
- SQL Server
- Docker

## Cloud
- AWS EC2
- Elastic IP
- Security Groups

---

# Código Fuente

## Frontend
Ruta:

```text
/frontend
```

## Backend
Ruta:

```text
/backend
```

## Configuración SQL
Ruta:

```text
/sql
```

## Dockerfiles
Incluidos en frontend y backend.

---

# Documentación Técnica

## Manual de Implementación

Disponible en:

```text
/docs/manual-implementacion.pdf
```

## Arquitectura Utilizada

Arquitectura distribuida en 3 instancias EC2.

## Explicación de Puertos

| Puerto | Uso |
|---|---|
| 80 | Frontend Angular |
| 8085 | Backend Spring Boot |
| 1433 | SQL Server |
| 22 | SSH |

---

# Security Groups

## EC2 Frontend
- 80
- 22

## EC2 Backend
- 8085
- 22

## EC2 SQL Server
- 1433
- 22

---

# Variables de Entorno Utilizadas

## Backend

```properties
DATABASE_URL
DATABASE_USERNAME
DATABASE_PASSWORD
DATABASE_DRIVER
PORT
SERVER_URL
```

---

# Pasos de Despliegue

## 1. Instalar Docker

```bash
sudo apt update

sudo apt install docker.io docker-compose-v2 -y
```

---

## 2. Construir Imágenes

### Backend

```bash
docker build -t cristhianyj/springboot-sqlserver:1.0 .
```

### Frontend

```bash
docker build -t cristhianyj/angular-frontend:1.0 .
```

---

## 3. Subir a Docker Hub

```bash
docker push cristhianyj/springboot-sqlserver:1.0

docker push cristhianyj/angular-frontend:1.0
```

---

## 4. Desplegar Contenedores

```bash
docker compose up -d
```

---

# Comandos Docker Utilizados

## Ver contenedores

```bash
docker ps
```

## Ver imágenes

```bash
docker images
```

## Ver logs

```bash
docker logs -f nombre-contenedor
```

## Descargar imágenes

```bash
docker pull nombre-imagen
```

---

# Evidencias

## Capturas de Pantalla

<img width="1406" height="645" alt="image" src="https://github.com/user-attachments/assets/fc2b7ee1-5174-4ce2-acd1-3c8ef793f254" />
<img width="1148" height="841" alt="image" src="https://github.com/user-attachments/assets/6ab1f125-e2e9-4df4-97fd-3d3946c51ae3" />
<img width="1097" height="763" alt="image" src="https://github.com/user-attachments/assets/83f6c4d6-d2f7-448c-97f0-fa6fb00dc5e9" />




Ubicación:

```text
/docs/capturas
```

## Evidencias Incluidas

- docker ps
- Frontend funcionando
- Backend funcionando
- SQL Server funcionando
- Docker Hub
- Comunicación entre servicios

---

# Evidencia de Funcionamiento

## Frontend

```text
http://IP_FRONTEND
```

## Backend

```text
http://IP_BACKEND:8085
```

---

# Imágenes Docker Hub

## Backend

```text
cristhianyj/springboot-sqlserver:1.0
```

## Frontend

```text
cristhianyj/angular-frontend:1.0
```

## SQL Server

```text
cristhianyj/sql-server:2022
```

---

# Resultado Final

Sistema desplegado exitosamente utilizando:

- Docker
- Docker Compose
- AWS EC2
- Angular
- Spring Boot
- SQL Server
- Docker Hub
