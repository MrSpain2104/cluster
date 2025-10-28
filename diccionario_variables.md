# Diccionario de Variables - Dataset de Tarjetas de Crédito

## Contexto del Dataset

Este caso requiere desarrollar una segmentación de clientes para definir estrategias de marketing. El dataset resume el comportamiento de uso de aproximadamente 9,000 titulares activos de tarjetas de crédito durante los últimos 6 meses. Los datos están a nivel de cliente con 18 variables de comportamiento.

---

## Variables del Dataset

| Variable Original | Variable en Español | Tipo | Descripción |
|-------------------|---------------------|------|-------------|
| `CUST_ID` | `ID_CLIENTE` | Categórica | Identificador único del titular de la tarjeta de crédito |
| `BALANCE` | `SALDO` | Numérica | Monto de saldo restante en la cuenta para realizar compras |
| `BALANCE_FREQUENCY` | `FRECUENCIA_SALDO` | Numérica (0-1) | Frecuencia con la que se actualiza el saldo. 1 = actualizado frecuentemente, 0 = no actualizado frecuentemente |
| `PURCHASES` | `COMPRAS` | Numérica | Monto total de compras realizadas desde la cuenta |
| `ONEOFF_PURCHASES` | `COMPRAS_UNICAS` | Numérica | Monto máximo de compra realizado en una sola transacción |
| `INSTALLMENTS_PURCHASES` | `COMPRAS_CUOTAS` | Numérica | Monto de compras realizadas en cuotas/plazos |
| `CASH_ADVANCE` | `ADELANTO_EFECTIVO` | Numérica | Adelanto de efectivo solicitado por el usuario |
| `PURCHASES_FREQUENCY` | `FRECUENCIA_COMPRAS` | Numérica (0-1) | Frecuencia con la que se realizan compras. 1 = compras frecuentes, 0 = compras no frecuentes |
| `ONEOFF_PURCHASES_FREQUENCY` | `FRECUENCIA_COMPRAS_UNICAS` | Numérica (0-1) | Frecuencia de compras realizadas en una sola transacción. 1 = frecuente, 0 = no frecuente |
| `PURCHASES_INSTALLMENTS_FREQUENCY` | `FRECUENCIA_COMPRAS_CUOTAS` | Numérica (0-1) | Frecuencia de compras en cuotas. 1 = frecuente, 0 = no frecuente |
| `CASH_ADVANCE_FREQUENCY` | `FRECUENCIA_ADELANTO_EFECTIVO` | Numérica (0-1) | Frecuencia con la que se paga adelanto de efectivo |
| `CASH_ADVANCE_TRX` | `NUM_TRX_ADELANTO_EFECTIVO` | Numérica (entera) | Número de transacciones realizadas con "Adelanto de Efectivo" |
| `PURCHASES_TRX` | `NUM_TRX_COMPRAS` | Numérica (entera) | Número de transacciones de compra realizadas |
| `CREDIT_LIMIT` | `LIMITE_CREDITO` | Numérica | Límite de crédito de la tarjeta para el usuario |
| `PAYMENTS` | `PAGOS` | Numérica | Monto de pagos realizados por el usuario |
| `MINIMUM_PAYMENTS` | `PAGOS_MINIMOS` | Numérica | Monto mínimo de pagos realizados por el usuario |
| `PRC_FULL_PAYMENT` | `PORC_PAGO_COMPLETO` | Numérica (0-1) | Porcentaje del pago completo realizado por el usuario |
| `TENURE` | `ANTIGUEDAD` | Numérica (entera) | Antigüedad del servicio de tarjeta de crédito para el usuario (en meses) |

---

## Notas Importantes

- **Variables de Frecuencia (0-1)**: Todas las variables que tienen "FREQUENCY" en su nombre original son scores entre 0 y 1, donde 1 indica alta frecuencia y 0 indica baja frecuencia.
- **Valores Faltantes**: Las variables `MINIMUM_PAYMENTS` y `CREDIT_LIMIT` tienen algunos valores faltantes que deben ser imputados.
- **Outliers**: Variables como `BALANCE`, `PURCHASES`, `CASH_ADVANCE`, `PAYMENTS` contienen outliers significativos que deben ser tratados.
- **Periodo de Análisis**: 6 meses de datos de comportamiento.

---

## Variables Clave para Clustering

Las variables más relevantes para segmentación suelen ser:
1. **SALDO** - Indica capacidad de gasto disponible
2. **COMPRAS** - Indica nivel de actividad de compras
3. **ADELANTO_EFECTIVO** - Indica necesidad de liquidez inmediata
4. **LIMITE_CREDITO** - Indica perfil crediticio del cliente
5. **PAGOS** - Indica comportamiento de pago
6. **PAGOS_MINIMOS** - Indica responsabilidad financiera
7. **PORC_PAGO_COMPLETO** - Indica si paga el total o solo el mínimo
8. **Frecuencias diversas** - Indican patrones de uso regular vs esporádico
