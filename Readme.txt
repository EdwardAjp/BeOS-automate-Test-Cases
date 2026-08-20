#  BeOS QA Auto-Generator

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python&logoColor=white)
![Gemini AI](https://img.shields.io/badge/Gemini_AI-2.5_Flash-orange?style=for-the-badge&logo=google&logoColor=white)
![ClickUp](https://img.shields.io/badge/ClickUp-API_v2-purple?style=for-the-badge&logo=clickup&logoColor=white)
![QASE](https://img.shields.io/badge/QASE-Ready-green?style=for-the-badge)

Una poderosa herramienta de automatización de QA (Shift-Left Testing) diseñada para agilizar la creación de casos de prueba. Este script actúa como un puente entre la gestión de proyectos y la ejecución de calidad, utilizando Inteligencia Artificial para analizar requerimientos y generar pruebas profundas y estructuradas.

##  Características Principales

- ** Extracción Inteligente (ClickUp):** Escanea automáticamente las listas de tareas buscando tickets aprobados (filtrados por prefijos específicos y longitud de criterios).
- **Generación con IA (Gemini):** Lee un archivo de reglas estricto (`prompt-test-cases.md`) y utiliza Google Gemini para redactar casos de prueba enfocados en flujos negativos, roles y *Edge Cases*.
- ** Anti-Pereza (Volume Forcing):** Algoritmo que obliga a la IA a generar un mínimo de 8 casos complejos para tareas de alto impacto.
- ** Exportación Dual (Word y Excel):** Crea una carpeta por cada tarea y genera automáticamente:
  - Un archivo `.xlsx` con el formato horizontal perfecto y listo para importación masiva a QASE.
  - Un archivo `.docx` limpio y maquetado para la lectura y revisión humana.
- ** Auditoría de Requerimientos:** Genera un reporte final detallando qué tareas de ClickUp fueron rechazadas por falta de criterios de aceptación.

##  Tecnologías Utilizadas

- **Python** (`pandas`, `python-docx`, `requests`)
- **Google Generative AI SDK** (Modelos Flash para procesamiento masivo)
- **Dotenv** para la seguridad y ocultación de API Keys

##  Flujo de Trabajo

1. El script lee el `.env` de forma segura.
2. Extrae las tareas de la lista indicada en ClickUp.
3. Filtra la "basura" y se queda solo con las historias de usuario válidas.
4. Gemini procesa la descripción cruzándola con las directrices de QA (recomendable crear un archivo .md con las directrices para la creación del documento de Word).
5. Se generan las carpetas en `Entregables_QA/` con los archivos listos para usar.

---
*Desarrollado para elevar los estándares de Calidad de Software y reducir el tiempo de diseño de pruebas en un 80%.*