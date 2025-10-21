# GENAI Application Engineering – Laboratorios

Este repositorio contiene los laboratorios prácticos del curso "GENAI Application Engineering" de ORT Uruguay.

Sitio del curso: https://fi.ort.edu.uy/genai-application-engineering

## Descripción
El repositorio ofrece notebooks (LETRA) para que completes en clase/tarea y notebooks de referencia (SOLUCION) con implementaciones guía. Cada laboratorio introduce conceptos y prácticas para construir aplicaciones con LLMs, RAG y agentes, siguiendo el ecosistema moderno de LangChain, LangGraph, Pinecone y proveedores de modelos.

## Laboratorios incluidos
- **Lab 1 – LangChain + LLM Prompting**
  - Enunciado: `Lab1_langchain_LLM_prompt_LETRA.ipynb`
  - Solución: `Soluciones/Lab01_langchain_llm_prompt_SOLUCION.ipynb`
- **Lab 2 – Bases de Datos Vectoriales**
  - Enunciado: `Lab2_BBDD_Vectoriales_LETRA.ipynb`
  - Solución: `Soluciones/Lab02_BBDD_Vectoriales_SOLUCION.ipynb`
- **Lab 3 – RAG Pipeline**
  - Enunciado: `Lab3_RAG_Pipeline_LETRA.ipynb`
  - Solución: `Soluciones/Lab03_RAG_Pipeline_SOLUCION.ipynb`
- **Lab 4 – Agents & Tools**
  - Enunciado: `Lab4_Agent_Tools_LETRA.ipynb`

## Requisitos
- Python 3.12 (recomendado para compatibilidad con dependencias actuales)
- Cuenta y API Key del proveedor que utilices:
  - **OpenAI**: variable `OPENAI_TOKEN`
  - **Hugging Face**: variable `HF_TOKEN`
- Git y un entorno de notebooks (VS Code + Python, Jupyter, o Colab)

## Configuración rápida (Windows / PowerShell)
1) Crear entorno virtual con Python 3.12 en la carpeta del proyecto:
```powershell
py -3.12 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -U pip
```

2) Instalar dependencias típicas usadas en los labs (ajusta según necesidad del notebook):
```powershell
pip install langchain langchain-openai langgraph langchain-community \
            langchain-pinecone pinecone-client langchain-huggingface \
            sentence-transformers pydantic pypdf wikipedia
```

3) Configurar variables de entorno (sesión actual):
```powershell
$env:OPENAI_TOKEN = "<TU_OPENAI_API_KEY>"
$env:HF_TOKEN     = "<TU_HF_USER_ACCESS_TOKEN>"
```

4) Abrir y ejecutar el notebook de tu laboratorio en orden de celdas.

## Ejecución de notebooks
- Selecciona el kernel del proyecto: `./.venv/Scripts/python.exe`.
- Ejecuta las celdas en orden. Si instalas paquetes desde una celda, reinicia el kernel si es necesario.
- En `Lab4_Agent_Tools_LETRA.ipynb`:
  - Parte 1–3 usan `OPENAI_TOKEN`.
  - Partes posteriores pueden requerir `wikipedia`, `pinecone-client`, `langchain-pinecone`, etc.

## Buenas prácticas de seguridad
- Nunca subas secretos (API keys) al repositorio. Usa variables de entorno o secretos de CI.
- `.gitignore` ya ignora `.venv` y `*.env`.
- Si un secreto se comitea por error, revócalo y reescribe el historial antes de volver a hacer push.

## Estructura del repositorio
- `Lab1_langchain_LLM_prompt_LETRA.ipynb`
- `Lab2_BBDD_Vectoriales_LETRA.ipynb`
- `Lab3_RAG_Pipeline_LETRA.ipynb`
- `Lab4_Agent_Tools_LETRA.ipynb`
- `Soluciones/`
  - `Lab01_langchain_llm_prompt_SOLUCION.ipynb`
  - `Lab02_BBDD_Vectoriales_SOLUCION.ipynb`
  - `Lab03_RAG_Pipeline_SOLUCION.ipynb`

## Recursos
- LangChain: https://python.langchain.com/
- LangGraph: https://langchain-ai.github.io/langgraph/
- Pinecone: https://docs.pinecone.io/
- Hugging Face Hub: https://huggingface.co/

## Licencia
Indica aquí la licencia del material si corresponde (por ejemplo, MIT, CC BY-NC, etc.).
