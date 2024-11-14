# Laboratorio LLM
## Carlos Alberto Sorza Gómez

### Explicación de Arquitectura

![Diagrama drawio](https://github.com/user-attachments/assets/70809e0d-7f0b-462e-9351-bc1d28db2d68)

1. Interfaz de Usuario (Frontend)
Descripción: Es la parte donde el usuario interactúa con la aplicación. Puede ser una interfaz web o una API.
Tecnologías: React, Vue, Angular (para frontend web), o cualquier cliente HTTP (si es solo una API REST).
2. API Backend
Descripción: El backend recibe las solicitudes de los usuarios, las procesa y coordina con el LLMChain para generar respuestas. Aquí también puede gestionarse la autenticación, validación de entradas, etc.
Tecnologías: FastAPI (como en el tutorial), Flask, Django, Node.js, etc.
3. LangChain (Motor de LLMs)
Descripción: El corazón de la arquitectura. LangChain se encarga de coordinar las cadenas de modelos, la creación de prompts y la integración con otros sistemas.

Componentes:

LLMChain: Aquí definimos las cadenas que utilizarán modelos de lenguaje para procesar los datos.
PromptTemplate: Plantillas de texto que estructuran cómo deben ser formuladas las solicitudes al modelo.
Tool: Herramientas adicionales que pueden ser utilizadas para enriquecer la respuesta del LLM (por ejemplo, recuperación de datos, búsqueda en bases de datos, etc.).
Agent: En el caso de que sea necesario un agente inteligente que decida entre diferentes acciones basadas en los resultados de los modelos o herramientas.
Tecnologías: LangChain, OpenAI GPT (o cualquier otro modelo LLM soportado), herramientas adicionales (e.g., APIs externas, bases de datos).

4. Modelos de Lenguaje (LLMs)
Descripción: LangChain puede usar cualquier modelo LLM compatible, como los de OpenAI, Hugging Face, o incluso modelos locales. Los modelos son utilizados para generar respuestas o procesar información.
Tecnologías: GPT-3/4 (OpenAI), modelos de Hugging Face, LLaMA, modelos entrenados por ti mismo, etc.
5. Almacenamiento (Opcional)
Descripción: Si necesitas guardar el historial de conversaciones, resultados de consultas, o cualquier dato relevante para el procesamiento posterior, un sistema de almacenamiento será necesario.
Tecnologías: Bases de datos relacionales (PostgreSQL, MySQL), bases de datos NoSQL (MongoDB, Firebase), almacenamiento de archivos (AWS S3, Azure Blob Storage).
6. Herramientas Externas y APIs (Opcional)
Descripción: En muchos casos, querrás integrar servicios externos para enriquecer las respuestas del modelo, realizar consultas o interacciones con otras plataformas.
Tecnologías: Servicios REST, APIs de terceros (e.g., APIs de búsqueda, servicios de traductores, bases de datos, etc.).

## Guía de Instalación

Para comenzar a trabajar con el proyecto, sigue estos pasos:

### 1. Clonar el repositorio en tu máquina local

Primero, necesitas clonar el repositorio en tu sistema usando Git. Esto descargará todos los archivos necesarios.

```bash
git clone <url_del_repositorio>
cd langchain-server
```
## Instalar las dependencias necesarias

Una vez dentro del directorio del proyecto, instala todos los paquetes requeridos desde el archivo requirements.txt. Esto instalará todas las bibliotecas necesarias para ejecutar el servidor.

pip install -r requirements.txt

## Configurar la clave de API de OpenAI
El siguiente paso es configurar tu clave de API de OpenAI para que el sistema pueda comunicarse con los modelos de lenguaje. Tienes dos formas de hacerlo:

Opción 1: Configura la clave en el archivo .env (si usas un archivo de entorno).
Opción 2: O puedes exportar la clave directamente en tu terminal.
Ejemplo de configuración para exportar la clave directamente:


export OPENAI_API_KEY='sk-tu-clave-de-api'

## Dependencias Requeridas
Este proyecto se apoya en varias bibliotecas clave:

FastAPI: Framework para construir y gestionar APIs de manera rápida y eficiente.
LangChain: Una biblioteca diseñada para trabajar con modelos de lenguaje, facilitando la creación de cadenas de procesamiento de texto.
Uvicorn: Un servidor ASGI ultrarrápido para ejecutar aplicaciones de FastAPI.
API de OpenAI: Necesaria para interactuar con los modelos de lenguaje de OpenAI, tales como GPT-3, para traducción y generación de texto.
![1](https://github.com/user-attachments/assets/f8ff2a41-85fd-417f-9f72-5d8b87d9ee88)

![image](https://github.com/user-attachments/assets/401c805c-4fc2-462d-98ab-ef2d5500077e)


