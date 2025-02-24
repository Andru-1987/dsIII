# CLASE 2

## NLP I

# 📌 **¿Qué es el NLP (Procesamiento de Lenguaje Natural)?**  
El **Procesamiento de Lenguaje Natural (NLP - Natural Language Processing)** es una rama de la inteligencia artificial que permite a las computadoras entender, interpretar y generar lenguaje humano de manera automática.  

El NLP combina lingüística y aprendizaje automático para trabajar con **texto** y **voz**, ayudando a las máquinas a interactuar con los humanos de manera más eficiente.  

---

## 🔹 **Características clave del NLP**  

### 1️⃣ **Tokenización**  
- Divide un texto en palabras o frases más pequeñas llamadas **tokens**.  
- Ejemplo:  
  ```
  Texto: "El gato duerme"
  Tokens: ["El", "gato", "duerme"]
  ```

### 2️⃣ **Lematización y stemming**  
- **Stemming:** Reduce una palabra a su raíz base eliminando sufijos.  
  - Ejemplo: "corriendo" → "corr"  
- **Lematización:** Convierte una palabra a su forma base considerando su significado.  
  - Ejemplo: "corriendo" → "correr"  

### 3️⃣ **Análisis morfosintáctico (POS Tagging)**  
- Identifica el tipo de cada palabra (**sustantivo, verbo, adjetivo, etc.**).  
- Ejemplo:  
  ```
  "El gato duerme"
  "El" (determinante), "gato" (sustantivo), "duerme" (verbo)
  ```

### 4️⃣ **Reconocimiento de entidades (NER - Named Entity Recognition)**  
- Identifica nombres de personas, lugares, fechas, organizaciones, etc.  
- Ejemplo:  
  ```
  "Apple lanzó el iPhone 15 en septiembre de 2023"
  - Apple → Empresa
  - iPhone 15 → Producto
  - septiembre de 2023 → Fecha
  ```

### 5️⃣ **Análisis de sentimiento**  
- Determina si un texto tiene un tono **positivo, negativo o neutral**.  
- Se usa en redes sociales, servicio al cliente, análisis de opiniones, etc.  

### 6️⃣ **Bag of Words y TF-IDF**  
- Métodos para representar texto en formato numérico.  
- **Bag of Words (BoW):** Cuenta la frecuencia de palabras en un documento.  
- **TF-IDF:** Asigna pesos a palabras según su importancia en un conjunto de documentos.  

### 7️⃣ **N-grams**  
- Secuencias de **N palabras consecutivas** usadas para modelar el lenguaje.  
- Ejemplo:  
  ```
  "El gato duerme en la casa"
  - Bigramas: ["El gato", "gato duerme", "duerme en"]
  ```

### 8️⃣ **Modelos avanzados de NLP**  
- **Word Embeddings (Word2Vec, GloVe, FastText):** Representan palabras en vectores numéricos capturando su significado.  
- **Transformers (BERT, GPT, T5):** Modelos más sofisticados que entienden contexto y generan texto de manera fluida.  

---

## 📌 **Resumen del NLP**  

| Característica | Descripción |
|--------------|------------|
| **Tokenización** | Divide texto en palabras o frases. |
| **Lematización y Stemming** | Normaliza palabras a su forma base. |
| **Análisis gramatical (POS Tagging)** | Identifica sustantivos, verbos, adjetivos, etc. |
| **Reconocimiento de entidades (NER)** | Detecta nombres de personas, lugares, fechas, etc. |
| **Análisis de sentimiento** | Determina si un texto es positivo, negativo o neutral. |
| **Bag of Words y TF-IDF** | Representan texto en formato numérico. |
| **N-grams** | Modela texto usando secuencias de palabras consecutivas. |
| **Word Embeddings y Transformers** | Métodos avanzados para capturar significado del lenguaje. |

---


## CHAT GPT

