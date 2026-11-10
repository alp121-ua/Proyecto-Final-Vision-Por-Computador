# Proyecto Final - Visión por Computador I (Curso 2026/2027)



**Sistema de Detección de Manzanas para Cosecha Robotizada**



---



## Participantes

* **Alejandro López**

* **Paulino Sanchiz**



---



## 1. Descripción del Proyecto

El presente proyecto tiene como objetivo diseñar e implementar un sistema de **visión por computador clásico** capaz de identificar manzanas maduras en árboles frutales. Este desarrollo está orientado a optimizar la recolección automatizada mediante robots agrícolas, abordando la escasez de mano de obra en el sector.



El sistema procesa imágenes reales de entornos agrícolas y compara los resultados con imágenes segmentadas de referencia (*Ground Truth*) para evaluar la precisión del algoritmo.



> ** IMPORTANTE:** En estricto cumplimiento con los requisitos de la asignatura, este proyecto utiliza **exclusivamente técnicas tradicionales** de visión por computador (procesamiento clásico), sin recurrir a modelos de *Deep Learning* o arquitecturas no vistas en clase.



---



## 2. 🛠️ Técnicas Utilizadas

El flujo de procesamiento se compone de las siguientes fases:



* **Preprocesamiento:** Filtrado espacial y conversión de espacios de color (ej. HSV, LAB) para mitigar los cambios de iluminación y sombras del follaje.

* **Segmentación:** Umbralización (global y adaptativa) para aislar el color de los frutos frente al fondo (hojas y ramas).

* **Operaciones Morfológicas:** Aperturas y cierres matemáticos para eliminar el ruido del entorno y rellenar huecos en la segmentación de las manzanas.

* **Análisis de Componentes Conexas (CCL):** Extracción de contornos y filtrado geométrico (por área o circularidad) para descartar falsos positivos.

* **Evaluación (Métricas):** Cálculo automatizado de IoU, Coeficiente de Dice (F1-Score), Exactitud, Precisión y Recall frente al *Ground Truth*.



---



## 3. Requisitos del Sistema

Para ejecutar el código es necesario contar con **Python 3.x** y las siguientes dependencias instaladas. Puedes instalarlas fácilmente mediante pip:



`pip install opencv-python numpy scipy matplotlib scikit-learn`



---



## 4. Estructura del Repositorio

* `/src/` : Contiene los scripts principales en Python.

* `/data/` : Carpeta destinada a las imágenes reales y sus *Ground Truth*.

* `/docs/` : Memoria descriptiva del desarrollo del proyecto.

* `README.md` : Este archivo de documentación e información.



---



## 5. Declaración de Uso de IA (Para la Memoria)

Según la normativa del proyecto, la memoria descriptiva incluirá el siguiente bloque de declaración:



* **Herramientas utilizadas:** *[Indicar herramienta, ej. Gemini, ChatGPT...]*

* **Finalidad del uso:** *[Ej. Asistencia en la generación de rutinas de métricas o formato de documentación...]*

* **Indicaciones o instrucciones proporcionadas:** *[Resumen de los prompts principales...]*

* **Uso del contenido generado:** *[Ej. Adaptación de fórmulas matemáticas al código Python...]*

* **Revisión y edición:** *[Ej. El código y texto fueron revisados, probados y ajustados a los requisitos de la práctica...]*

* **Limitaciones y consideraciones éticas:** *[Ej. Se ha garantizado el uso exclusivo de técnicas tradicionales de visión por computador...]*
