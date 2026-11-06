# menu-service

Parte de **Arepa Express** (DOSW · Semana 14): API Gateway en Azure API Management y eventos con RabbitMQ. Spring Boot 4.1.2 · Java 21 · Maven.

Microservicio que expone el menú de la arepería.

## Endpoint

| Método | Ruta | Respuesta |
|---|---|---|
| GET | `/menu` | lista de arepas `{id, nombre, precio}` |

A través del gateway: `GET https://arepas-gw-kevina.azure-api.net/menu-api/menu` con el header `Ocp-Apim-Subscription-Key`.

## Cómo ejecutarlo

```bash
./mvnw spring-boot:run          # local (puerto 8080)
./mvnw -q package -DskipTests   # genera target/*.jar
docker build -t menu-service .           # imagen con el Dockerfile del repo
```
