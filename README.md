# 👤 Customer Service

**Puerto:** `8082`
**Base de Datos:** `db_customer`

Ayuda a la gestión de perfiles de clientes (nombre, apellidos, RFC, , número de teléfono, dirección de envío, región).

**Nota: La dirección de envío es imprescindible, pues en `invoice-server` ocupamos esta dirección para generar la factura.**

## ⚠️ Nota Importante para Pruebas
**Sincronización de IDs:**
Al registrar un cliente, asegurarse de usar en el campo `user_id` el mismo ID que generó el **Auth-Service**.
*   *Ejemplo:* Si en Auth el usuario es ID 1, el Cliente aquí debe registrarse con `user_id: 1`.

## 🛠️ Base de Datos
```sql
CREATE DATABASE db_customer; -- Para clientes y regiones
```
---
### 🔗 Mapa de Arquitectura
0. [Config data](https://github.com/AlexaRamirezV/config-data.git)
1. [Config Server](https://github.com/AlexaRamirezV/config-service.git)
2.  [Registry Service (Eureka)](https://github.com/AlexaRamirezV/registry-service.git)
3.  [Gateway Service](https://github.com/AlexaRamirezV/gateway-service.git)
4.  [Admin Service](https://github.com/AlexaRamirezV/admin-service.git)
5.  APIs del sistema:
   * [Auth](https://github.com/AlexaRamirezV/DWB-auth.git)
   *  ➡️ **[Customer]**
   * [Product](https://github.com/xEriis/Backend.git)
   * [Invoice](https://github.com/AlexaRamirezV/DWB-invoice.git)
