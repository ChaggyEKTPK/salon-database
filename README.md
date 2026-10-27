# 💇‍♀️ Salon Appointment Scheduler

Programa de citas para un salón de belleza en **Bash + PostgreSQL**, con menú interactivo. Proyecto del currículo [Relational Database de freeCodeCamp](https://www.freecodecamp.org/).

## Flujo del programa

1. Muestra los servicios disponibles (`service_id` + nombre)
2. Pide el ID del servicio y lo valida en bucle hasta ser correcto
3. Pide el número de teléfono del cliente:
   - Si existe → saluda al cliente con su nombre
   - Si no existe → pide su nombre y lo registra
4. Registra la cita en la tabla `appointments`

## Esquema de la base de datos

| Tabla | Columnas |
|---|---|
| `customers` | `customer_id`, `name`, `phone` |
| `services` | `service_id`, `name` |
| `appointments` | `appointment_id`, `customer_id`, `service_id`, `time` |

Las tres tablas están relacionadas con claves foráneas.

## Tecnologías

- Bash (`psql`, funciones, bucles `while`)
- PostgreSQL

## Notas técnicas

⚠️ Versión original usa interpolación de strings en las queries (suficiente para FCC). Una mejora pendiente: usar consultas parametrizadas para prevenir inyección SQL.
