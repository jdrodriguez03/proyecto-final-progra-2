# Limpieza y Analisis de Datos: Cybersecurity Intrusion Detection Dataset

## Descripción del proyecto

El proyecto realiza un **Análisis Exploratorio de Datos (EDA) y un proceso de Limpieza de Datos** sobre el conjunto de datos **“Cybersecurity Intrusion Detection Dataset”**, disponible públicamente en [Kaggle](https://www.kaggle.com/datasets/dnkumars/cybersecurity-intrusion-detection-dataset).
El propósito es comprender la estructura de los datos e **identificar patrones, anomalías y relaciones entre variables del tráfico de red y comportamiento del usuario que sirvan como indicadores efectivos de actividad maliciosa o intrusión**.

El análisis se desarrolló en **Python** (utilizando librerías estándar como **Pandas**, **NumPy**, **Matplotlib** y **Seaborn**), dentro de un **Jupyter Notebook**, con un enfoque académico y de aprendizaje.

---
## Objetivos

### Objetivo General

Realizar un proceso integral de **Limpieza**, **Validación** y **Análisis Exploratorio de Datos (EDA)** del conjunto de datos. 
El propósito es **sanear y comprender la estructura, distribución y comportamiento de las variables**, con el fin de **identificar y evaluar patrones relevantes** en el tráfico de red y en la actividad de los usuarios. 

Estos patrones deben aportar **correlación significativa** y **capacidad discriminatoria**, contribuyendo a una **detección más efectiva de ataques cibernéticos**.


### Objetivos Específicos

**Garantía de la Calidad e Integridad de los Datos:**

* **Gestión de Datos Faltantes:** Realizar un análisis exhaustivo de la completitud del *dataset* para identificar y cuantificar los valores nulos, determinando la estrategia de imputación metodológicamente más sólida para las variables categóricas afectadas.
* **Consistencia Estructural:** Evaluar la unicidad de los registros mediante la identificación de filas duplicadas y proceder a su eliminación sistemática, asegurando la integridad y la ausencia de redundancias que puedan sesgar el análisis estadístico posterior.

**Optimización Estadística mediante Tratamiento de Valores Atípicos (*Outliers*):**

* **Identificación Cuantitativa:** Aplicar métricas estadísticas robustas (e.g., el Rango Intercuartílico) para la detección formal de valores atípicos dentro de las distribuciones de las variables cuantitativas de tráfico y sesión.
* **Mitigación Condicional:** Evaluar y ejecutar la normalización o remoción justificada de los *outliers* identificados, asegurando que esta intervención no comprometa los patrones intrínsecos de la clase objetivo (detección de ataque), con el fin de optimizar la robustez de los estadísticos descriptivos.

**Caracterización y Análisis Descriptivo Profundo:**

* **Medidas Descriptivas Clave:** Calcular, documentar y presentar las métricas de tendencia central y dispersión (media, desviación estándar, cuartiles, etc.) para todas las variables cuantitativas del *dataset*.
* **Análisis de Distribución y Frecuencias:** Generar visualizaciones y tablas de frecuencia que permitan establecer la forma de la distribución de las variables numéricas y la proporción de ocurrencia de las diferentes categorías en las variables cualitativas (e.g., tipo de protocolo, tipo de navegador), proporcionando un perfil demográfico del tráfico.

**Diferenciación de Patrones de Tráfico y Potenciales Indicadores:**

* **Visualización Bivariada Comparativa:** Diseñar y generar visualizaciones analíticas comparativas (Boxplots, Gráficos de Densidad) para contrastar las distribuciones de las variables predictivas clave (relacionadas con el volumen de datos, la duración y la frecuencia de acciones) en función del estado binario de la variable objetivo (tráfico normal vs. tráfico malicioso).
* **Exploración de la Discriminalidad:** Utilizar el contraste visual para explorar la existencia de patrones distintivos o umbrales operativos que puedan ser postulado como indicadores potenciales y tempranos de actividad anómala o intrusión dentro de la infraestructura de red.
---
## Autores
  
- **Julian David Rodríguez Ramírez**
-
-
-

---

## Estructura del repositorio
```text
├── data/            # Dataset original
├── src/             # Notebook principal en Python usado para el análisis
├── LICENSE          # Licencia (MIT License)
├── README.md        # Este archivo
└── requirements.txt # Dependencias del proyecto


```
---

## Dataset

**Nombre:** Cybersecurity Intrusion Detection Dataset  
**Autor original:** [Dinesh Naveen Kumar Samudrala](https://www.kaggle.com/dnkumars)  
**Fuente:** [Kaggle Dataset](https://www.kaggle.com/datasets/dnkumars/cybersecurity-intrusion-detection-dataset)  
**Licencia:** MIT License

>  El dataset fue creado por Dinesh Naveen Kumar Samudrala y se usa aquí **solo con fines académicos** bajo los términos de la licencia MIT License.  
> Los análisis y visualizaciones producidos en este repositorio son obra original de los autores mencionados.

---
