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


 