## 📌 Favoritos
| Atributo        | Descripción |
|-----------------|-------------|
| id_telegram     | Identificador del usuario en Telegram |
| mail            | Correo electrónico del usuario |
| ticket          | Ticker de la acción |
| active          | Indica si el favorito está activo |

---

## 📌 Órdenes Programadas
| Atributo              | Descripción |
|-----------------------|-------------|
| id_orden              | Identificador único de la orden |
| user_telegram_id      | Identificador del usuario en Telegram |
| ticker                | Ticker del activo |
| orden                 | Tipo de orden (BUY / SELL) |
| tipo_orden            | Tipo de ejecución (LIMIT / MARKET) |
| precio_objetivo       | Precio objetivo para órdenes LIMIT |
| cantidad              | Cantidad de activos |
| precio_operacion      | Precio al que se ejecutó la orden |
| estado                | Estado de la orden |
| fecha_creacion        | Fecha de creación de la orden |
| fecha_ejecucion       | Fecha de ejecución de la orden |

---

## 📌 Portfolio
| Atributo         | Descripción |
|------------------|-------------|
| id_portfolio     | Identificador del portfolio |
| user_telegram_id | Identificador del usuario en Telegram |
| ticker           | Ticker del activo |
| cantidad_total   | Cantidad total del activo |

---

## 📌 Transacciones
| Atributo              | Descripción |
|-----------------------|-------------|
| id_transaccion        | Identificador único de la transacción |
| id_orden              | Identificador de la orden asociada |
| user_telegram_id      | Identificador del usuario en Telegram |
| ticker                | Ticker del activo |
| orden                 | Tipo de orden (BUY / SELL) |
| tipo_orden            | Tipo de ejecución (LIMIT / MARKET) |
| precio_ejecucion      | Precio de ejecución |
| cantidad              | Cantidad ejecutada |
| monto_total           | Monto total de la transacción |
| fecha_hora            | Fecha y hora de la transacción |

---

## 📌 Usuarios
| Atributo          | Descripción |
|-------------------|-------------|
| user_telegram_id  | Identificador del usuario en Telegram |
| nombre_usuario    | Nombre del usuario |
| saldo_disponible  | Saldo disponible en la cuenta |
| fecha_registro    | Fecha de registro del usuario |
| estado            | Estado de la cuenta |
