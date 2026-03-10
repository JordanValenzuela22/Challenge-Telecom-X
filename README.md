# 📉 Telecom X - Análisis de Evasión de Clientes (Churn)

## 📖 Descripción del Proyecto
Este proyecto de análisis de datos fue desarrollado para **Telecom X**, una empresa de telecomunicaciones que enfrenta una alta tasa de cancelación de servicios (Churn). El objetivo principal es recopilar, limpiar y analizar la información de los clientes para comprender los factores que motivan su salida. Los insights obtenidos servirán como base para que el equipo de Data Science desarrolle modelos predictivos y el área de negocio aplique estrategias de retención.

## 🎯 Objetivos
* Importar y procesar datos desde una API simulada (archivo JSON) con estructuras anidadas.
* Aplicar un proceso **ETL** (Extracción, Transformación y Carga) para asegurar la calidad de los datos.
* Realizar un **Análisis Exploratorio de Datos (EDA)** mediante visualizaciones para identificar patrones de comportamiento.
* Brindar recomendaciones estratégicas basadas en el cruce de variables categóricas y numéricas.

## 🛠️ Tecnologías Utilizadas
El análisis se ejecutó en un entorno de **Jupyter Notebook** (`.ipynb`) utilizando el ecosistema de Python para ciencia de datos:
* **Python 3.x**
* **Pandas:** Para manipulación, limpieza y aplanamiento de datos (`json_normalize`).
* **NumPy:** Para operaciones numéricas y manejo de valores nulos.
* **Matplotlib & Seaborn:** Para la creación de gráficos estadísticos (barras y mapas de calor).
* **JSON:** Para la lectura de la fuente de datos original.

## 📂 Estructura de los Datos
El dataset original (`TelecomX_Data.json`) contiene información de más de 7000 clientes. Algunas de las variables clave analizadas, según nuestro diccionario de datos, incluyen:
* `Churn`: Indicador de si el cliente dejó o no la empresa (Variable objetivo).
* `tenure`: Meses de contrato del cliente.
* `Contract`: Tipo de contrato (Mes a mes, Un año, Dos años).
* `PaymentMethod`: Forma de pago.
* `Charges.Monthly` / `Charges.Total`: Gastos mensuales y totales del cliente.

*(Nota: Durante la fase de transformación, se creó la variable adicional `Cuentas_Diarias` para un análisis más granular)*

## 🚀 Metodología
1. **Extracción:** Se cargó el JSON y se aplanó la estructura jerárquica en un DataFrame tabular.
2. **Transformación:** Se eliminaron registros vacíos en la variable objetivo, se corrigieron los tipos de datos en la facturación total y se imputaron valores nulos.
3. **Análisis (EDA):** Se evaluó la distribución del Churn (aprox. 26.5% de evasión) y se cruzó esta información con variables demográficas y de servicio para encontrar correlaciones.

## 💡 Resultados Clave (Insights)
* **Contratos:** Los usuarios con contratos de modalidad "Mes a mes" presentan un riesgo de cancelación críticamente mayor que aquellos con contratos anuales.
* **Antigüedad:** Existe una fuerte correlación negativa entre la retención y los meses de contrato (`tenure`); el riesgo de abandono es mucho más alto durante los primeros meses.
* **Métodos de Pago:** El pago mediante "Cheque electrónico" concentra la mayor proporción de evasión respecto a otros métodos automatizados.

## ⚙️ Instrucciones de Instalación y Uso
1. Clona este repositorio en tu máquina local:
   ```bash
   git clone https://github.com/JordanValenzuela22/Challenge-Telecom-X.git
