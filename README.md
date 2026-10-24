# platon-eureka-server

Eureka Server para registrar y descubrir los microservicios de Platon.

## Requisitos

Elige una de las dos formas de ejecutarlo:

- **Local:** Java 25 (Maven no hace falta, el proyecto incluye `mvnw`).
- **Docker:** Docker con Compose.

## Ejecutar

Desde la carpeta del proyecto:

```bash
# Con Maven Wrapper (Linux/macOS)
./mvnw spring-boot:run

# Con Maven Wrapper (Windows)
.\mvnw.cmd spring-boot:run

# Con Docker
docker compose up -d --build
```

Consola de Eureka: <http://localhost:8761>

Con Docker, para ver logs y detener:

```bash
docker compose logs -f app
docker compose down
```

## Configuración

- Nombre de la aplicación: `platon-eureka-server`
- Puerto: `8761` (se puede cambiar con la variable `SERVER_PORT`)
- No se registra a sí mismo ni descarga el registro de otros servidores Eureka

## Orden recomendado

1. `platon-eureka-server`
2. `platon-config-server`
3. Microservicios
4. `platon-api-gateway`
