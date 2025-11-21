# Limpieza y Analisis de Datos: Cybersecurity Intrusion Detection Dataset

## Descripción del proyecto

El proyecto realiza un **Análisis Exploratorio de Datos (EDA) y un proceso de Limpieza de Datos** sobre el conjunto de datos **“Cybersecurity Intrusion Detection Dataset”**, disponible públicamente en [Kaggle](https://www.kaggle.com/datasets/dnkumars/cybersecurity-intrusion-detection-dataset).
El propósito es comprender la estructura de los datos e **identificar patrones, anomalías y relaciones entre variables del tráfico de red y comportamiento del usuario que sirvan como indicadores efectivos de actividad maliciosa o intrusión**.

El análisis se desarrolló en **Python** (utilizando librerías estándar como **Pandas**, **NumPy**, **Matplotlib** y **Seaborn**), dentro de un **Jupyter Notebook**, con un enfoque académico y de aprendizaje.

---
## Autores
  
- **Julian David Rodríguez Ramírez**
- **Sara Gabriela Chisaba Cárdenas**
- **Alejandra Cortes Murillo**
- **Juan Angel Triana Olarte**

---
## Roles

- **Alejandra:** Carga e inspección inicial de los datos, Manejo de datos faltantes, Tratamiento de valores inconsistentes en texto y duplicados
- **Juan:** Identificación de outliers, Filtrado y condiciones en Pandas
- **Gabriela:** Creación de variables, Agrupación con groupby
- **Julian:** Visualizaciones, Archivo Readme
---

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
### Explicación de la estructura y diccionario de la base de datos
## **Variables categóricas:**
1.	**Encryption_used:**
Indica el tipo de encriptación aplicado en la conexión. Sus categorías son:
-	AES: Estándar de cifrado avanzado, fuerte y ampliamente utilizado.
-	DES: Estándar antiguo de cifrado de datos.
-	Ninguna encriptación: No se usó ningún método de encriptación.
2.	**Protocol_type:**
Representa el protocolo utilizado en la comunicación:
-   TCP (Protocolo de Control de Transmisión).
-   UDP (Protocolo de Datagramas del Usuario).
-   ICMP (Protocolo de Mensajes de Control de Internet, usado en diagnósticos).
3. **Browser_type:** Tipo de navegador utilizado por el usuario.
4.	**Unusual_time_access:** Con registro binario que indica si inicio sesión fuera del horario normal.
5. **Attack_detected:** Variable con clasificación binaria que determina si recibió un ataque o no.
### **Variables númericas:**
-	**Asociadas al tráfico de red:**
 6.	**Network_packet_size:** Tamaño de paquetes de bytes que oscila entre 64 y 1500 bytes.
-	**Asociadas al comportamiento del usuario:**
 7.	**Login_attempts:** Intentos de inicio de sesión típicos de los usuarios
 8.	**Session_duration:** Tiempo de sesión iniciada.
 9.	**Failed_logins:** Número de inicios de sesión fallidos.
 10.	**Ip_reputation_score:** Mide y clasifica la confiabilidad de la dirección IP.
### **Otras**
11. **Session_id:** Número de ID de la sesión del usuario.
### **Nuevas variables**
12. **Minutos_sesion:** Cantidad de minutos de sesión iniciada relacionado con **Sesion_duration**.
13. **accesos_fallidos:** Mapeo especial creado a partir del **login_attempts**.
14. **paquetes_bytes:** Mapeo especial creado a partir del **network_packet_size**.

--
## Ejecución del Proyecto y activación del entorno

Para trabajar con este proyecto, es necesario configurar un entorno virtual de Python e instalar las dependencias requeridas.

### 1. Requisitos Previos

Asegúrate de tener instalado lo siguiente en tu sistema (instalar requirements.txt):

* **Python 3.8+**
* **pip** (Administrador de paquetes de Python)
* **Git** (Opcional, si clonas el repositorio)

---

### 2. Configuración del Entorno

Sigue estos pasos para crear y activar un entorno virtual. Esto aísla las dependencias del proyecto de tu instalación principal de Python.

#### A. Crear y Activar el Entorno

Abre tu terminal (Git Bash, PowerShell o CMD) y ejecuta:

| Sistema Operativo | Comando de Creación | Comando de Activación |
| :--- | :--- | :--- |
| **Windows** | `python -m venv venv` | `.\venv\Scripts\activate` |
| **macOS/Linux** | `python3 -m venv venv` | `source venv/bin/activate` |

*(El prefijo `(venv)` aparecerá en tu terminal, indicando que el entorno está activo.)*

#### B. Instalar Dependencias

Una vez activado el entorno, instala todas las librerías necesarias (Pandas, Matplotlib, Seaborn, Jupyter, etc.) utilizando el archivo `requirements.txt`.

```bash
pip install -r requirements.txt

¡Claro! Aquí tienes el código Markdown para las instrucciones de tu archivo README.md. Estas instrucciones guiarán a cualquier usuario sobre cómo configurar el entorno y ejecutar el notebook principal.

He incluido pasos para configurar un entorno virtual (recomendado) y ejecutar Jupyter.

Markdown

## 🚀 Ejecución y Análisis del Proyecto

Para trabajar con este proyecto, es necesario configurar un entorno virtual de Python e instalar las dependencias requeridas.

### 1. Requisitos Previos

Asegúrate de tener instalado lo siguiente en tu sistema:

* **Python 3.8+**
* **pip** (Administrador de paquetes de Python)
* **Git** (Opcional, si clonas el repositorio)

---

### 2. Configuración del Entorno

Sigue estos pasos para crear y activar un entorno virtual. Esto aísla las dependencias del proyecto de tu instalación principal de Python.

#### A. Crear y Activar el Entorno

Abre tu terminal (Git Bash, PowerShell o CMD) y ejecuta:

| Sistema Operativo | Comando de Creación | Comando de Activación |
| :--- | :--- | :--- |
| **Windows** | `python -m venv venv` | `.\venv\Scripts\activate` |
| **macOS/Linux** | `python3 -m venv venv` | `source venv/bin/activate` |

*(El prefijo `(venv)` aparecerá en tu terminal, indicando que el entorno está activo.)*

#### B. Instalar Dependencias

Una vez activado el entorno, instala todas las librerías necesarias (Pandas, Matplotlib, Seaborn, Jupyter, etc.) utilizando el archivo `requirements.txt` (asumo que tienes uno en la raíz del proyecto).

```bash
pip install -r requirements.txt

### 3. Ejecutar el Notebook Principal
El análisis completo y la limpieza de datos se encuentran en el archivo main.ipynb dentro de la carpeta src/.

####A. Iniciar Jupyter Notebook
Desde la carpeta raíz de tu proyecto, inicia el servidor de Jupyter:

```bash
jupyter notebook

####B. Abrir el Archivo
Tu navegador web se abrirá automáticamente en la interfaz de Jupyter. Navega a la carpeta src/ y haz clic en el archivo main.ipynb para comenzar el análisis.

###4. Finalizar el Entorno
Cuando termines de trabajar, puedes desactivar el entorno virtual ejecutando:

```bash
deactivate

---
### **Conclusiones**
1. **Ataques de Fuerza Bruta Son Rápidos y Automatizados**
- **Insight:** Los ataques que se enfocan en la autenticación (alto número de failed_logins) están optimizados para ser lo más breves posible.

- Hay una correlación inversa entre la cantidad de failed_logins y la duración total de la sesión (minutos_sesion): a medida que los fallos aumentan, el tiempo total de sesión disminuye (ej. la suma de duración cae drásticamente de 40k minutos en 1 fallo a 587 minutos en 5 fallos).

- **Recomendación:** La defensa más efectiva contra estos ataques (probablemente de fuerza bruta) es el rate-limiting y el bloqueo inmediato ante umbrales bajos de fallos, ya que la corta duración confirma que son procesos automatizados y de alta velocidad.

2. **Prioridad de Detección en Navegadores 'Unknown'**
- **Insight:** Las sesiones registradas con un navegador 'Unknown' (desconocido) son desproporcionadamente sospechosas. Aunque este grupo tiene un volumen de sesiones bajo, presenta una proporción de ataques muy alta en comparación con navegadores comunes como Chrome o Firefox.

- **Recomendación:** Se debe aplicar la política de seguridad más estricta (o el bloqueo preventivo) a cualquier sesión donde el browser_type sea 'Unknown', ya que esto indica el uso probable de scripts, bots o herramientas que no simulan un agente de usuario estándar.

3. **Intensidad del Ataque vs. Intentos de Login FallidosComparación:** 
attack_detected vs. failed_logins (a través de Box Plot o Estadísticas Descriptivas).

- **Insight Clave:** La presencia de un ataque se correlaciona con una mayor dispersión y un promedio más alto de intentos de login fallidos.

- **Detalle:** Las sesiones con ataques (attack_detected = 1) no solo tienen una mediana de fallos similar a las sesiones limpias, sino que muestran una mayor variabilidad y una fuerte presencia de outliers (hasta 13 intentos), mientras que las sesiones limpias rara vez superan los 7.
- **Conclusión:** El número de intentos fallidos es un predictor funcional del ataque si se relaciona con el tiempo de las sesiones y dependiendo el comportamiento de cada usuario (probablemente fuerza bruta o relleno de credenciales). El modelo de detección debe configurarse con un umbral estricto (ej. $> 7$ fallos) para activar la alerta de ataque.

4. **Encriptación Fuerte (AES) y la Frecuencia de AtaqueComparación:**  encryption_used vs. attack_detected.
- **Insight Clave:** Los ataques están significativamente presentes en conexiones que utilizan el estándar de encriptación AES (fuerte y moderno), lo que sugiere que los atacantes están apuntando a sesiones de alto valor o que han encontrado formas de evadir la detección a pesar de la encriptación.
- **Detalle:** Aunque DES es un estándar más antiguo y débil, AES (el más robusto) no disuade a los atacantes. Se encontró un volumen sustancial de ataques en sesiones encriptadas con AES, y la diferencia con DES podría no ser tan grande como se esperaría.
- **Conclusión:** La fortaleza de la encriptación no debe ser un factor de confianza para la seguridad. Las reglas de detección deben ser igualmente estrictas para el tráfico encriptado con AES, asumiendo que el ataque puede ocurrir una vez que la sesión está establecida.

5. **Reputación IP y Riesgo de Sesión** Comparación: ip_reputation_score vs. attack_detected (distribución de la puntuación).

- **Insight Clave:** Los ataques no se concentran solo en IPs de mala reputación (puntuaciones bajas), sino que también ocurren en un rango amplio de reputación IP.

- **Detalle:** Aunque las sesiones atacadas pueden mostrar una ligera tendencia hacia puntuaciones de reputación más bajas (IPs conocidas como riesgosas), existe una distribución considerable de ataques que provienen de IPs con reputación media o alta.

- **Conclusión:** La reputación de la IP es útil, pero no suficiente. Los atacantes sofisticados utilizan VPNs, proxies de pago o hosts de cloud limpios para lanzar ataques, eludiendo los bloqueos basados únicamente en la reputación IP. El modelo debe depender de indicadores de comportamiento (como failed_logins y session_duration) para detectar a estos atacantes "silenciosos".

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
