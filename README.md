# 📊 Challenge Telecom X: Análisis de Evasión de Clientes

## 📝 Descripción del Proyecto

Este proyecto es un análisis integral de **evasión de clientes (Churn)** para Telecom X. El objetivo es identificar patrones y factores que influyen en la decisión de los clientes de abandonar el servicio, proporcionando insights accionables para mejorar la retención de clientes.

## 🎯 Objetivos Principales

- 🔍 **Explorar y caracterizar** el conjunto de datos de clientes de Telecom X
- 📊 **Identificar patrones** asociados con la evasión de clientes
- 📈 **Analizar variables clave** como tipo de contrato, servicio, método de pago y cargos
- 💡 **Generar insights** que permitan tomar decisiones estratégicas para reducir el churn
- 🛠️ **Preparar datos** para futuros modelos de predicción

## 📁 Estructura del Proyecto

```
.
├── README.md                    # Este archivo
├── requirements.txt             # Dependencias del proyecto
├── Telecom.ipynb                # Notebook principal con análisis ETL
├── json/
│   └── TelecomX_Data.json       # Datos de la API en formato JSON
└── env/                         # Entorno virtual de Python
```

## 📦 Requisitos

- **Python 3.8+**
- **pandas**: Manipulación y análisis de datos
- **Jupyter**: Entorno interactivo para análisis

Para instalar las dependencias:

```bash
pip install -r requirements.txt
```

## 🚀 Cómo Ejecutar

1. **Activar el entorno virtual**:

   ```bash
   env\Scripts\activate  # En Windows
   ```

2. **Ejecutar el Jupyter Notebook**:

   ```bash
   jupyter notebook Telecom.ipynb
   ```

3. **Seguir las secciones ETL**:
   - ✅ **Extract (E)**: Cargar datos desde la API JSON
   - ✅ **Transform (T)**: Limpiar, normalizar y explorar los datos
   - ✅ **Load (L)**: Preparar datos para análisis posterior

## 📊 Estructura de Datos

### Fuentes de Datos

Los datos se cargan desde `json/TelecomX_Data.json` y se normalizan en las siguientes categorías:

| Categoría    | Descripción                                 |
| ------------ | ------------------------------------------- |
| **customer** | Información demográfica del cliente         |
| **phone**    | Detalles del servicio telefónico contratado |
| **internet** | Información del servicio de internet        |
| **account**  | Detalles de la cuenta y facturación         |

### Variables Clave

- `customerID`: Identificador único del cliente
- `Churn`: Variable objetivo (sí/no - indica si el cliente se fue)
- `Contract`: Tipo de contrato (mes a mes, anual, bienal)
- `PaperlessBilling`: Si utiliza facturación sin papel
- `PaymentMethod`: Método de pago utilizado
- `Charges.Monthly`: Cargo mensual
- `Charges.Total`: Cargo total acumulado

## 📈 Metodología

El análisis sigue el enfoque **ETL** (Extract, Transform, Load):

1. **Extract**: Importación de datos JSON desde la API
2. **Transform**:
   - Normalización de estructuras anidadas
   - Validación de integridad de datos
   - Identificación de valores ausentes y duplicados
   - Exploración de inconsistencias en categorías
3. **Load**: Preparación de datos listos para análisis y modelado

## � Contenido del Notebook

### Sección 1: Extracción (Extract)

- Importación de datos desde `json/TelecomX_Data.json`
- Visualización de estructura inicial
- Obtención de dimensiones del dataset

### Sección 2: Transformación (Transform)

- **Normalización de estructuras anidadas:**
  - `customer_df`: Datos demográficos
  - `phone_df`: Servicios telefónicos
  - `internet_df`: Servicios de internet
  - `account_df`: Información de cuenta
- **Creación de DataFrame unificado** (`df_flat`)
- **Selección de columnas relevantes:** 15 variables clave para análisis
- **Conversión de tipos de datos:** Cargos convertidos a float64

### Sección 3: Validación y Limpieza de Datos

- Verificación de valores nulos (`isnull()`, `isna()`)
- Rellenado de valores faltantes
- Identificación y conteo de registros duplicados
- Normalización de nombres de columnas (minúsculas y reemplazar puntos)

### Sección 4: Análisis Descriptivo

- Cálculo de estadísticas descriptivas
- Visualizaciones gráficas de distribuciones
- Análisis de métricas clave (`media`, `percentiles`, etc.)
- Exploración de patrones en variables de churn

## 🔧 Estado del Proyecto

**✅ PROYECTO COMPLETADO**

### Etapas Completadas:

- ✅ Carga e importación de datos (7,043 registros)
- ✅ Normalización de estructuras JSON anidadas
- ✅ Exploración y caracterización de variables
- ✅ Identificación y manejo de incoherencias
- ✅ Limpieza y transformación de datos
- ✅ Conversión de tipos de datos
- ✅ Análisis descriptivo completo
- ✅ Visualizaciones gráficas (histogramas, barras, box plots)
- ✅ Análisis exploratorio de datos (EDA) detallado
- ✅ Análisis de variables categóricas y numéricas
- ✅ Identificación de patrones de churn
- ✅ Informe ejecutivo final con conclusiones e insights
- ✅ Recomendaciones estratégicas basadas en datos

---

## 🎯 Resultados Principales

### Hallazgos Clave Descubiertos:

1. **Factor Más Determinante**: Tipo de contrato
   - Contratos mes a mes: 5-6x mayor churn
   - Contratos bianuales: Máxima retención

2. **Ventana Critical Risk**: Primeros 12 meses
   - Clientes que abandonan: < 12 meses de antigüedad
   - Clientes leales: > 24 meses de antigüedad

3. **Fricción en Pagos**: Método de pago impacta retención
   - Métodos manuales: Mayor churn
   - Métodos automáticos: Menor churn

4. **Planes Premium Riesgo**: Clientes de cargos altos
   - Mayor propensión a cambiar de proveedor
   - Brecha entre precio y valor percibido

### Recomendaciones Priorizadas:

- 🔴 Incentivos para contratos a largo plazo (Impacto: 25-35% reducción churn)
- 🔴 Programa agresivo de retención en año 1 (Impacto: +20% retención)
- 🔴 Automatización de métodos de pago (Impacto: 10-15% reducción friction)
- 🟡 Auditoría de propuesta de valor para planes premium
- 🟡 Dashboard predictivo de churn

---

## 📋 Tabla de Contenidos del Notebook

1. **Introducción** - Contexto y objetivos del análisis
2. **Limpieza y Tratamiento de Datos** - Proceso ETL detallado
3. **Análisis Exploratorio de Datos (EDA)** - Visualizaciones y patrones
4. **Conclusiones e Insights** - Hallazgos principales documentados
5. **Recomendaciones Estratégicas** - Acciones priorizadas por impacto

---

## 💡 Valor Generado

✨ **Este análisis proporciona a Telecom X:**

- Comprensión profunda de factores que impulsan la evasión
- Identificación de segmentos de alto riesgo
- Estrategias accionables para reducir churn
- Base para futuros modelos predictivos
- ROI estimado de 25-35% reducción en tasa de churn

## 📌 Notas Importantes

- Los datos están disponibles en formato JSON en el archivo `TelecomX_Data.json`
- Se recomienda consultar el diccionario de datos para comprender mejor cada variable
- El análisis es iterativo y se irá refinando conforme se exploren más patrones

## 👤 Autor

Jose Luis Prado Valencia

---

**Última actualización**: 12 de Febrero de 2026
