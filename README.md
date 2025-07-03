# TelecomX_LATAM
Análisis de Evasión de Clientes
INFORME FINAL: ANÁLISIS DE CHURN Y ESTRATEGIAS DE RETENCIÓN
# 📊 INFORME FINAL: ANÁLISIS DE CHURN Y ESTRATEGIAS DE RETENCIÓN  
**Empresa:** TelecomX  
**Fecha:** `3 de julio de 2025`  
**Elaborado por:** `Iván Risco Barría`  
---

## Objetivo
El proyecto "Churn de Clientes" surge ante la necesidad de abordar una alta tasa de cancelaciones 'Churn' que afecta a la empresa. El objetivo es
comprender qué factores están asociados a la pérdida de clientes, a fin de tomar decisiones informadas.

Como parte del equipo, tu tarea consiste en recopilar, procesar y analizar los datos utilizando Python y sus principales bibliotecas de análisis.
A partir de estos hallazgos, el equipo de Data Science podrá avanzar en el desarrollo de modelos predictivos y diseñar estrategias efectivas para
reducir la tasa de evasión.

-   Carga de datos (JSON)
    Lectura de los datos desde un archivo JSON alojado en un repositorio remoto.

-   Normalización de datos
    Transformación de estructuras anidadas en un formato tabular utilizando pandas.json_normalize.

-   Verificación y limpieza de datos
    Detección y eliminación de valores nulos (NaN), vacíos ('') y registros duplicados para garantizar la calidad del dataset.

-   Conversión de tipos de datos
    Asignación de tipos de datos más eficientes (como category, int8, float32) para optimizar el uso de memoria y facilitar el análisis.

-   Análisis exploratorio y visualización
    Generación de gráficos y estadísticas descriptivas para identificar patrones relacionados con la cancelación del servicio (churn).

---

## 🔍 RESUMEN  
La empresa enfrenta una **alta tasa de abandono (Churn Rate: 26.54%)**, donde **1 de cada 4 clientes cancela su servicio**. Este informe identifica:  
- Factores clave que impulsan el abandono.  
- Segmentos de clientes de alto riesgo.  
- Estrategias concretas para reducir el Churn.  
--- 

## 📌 HALLAZGOS CLAVE  

### 1. Perfil del Cliente que Abandona  
| **Variable**         | **Retenidos (No)** | **Abandono (Yes)** | **Diferencia** |  
|----------------------|-------------------|-------------------|----------------|  
| **Charges.Monthly**  | $61.27           | $74.44            | ↑ **21.5%**    |  
| **SeniorCitizen**    | 12.87%           | 25.47%            | ↑ **12.6%**    |  
| **Tenure**           | 37.57 meses      | 17.98 meses       | ↓ **48%**      |  
| **Charges.Total**    | $2,555.34        | $1,531.80         | ↓ **40%**      |  

**🔎 Insights:**  
- Los clientes que abandonan pagan **+21.5% mensual** pero **-40% en total** (por menor permanencia).  
- **Senior Citizens abandonan 2× más** que otros grupos.  
- **Antigüedad baja (tenure)** es el predictor más fuerte de abandono.  

---

### 2. Contrato y Método de Pago  
#### 📜 Contrato  
- **Month-to-month**: Mayor abandono (ej: 994 cancelaciones).  
- **Two year**: Mínimo abandono (ej: solo 13 cancelaciones).  

#### 💳 Método de Pago  
- **Electronic check**: Peor desempeño (994 abandonos).  
- **Bank transfer (auto)**: Mejor retención (19 abandonos en 2 años).  

**🎯 Conclusión:**  
Clientes con contratos cortos y pagos manuales son los de **mayor riesgo**.  

---

### 3. Antigüedad (Tenure) vs. Churn  
- **Meses 0-6**: Alto riesgo (ej: 380 abandonos en Month-to-month).  
- **Meses 24+**: Clientes estables (casi 0 abandonos).  

---

## 🛠 ESTRATEGIAS DE RETENCIÓN  

| **Estrategia**                          | **Ejemplos de Acción**                                                                 | **Beneficio Esperado** |  
|-----------------------------------------|---------------------------------------------------------------------------|-----------------------|  
| **Migrar a contratos largos**           | Ofrecer **10-15% de descuento** para cambiar a 1-2 años.                  | ↓ 8-10% Churn         |  
| **Incentivar pagos automáticos**        | **5% de descuento** por usar Bank transfer/Credit card (auto).            | ↓ 12% abandonos       |  
| **Programa para Senior Citizens**       | Soporte prioritario + planes personalizados.                              | ↓ 7% Churn            |  
| **Campañas para clientes nuevos (<6m)** | Guías de uso + "1 mes gratis" al cumplir 6 meses.                         | ↑ 20% retención       |  

---

## 📈 MÉTRICAS DE ÉXITO PARA LOGROS
| **Objetivo**                     | **Meta (6 meses)** |  
|-----------------------------------|--------------------|  
| Reducir Churn Rate                | <20%               |  
| Aumentar contratos de 1-2 años   | +15%               |  
| Incrementar pagos automáticos     | +25%               |  

---

## ✅ CONCLUSIÓN  
**Principales causas del Churn:**  
1. Contratos cortos (`Month-to-month`).  
2. Pagos manuales (`Electronic check`).  
3. Baja antigüedad (`<12 meses`).  

**Recomendaciones clave:**  
- Implementar **estrategias segmentadas** (ej: descuentos para contratos largos).  
- Monitorear resultados con un **dashboard mensual**.  

--- 
## Tecnologías
---
 -  Python
 -  Jupyter Notebook 
 -  NumPy
 -  Pandas
 -  Seaborn
 -  Matplotlib
 -  Plotly

 ---

