====================================================================

PROYECTO FINAL - VISIÓN POR COMPUTADOR I (Curso 2026/2027)

Sistema de Detección de Manzanas para Cosecha Robotizada

====================================================================



PARTICIPANTES:

- Alejandro López

- Paulino Sanchiz



--------------------------------------------------------------------

1. DESCRIPCIÓN DEL PROYECTO

--------------------------------------------------------------------

El presente proyecto tiene como objetivo diseñar e implementar un sistema 

de visión por computador clásico capaz de identificar manzanas maduras en 

árboles frutales. Este desarrollo está orientado a optimizar la recolección 

automatizada mediante robots agrícolas, abordando la escasez de mano de 

obra en el sector.



El sistema procesa imágenes reales de entornos agrícolas y compara los 

resultados con imágenes segmentadas de referencia (Ground Truth) para 

evaluar la precisión del algoritmo.



IMPORTANTE: En estricto cumplimiento con los requisitos de la asignatura, 

este proyecto utiliza exclusivamente técnicas tradicionales de visión por 

computador (procesamiento clásico), sin recurrir a modelos de Deep Learning 

o arquitecturas no vistas en clase.



--------------------------------------------------------------------

2. TÉCNICAS UTILIZADAS

--------------------------------------------------------------------

El flujo de procesamiento se compone de las siguientes fases:

- Preprocesamiento: Filtrado espacial y conversión de espacios de color 

  (ej. HSV, LAB) para mitigar los cambios de iluminación y sombras del follaje.

- Segmentación: Umbralización (global y adaptativa) para aislar el 

  color de los frutos frente al fondo (hojas y ramas).

- Operaciones Morfológicas: Aperturas y cierres matemáticos para eliminar 

  el ruido del entorno y rellenar huecos en la segmentación de las manzanas.

- Análisis de Componentes Conexas (CCL): Extracción de contornos y 

  filtrado geométrico (por área o circularidad) para descartar falsos positivos.

- Evaluación (Métricas): Cálculo automatizado de IoU, Coeficiente de Dice 

  (F1-Score), Exactitud, Precisión y Recall frente al Ground Truth.



--------------------------------------------------------------------

3. REQUISITOS DEL SISTEMA

--------------------------------------------------------------------

Para ejecutar el código es necesario contar con Python 3.x y las siguientes 

dependencias instaladas:



pip install opencv-python numpy scipy matplotlib scikit-learn



--------------------------------------------------------------------

4. ESTRUCTURA DEL REPOSITORIO

--------------------------------------------------------------------

- /src/          : Contiene los scripts principales en Python.

- /data/         : Carpeta destinada a las imágenes reales y sus Ground Truth.

- /docs/         : Memoria descriptiva del desarrollo del proyecto.

- README.txt     : Este archivo de configuración e información.



--------------------------------------------------------------------

5. DECLARACIÓN DE USO DE IA (Para incluir en la Memoria)

--------------------------------------------------------------------

Según la normativa del proyecto, la memoria descriptiva incluye el 

siguiente bloque de declaración:



- Herramientas utilizadas: [Indicar herramienta, ej. ChatGPT, Gemini...]

- Finalidad del uso: [Ej. Asistencia en la generación de rutinas de métricas...]

- Indicaciones o instrucciones proporcionadas: [Resumen de prompts...]

- Uso del contenido generado: [Ej. Adaptación de fórmulas geométricas...]

- Revisión y edición: [Ej. El código fue revisado, modificado y validado...]

- Limitaciones y consideraciones éticas: [Ej. Se ha asegurado el uso exclusivo de técnicas tradicionales...]