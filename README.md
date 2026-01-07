# Hub de Infraestructura - Microservicios Clean Architecture

Este repositorio centraliza toda la infraestructura necesaria (Bases de Datos y Mensajería) para el ecosistema de microservicios. Al centralizar estos servicios, aseguramos que todos los microservicios (Users, Orders, Payments) puedan comunicarse entre sí a través de una red común y un broker de mensajes compartido.

## Servicios Incluidos

1.  **RabbitMQ (Shared Broker)**: Puerto `5672`. Es el corazón de la comunicación asíncrona. Todos los microservicios se conectan aquí para publicar y escuchar eventos.
2.  **MongoDB (Users)**: Puerto `27017`. Base de datos dedicada para el microservicio de Usuarios.
3.  **MongoDB (Orders)**: Puerto `27018`. Base de datos dedicada para el microservicio de Pedidos.
4.  **MongoDB (Payments)**: Puerto `27019`. Base de datos dedicada para el microservicio de Pagos.

## Requisitos Previos

- Docker
- Docker Compose

## Cómo Iniciar

Clona este repositorio y ejecuta el siguiente comando para levantar toda la infraestructura:

```bash
docker compose up -d
