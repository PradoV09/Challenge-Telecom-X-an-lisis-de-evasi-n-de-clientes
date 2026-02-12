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
├── Telecom.ipynb               # Notebook principal con análisis ETL
├── json/
│   └── TelecomX_Data.json      # Datos de la API en formato JSON
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

- ✅ Carga e importación de datos
- ✅ Normalización de estructuras JSON
- ✅ Exploración inicial de variables
- ✅ Identificación de incoherencias (valores nulos y duplicados)
- ✅ Limpieza y transformación de datos
- ✅ Conversión de tipos de datos (cargos a float)
- ✅ Normalización de nombres de columnas
- ✅ Análisis descriptivo básico con estadísticas
- ✅ Visualizaciones gráficas (gráficos estadísticos)
- ✅ Cálculos de métricas (media, percentiles, distribuciones)
- 🔄 **En progreso**: Análisis exploratorio avanzado (EDA detallado)
- ⏳ Próximo: Análisis de correlaciones, segmentación y patrones de churn
- ⏳ Próximo: Análisis de correlaciones
- ⏳ Próximo: Modelado predictivo

## 💡 Insights Iniciales

- Dataset contiene información completa de clientes de Telecom X
- Los datos están estructurados en 4 dimensiones principales (cliente, teléfono, internet, cuenta)
- Se han identificado clientes con estado de churn para análisis posterior

## 📌 Notas Importantes

- Los datos están disponibles en formato JSON en el archivo `TelecomX_Data.json`
- Se recomienda consultar el diccionario de datos para comprender mejor cada variable
- El análisis es iterativo y se irá refinando conforme se exploren más patrones

## 👤 Autor

Jose Luis Prado Valencia

---

**Última actualización**: 12 de Febrero de 2026
