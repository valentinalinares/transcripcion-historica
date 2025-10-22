# 🧾 Transcripción Histórica con Python y OCR

Este repositorio contiene el proyecto **"Transcripción Histórica"**, presentado en el curso de Filosofía (Escuela de Filosofía, PUCP).  
Su objetivo es **mostrar cómo las herramientas computacionales —particularmente Python y OCR— pueden aplicarse a las humanidades** para digitalizar, analizar y re-editar textos antiguos.

---

## 🎯 Objetivo del proyecto

El proyecto parte de la digitalización de un texto histórico disponible en la **Biblioteca Digital PUCP**, cuyo formato original era un PDF compuesto únicamente por imágenes (sin texto reconocible).

A partir de ello, se implementó un flujo de trabajo que permite:

1. Extraer texto mediante **reconocimiento óptico de caracteres (OCR)** con [Tesseract](https://github.com/tesseract-ocr/tesseract).  
2. Limpiar, organizar y guardar la transcripción usando **Python**.  
3. Crear un modelo **replicable** para futuras reediciones y estudios de documentos históricos.

---

## 🧠 Tecnologías utilizadas

| Herramienta | Uso principal |
|--------------|---------------|
| **Python 3.11** | Lenguaje principal del proyecto |
| **Tesseract OCR** | Reconocimiento óptico de texto (imágenes → texto) |
| **Pillow** | Procesamiento de imágenes |
| **PyPDF2** | Extracción de páginas desde PDF |
| **Pandas** | Organización y almacenamiento estructurado de los datos |
| **Jupyter Notebook** | Documentación del proceso y experimentación de código |

---

## 🧩 Estructura del repositorio

transcripcion-historica/
│
├── 45 DER 1322.pdf # Documento histórico original (escaneado)
├── documento_limpio_partes/ # Carpeta con resultados parciales del OCR
├── documento_limpio_gemini.md # Transcripción limpia generada con IA (Gemini)
├── documento_limpio_gemini.docx # Versión Word del texto transcrito
├── transcripcion_simple.md # Resultado previo o versión base del OCR
├── transcripcion.ipynb # Notebook principal con el código de procesamiento OCR
├── requirements.txt # Librerías necesarias para ejecutar el notebook
└── README.md # Descripción del proyecto (este archivo)


---

## ⚙️ Flujo del Proceso

El proyecto sigue una secuencia reproducible que combina técnicas de **OCR**, **limpieza de texto** y **formateo automatizado**:

1. **Entrada:**  
   El proceso inicia con un documento PDF escaneado (`45 DER 1322.pdf`), compuesto únicamente por imágenes de texto antiguo.

2. **Conversión a Imágenes:**  
   El notebook divide el PDF en páginas individuales, guardadas temporalmente en `/documento_limpio_partes/`.

3. **Reconocimiento de Texto (OCR):**  
   Cada imagen se procesa con **Tesseract OCR** (configurado con el idioma español `spa`), extrayendo el texto en bruto.

4. **Limpieza y Estructuración:**  
   El texto se limpia mediante herramientas de Python y modelos de IA (como Gemini) para eliminar errores de reconocimiento y normalizar el formato.

5. **Exportación:**  
   El resultado se guarda en dos versiones:
   - `documento_limpio_gemini.md`: archivo Markdown editable.
   - `documento_limpio_gemini.docx`: versión en formato Word para revisión o reedición.

---

## 🧠 Objetivo Académico

Este proyecto busca demostrar el **potencial de Python en las humanidades**, especialmente para:

- **Preservar y difundir** documentos antiguos en formato digital accesible.  
- **Automatizar** procesos de transcripción que antes dependían de trabajo manual.  
- **Facilitar re-ediciones críticas** y comparaciones filológicas en filosofía, historia y literatura.

---

## 🔧 Requisitos

- Python 3.11+
- [Tesseract OCR](https://github.com/tesseract-ocr/tesseract)
- [Poppler](https://poppler.freedesktop.org/)
- Librerías Python:  
  ```bash
  pip install -r requirements.txt
