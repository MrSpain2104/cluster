---
layout: default
title: Home
---

<div align="center">
  <img src="image.png" alt="Credit Card Analytics" width="300" style="border-radius: 15px; margin: 20px 0; box-shadow: 0 4px 6px rgba(0,0,0,0.1);"/>
</div>

# 🎯 Segmentación de Clientes de Tarjetas de Crédito

## Proyecto de Machine Learning - Clustering

> **Objetivo:** Identificar perfiles de comportamiento financiero en una cartera de ~9,000 clientes mediante técnicas de clustering no supervisado (K-Means + PCA).

---

## 🚀 Vista Rápida del Proyecto

Este proyecto aplica técnicas de **ciencia de datos** y **machine learning** para segmentar clientes de tarjetas de crédito y generar insights accionables para estrategias de negocio.

### Datos
- **~9,000 clientes** analizados
- **18 variables** de comportamiento financiero
- **6 meses** de historial transaccional

### Técnicas Aplicadas
- Análisis Exploratorio de Datos (EDA)
- Ingeniería de características
- Imputación robusta (KNN)
- Reducción de dimensionalidad (PCA)
- Clustering K-Means optimizado
- ✅ Validación con Silhouette Score y Calinski-Harabasz

---

## 📁 Estructura del Repositorio

```
📦 cluster/
├── 📊 CC GENERAL.csv                    # Dataset original
├── 📓 CC_GENERAL_analysis.ipynb         # Análisis exploratorio completo
├── 📓 CC_GENERAL_modelado.ipynb         # Modelado y clustering
├── 📄 CC_GENERAL_clustered.csv          # Resultados con clusters
├── 📖 diccionario_variables.md          # Diccionario de variables
├── 📋 requirements.txt                  # Dependencias Python
├── 🖼️ image.png                          # Logo del proyecto
└── 📝 README.md                         # Documentación
```

---

## 🔍 Hallazgos Principales

### Segmentos Identificados

El análisis reveló **4 perfiles diferenciados** de clientes:

<div style="margin: 20px 0;">
  <div style="background: linear-gradient(135deg, #E8F5E9, #C8E6C9); padding: 15px; border-radius: 8px; margin: 10px 0;">
    <h4>🟢 Cluster 0: Usuarios Conservadores (~25%)</h4>
    <ul>
      <li>Bajo uso de crédito</li>
      <li>Pagos responsables</li>
      <li>Baja actividad transaccional</li>
    </ul>
    <p><strong>💡 Estrategia:</strong> Cross-selling y aumento de límite</p>
  </div>
  
  <div style="background: linear-gradient(135deg, #E3F2FD, #BBDEFB); padding: 15px; border-radius: 8px; margin: 10px 0;">
    <h4>🔵 Cluster 1: Clientes Premium (~20%)</h4>
    <ul>
      <li>Alto límite de crédito</li>
      <li>Compras frecuentes de alto valor</li>
      <li>Excelente comportamiento de pago</li>
    </ul>
    <p><strong>💡 Estrategia:</strong> Retención con beneficios exclusivos</p>
  </div>
  
  <div style="background: linear-gradient(135deg, #FFF9C4, #FFF59D); padding: 15px; border-radius: 8px; margin: 10px 0;">
    <h4>🟡 Cluster 2: Usuarios Intermedios (~35%)</h4>
    <ul>
      <li>Uso moderado del crédito</li>
      <li>Balance entre compras y pagos</li>
      <li>Mayor oportunidad de crecimiento</li>
    </ul>
    <p><strong>💡 Estrategia:</strong> Up-selling e incentivos</p>
  </div>
  
  <div style="background: linear-gradient(135deg, #FFEBEE, #FFCDD2); padding: 15px; border-radius: 8px; margin: 10px 0;">
    <h4>🔴 Cluster 3: Alto Riesgo (~20%)</h4>
    <ul>
      <li>Alta utilización del crédito</li>
      <li>Dependencia de adelantos</li>
      <li>Pagos mínimos frecuentes</li>
    </ul>
    <p><strong>💡 Estrategia:</strong> Mitigación de riesgo y consolidación</p>
  </div>
</div>

---

## 💡 Insights de Negocio

### Variables Más Discriminantes

1. **🎯 Tasa de Utilización de Crédito** - Separa usuarios conservadores de agresivos
2. **📊 Frecuencia de Compras** - Identifica clientes activos vs. inactivos
3. **💳 Ratio de Pagos Mínimos** - Distingue comportamiento responsable vs. riesgoso
4. **💰 Intensidad de Adelantos** - Señala necesidad financiera

### Estrategias Accionables

| Segmento | Objetivo | Acciones Recomendadas |
|----------|----------|----------------------|
| 🟢 Conservadores | **Cross-selling** | Aumento de límite, beneficios por uso, recompensas |
| 🔵 Premium | **Retención** | Programas VIP, concierge, cashback exclusivo |
| 🟡 Intermedios | **Up-selling** | Incentivos temporales, campañas personalizadas |
| 🔴 Alto Riesgo | **Mitigación** | Consolidación, reducción de tasas, educación |
## Tecnologías Utilizadas

- **Python 3.x** - Lenguaje principal
- **Pandas & NumPy** - Manipulación de datos
- **Scikit-learn** - Machine Learning (K-Means, PCA, KNN Imputer)
- **Matplotlib & Seaborn** - Visualizaciones
- **Jupyter Notebook** - Análisis interactivo

---

## Métricas de Validación

| Métrica | Valor | Interpretación |
|---------|-------|----------------|
| **Silhouette Score** | 0.45 - 0.55 | Clusters bien diferenciados |
| **Calinski-Harabasz** | >1000 | Alta cohesión intra-cluster |
| **Varianza Explicada (PCA)** | 95% | Reducción dimensional efectiva |

---

## Documentación Adicional

- [Diccionario de Variables](diccionario_variables.md) - Descripción completa de todas las variables
- [Notebook de Análisis](CC_GENERAL_analysis.ipynb) - EDA completo con visualizaciones
- [Notebook de Modelado](CC_GENERAL_modelado.ipynb) - Clustering y validación

---

## Autor

**Andrés España**

Contact: [GitHub Profile](https://github.com/MrSpain2104)

---

<div align="center">
  <strong>⭐ Si este proyecto te resultó útil, considera darle una estrella en GitHub ⭐</strong>
</div>