El algoritmo detrás de ChatGPT es un **modelo de lenguaje basado en redes neuronales profundas**, específicamente una variante de **GPT (Generative Pre-trained Transformer)** desarrollado por OpenAI.  

[DNN](https://botpress.com/es/blog/deep-neural-network)

### 🔹 **Principales características del algoritmo de ChatGPT**  

1. **Basado en la arquitectura Transformer**  
   - Utiliza el mecanismo de **atención** (Self-Attention) para analizar el contexto de las palabras en una conversación y generar respuestas coherentes.  

2. **Entrenamiento en dos fases:**  
   - **Pre-entrenamiento:** Se entrena con grandes volúmenes de texto de internet para aprender patrones del lenguaje.  
   - **Ajuste fino (Fine-Tuning):** Se refina con datos específicos y, en algunos casos, con aprendizaje por refuerzo con retroalimentación humana (**RLHF - Reinforcement Learning from Human Feedback**).  

3. **Generación de texto autoregresiva**  
   - Predice la siguiente palabra en función del contexto previo.  

4. **Uso de embeddings de palabras**  
   - Representa palabras y frases en un espacio matemático para entender relaciones semánticas.  

5. **Tamaño del modelo**  
   - Existen versiones con diferentes cantidades de parámetros (GPT-3, GPT-3.5, GPT-4, etc.), donde los modelos más grandes tienen más capacidad de comprensión y generación de texto.  

6. **Optimización con RLHF**  
   - Se mejora la calidad de las respuestas a través de un proceso donde entrenadores humanos califican y ajustan las respuestas del modelo.  

### 🔹 **Diferencia con otros modelos**  
- **Vs RNN/LSTM:** ChatGPT usa Transformers, que manejan dependencias a largo plazo mejor que RNNs o LSTMs.  
- **Vs Modelos Basados en Reglas:** No sigue reglas preprogramadas, sino que aprende patrones del lenguaje.  

---

### REGEXP

# 📌 **Mini Tutorial de Expresiones Regulares (RegEx) para NLP**  

Las **expresiones regulares (RegEx)** son herramientas poderosas para procesar y manipular texto en **NLP (Procesamiento de Lenguaje Natural)**. Se usan para extraer información, limpiar datos y estructurar texto de manera eficiente.  

---

## 📌 **1️⃣ Conceptos Básicos de RegEx**  

| **Patrón** | **Significado** | **Ejemplo Coincidente** |
|-----------|----------------|-------------------------|
| `.`       | Cualquier carácter (excepto nueva línea) | `"casa"`, `"mesa"` → `".asa"` |
| `\d`      | Un dígito (0-9) | `"123"` → `"\d\d\d"` |
| `\w`      | Cualquier carácter alfanumérico (`a-z, A-Z, 0-9, _`) | `"Python_3"` → `"\w+"` |
| `\s`      | Espacio en blanco (espacio, tabulación, salto de línea) | `"Hola mundo"` → `"Hola\s"` |
| `\b`      | Límite de palabra | `"el gato"` → `"\bel\b"` (solo coincide "el") |
| `+`       | Uno o más repeticiones | `"aaa"`, `"abc"` → `"a+"` |
| `*`       | Cero o más repeticiones | `""`, `"aaa"` → `"a*"` |
| `?`       | Cero o una repetición | `"color"`, `"colour"` → `"colou?r"` |
| `{n,m}`   | Entre `n` y `m` repeticiones | `"12345"` → `"\d{2,4}"` (coincide con "1234") |
| `[]`      | Grupo de caracteres | `"casa"`, `"cosa"` → `"[cC]asa"` |
| `\|`       | Operador "o" | `"gato"`, `"perro"` → `"gato\|perro"` |
| `()`      | Grupo de captura | `"abc123"` → `"(abc)\d+"` (captura "abc") |

---

## 📌 **2️⃣ Aplicaciones en NLP**  

### 📝 **1. Eliminación de Puntuación**  
```python
import re

texto = "¡Hola! ¿Cómo estás? Me llamo Andru."
texto_limpio = re.sub(r"[^\w\s]", "", texto)  # Remueve puntuación
print(texto_limpio)
```
🔹 **Salida:**  
```
Hola Cómo estás Me llamo Andru
```

---

### 🔢 **2. Extraer Números de un Texto**  
```python
texto = "Tengo 3 gatos y 2 perros."
numeros = re.findall(r"\d+", texto)
print(numeros)
```
🔹 **Salida:**  
```
['3', '2']
```

---

### 📧 **3. Validar Correos Electrónicos**  
```python
def es_email_valido(email):
    patron = r"^[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+$"
    return bool(re.match(patron, email))

print(es_email_valido("correo@dominio.com"))  # True
print(es_email_valido("correo@dominio"))      # False
```

---

### 📅 **4. Extraer Fechas**  
```python
texto = "Las reuniones son el 15/08/2023 y el 20-09-2024."
fechas = re.findall(r"\b\d{2}[/\-]\d{2}[/\-]\d{4}\b", texto)
print(fechas)
```
🔹 **Salida:**  
```
['15/08/2023', '20-09-2024']
```

---

### 🏷 **5. Tokenización de Texto con RegEx**  
```python
texto = "El NLP es increíble, ¿no crees?"
tokens = re.findall(r"\b\w+\b", texto)
print(tokens)
```
🔹 **Salida:**  
```
['El', 'NLP', 'es', 'increíble', 'no', 'crees']
```

---

[Curso de expresiones regulares](https://www.youtube.com/watch?v=de_7k4SHEO0&t=2s)


---
Usos más comunes de la técnica **Bag of Words (BoW)** en procesamiento de lenguaje natural (NLP):

| Uso Común                      | Descripción                                                                                     |
|--------------------------------|-------------------------------------------------------------------------------------------------|
| **Clasificación de Texto**     | Se utiliza para categorizar documentos o reseñas en diferentes clases (ej. positivo/negativo).|
| **Análisis de Sentimientos**   | Permite identificar el sentimiento detrás de un texto, clasificándolo en categorías emocionales.|
| **Extracción de Características** | Se usa para convertir texto en vectores numéricos, facilitando su uso en algoritmos de machine learning.|
| **Modelado de Temas**         | Ayuda a descubrir temas predominantes en un conjunto de documentos al analizar las palabras más frecuentes. |
| **Recomendaciones de Contenido** | Puede mejorar sistemas de recomendación al analizar la similitud entre textos (ej. artículos, libros).|
| **Búsqueda de Información**   | Facilita la indexación y recuperación de documentos relevantes en bases de datos o motores de búsqueda. |
| **Análisis de Tendencias**    | Permite identificar tendencias en el uso de palabras o frases a lo largo del tiempo en redes sociales o artículos.|
| **Generación de Resúmenes**   | Ayuda a identificar las palabras clave y frases más relevantes para crear resúmenes automáticos de textos largos. |
| **Detección de Plagio**       | Se usa para comparar la similitud entre documentos y detectar contenido plagiado.              |
| **Filtrado de Spam**          | Ayuda a clasificar correos electrónicos o mensajes como spam o no spam analizando las palabras clave. |


---

Claro, aquí tienes un ejemplo sencillo para ilustrar cómo se calcula TF-IDF:

### Supongamos que tenemos un corpus de 3 documentos:

- **Documento 1 (D1)**: "El perro juega en el parque."
- **Documento 2 (D2)**: "El gato juega en la casa."
- **Documento 3 (D3)**: "El perro y el gato están en casa."

### Paso 1: Calcular TF

Primero, contamos la frecuencia de cada término en cada documento:

- **D1**:
  - "El": 1
  - "perro": 1
  - "juega": 1
  - "en": 1
  - "parque": 1
  - **Total**: 5

  \[
  TF(\text{"perro"}, D1) = \frac{1}{5} = 0.2
  \]
  \[
  TF(\text{"juega"}, D1) = \frac{1}{5} = 0.2
  \]

- **D2**:
  - "El": 1
  - "gato": 1
  - "juega": 1
  - "en": 1
  - "la": 1
  - "casa": 1
  - **Total**: 6

  \[
  TF(\text{"gato"}, D2) = \frac{1}{6} \approx 0.167
  \]
  \[
  TF(\text{"juega"}, D2) = \frac{1}{6} \approx 0.167
  \]

- **D3**:
  - "El": 1
  - "perro": 1
  - "y": 1
  - "gato": 1
  - "están": 1
  - "en": 1
  - "casa": 1
  - **Total**: 7

  \[
  TF(\text{"perro"}, D3) = \frac{1}{7} \approx 0.143
  \]
  \[
  TF(\text{"gato"}, D3) = \frac{1}{7} \approx 0.143
  \]

### Paso 2: Calcular IDF

Ahora calculamos IDF para cada término:

- **Número total de documentos (N)**: 3

- **Documentos que contienen cada término**:
  - "perro": 2 (D1, D3)
  - "gato": 2 (D2, D3)
  - "juega": 2 (D1, D2)
  - "en": 3 (D1, D2, D3)
  - "parque": 1 (D1)
  - "casa": 2 (D2, D3)

Usamos la fórmula para IDF:

\[
IDF(t) = \log\left(\frac{N}{|\{d \in D : t \in d\}|}\right)
\]

- **IDF("perro")**:
  \[
  IDF(\text{"perro"}) = \log\left(\frac{3}{2}\right) \approx 0.176
  \]

- **IDF("gato")**:
  \[
  IDF(\text{"gato"}) = \log\left(\frac{3}{2}\right) \approx 0.176
  \]

- **IDF("juega")**:
  \[
  IDF(\text{"juega"}) = \log\left(\frac{3}{2}\right) \approx 0.176
  \]

- **IDF("en")**:
  \[
  IDF(\text{"en"}) = \log\left(\frac{3}{3}\right) = 0
  \]

- **IDF("parque")**:
  \[
  IDF(\text{"parque"}) = \log\left(\frac{3}{1}\right) \approx 1.098
  \]

- **IDF("casa")**:
  \[
  IDF(\text{"casa"}) = \log\left(\frac{3}{2}\right) \approx 0.176
  \]

### Paso 3: Calcular TF-IDF

Finalmente, multiplicamos TF y IDF para cada término en cada documento:

- **Para D1**:
  - **TF-IDF("perro", D1)**:
    \[
    TFIDF(\text{"perro"}, D1) = 0.2 \times 0.176 \approx 0.0352
    \]
  - **TF-IDF("juega", D1)**:
    \[
    TFIDF(\text{"juega"}, D1) = 0.2 \times 0.176 \approx 0.0352
    \]
  - **TF-IDF("parque", D1)**:
    \[
    TFIDF(\text{"parque"}, D1) = 0.2 \times 1.098 \approx 0.2196
    \]

- **Para D2**:
  - **TF-IDF("gato", D2)**:
    \[
    TFIDF(\text{"gato"}, D2) \approx 0.167 \times 0.176 \approx 0.0294
    \]
  - **TF-IDF("juega", D2)**:
    \[
    TFIDF(\text{"juega"}, D2) \approx 0.167 \times 0.176 \approx 0.0294
    \]

- **Para D3**:
  - **TF-IDF("perro", D3)**:
    \[
    TFIDF(\text{"perro"}, D3) \approx 0.143 \times 0.176 \approx 0.0252
    \]
  - **TF-IDF("gato", D3)**:
    \[
    TFIDF(\text{"gato"}, D3) \approx 0.143 \times 0.176 \approx 0.0252
    \]

Este es un ejemplo básico de cómo se calcula TF-IDF para un pequeño corpus. En la práctica, trabajarías con textos mucho más grandes y usarías herramientas y bibliotecas que faciliten estos cálculos.

