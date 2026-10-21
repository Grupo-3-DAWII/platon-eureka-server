# platon-eureka-server

Eureka Server para registrar y descubrir los microservicios de Platon.

## Requisitos

- Java 21 o superior
- Maven 3.9 o superior

## Ejecutar

```bash
.\mvnw.cmd spring-boot:run
```

La consola de Eureka queda disponible en:

```text
http://localhost:8761
```

## Configuracion

- Nombre de aplicacion: `platon-eureka-server`
- Puerto: `8761`
- No se registra a si mismo como cliente Eureka
- No descarga el registro de otros servidores Eureka

## Orden recomendado

1. Levantar `platon-eureka-server`
2. Levantar `platon-microservice-account`
3. Levantar `platon-api-gateway`

Con eso, el gateway puede resolver `platon-microservice-account` usando Eureka.
