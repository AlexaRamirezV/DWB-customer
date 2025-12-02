# 👤 Customer Service (Negocio)

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
