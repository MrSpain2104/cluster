# Segmentación de clientes de tarjetas de crédito

Objetivo general:

> El objetivo de este proyecto es agrupar clientes de tarjetas de crédito según su comportamiento de uso, pagos y compras, con el fin de identificar distintos perfiles financieros y obtener insights accionables para estrategias de retención y personalización.

Objetivos específicos:
- Identificar patrones de comportamiento financiero (por ejemplo: compradores impulsivos, usuarios responsables, deudores frecuentes, etc.).
- Determinar variables que más influyen en la segmentación.
- Proponer estrategias de negocio basadas en los grupos detectados.

## Dataset

El dataset contiene **~9,000 clientes** con **18 variables de comportamiento** durante los últimos **6 meses**:

- Variables financieras: SALDO, COMPRAS, ADELANTO_EFECTIVO, LIMITE_CREDITO, PAGOS, PAGOS_MINIMOS
- Variables de frecuencia (0-1): Frecuencias de actualización de saldo, compras, adelantos, pagos
- Variables transaccionales: Número de transacciones de compras y adelantos
- Variables de comportamiento: Porcentaje de pago completo, antigüedad

Ver **`diccionario_variables.md`** para descripción completa de todas las variables.

## Contenido del repositorio

- `CC GENERAL.csv`: Dataset original con datos de comportamiento de clientes
- `CC_GENERAL_analysis.ipynb`: Notebook completo con análisis exploratorio, clustering y estrategias
- `diccionario_variables.md`: Diccionario completo de variables (inglés/español)
- `requirements.txt`: Dependencias necesarias
- `CC_GENERAL_clustered.csv`: Dataset con clusters asignados (generado al ejecutar el notebook)

## Estructura del análisis

1. **Carga y exploración inicial**: Inspección de datos, valores faltantes, estadísticas descriptivas
2. **EDA (Análisis Exploratorio)**: Distribuciones, outliers, correlaciones
3. **Preprocesamiento**: Imputación, escalado, PCA
4. **Clustering**: KMeans con evaluación de k óptimo (Silhouette + Calinski-Harabasz)
5. **Análisis de segmentos**: Perfiles de cada cluster, variables influyentes (ANOVA + PCA loadings)
6. **Estrategias de negocio**: Recomendaciones accionables por cluster

## Resultados esperados

- Identificación de 3-5 segmentos de clientes con comportamientos distintivos
- Variables más influyentes en la segmentación (ej: SALDO, COMPRAS, ADELANTO_EFECTIVO)
- Estrategias personalizadas de marketing y retención por segmento
- Dataset exportado con clusters asignados para uso en sistemas CRM

## Notas técnicas
- El análisis usa **KMeans** (simple y efectivo) y puede extenderse con DBSCAN o HDBSCAN
- PCA mantiene ~95% de varianza para reducir dimensionalidad
- Outliers tratados con capping (percentiles 1% y 99%)

