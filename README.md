# Alerta temprana de clientes insatisfechos con automatización e IA
## Impacto empresarial de la automatización del feedback de clientes
En un entorno donde la experiencia del cliente es un factor diferencial clave, **disponer de sistemas que permitan actuar rápidamente ante opiniones negativas es fundamental** para mejorar la retención y la reputación de marca.

**Este proyecto consiste en una automatización inteligente del ciclo de feedback de clientes**, basada en herramientas no-code y servicios de inteligencia artificial. A partir de un formulario de opinión, se capturan respuestas en tiempo real, se detectan automáticamente las puntuaciones bajas y se activa un correo inmediato al equipo de atención al cliente. A su vez, los comentarios son analizados mediante GPT para clasificar su tono emocional (positivo, neutral o negativo) y, según esa clasificación, se activan acciones personalizadas como emails de agradecimiento, alertas o almacenamiento estructurado para análisis posterior.

Esta automatización proporciona **beneficios estratégicos tangibles** para cualquier empresa orientada al cliente, entre los que destacan:

**1. Respuesta temprana ante clientes insatisfechos**

La automatización detecta y alerta al equipo cuando se recibe un feedback negativo, lo que permite actuar de inmediato antes de que la insatisfacción se traduzca en pérdida de clientes o mala reputación.


**2. Registro estructurado del feedback por tipo de sentimiento**

Los comentarios se clasifican y almacenan por separado (positivos, neutrales y negativos), lo que facilita su análisis posterior para detectar patrones, medir la evolución de la satisfacción o generar dashboards en herramientas como Power BI.

​
**3. Ahorro de tiempo y eficiencia operativa**

El proceso elimina tareas manuales repetitivas como revisar formularios, enviar correos o filtrar comentarios, permitiendo que el equipo se enfoque en resolver problemas en lugar de identificarlos.


**4. Aplicación práctica de IA en procesos de negocio**

Se demuestra cómo integrar modelos de lenguaje como GPT en flujos reales de trabajo, generando análisis semánticos automatizados sin necesidad de intervención humana.


**5. Reconocimiento proactivo a clientes satisfechos**

A través del análisis del sentimiento, el sistema envía automáticamente correos de agradecimiento a los usuarios que valoran positivamente el servicio, reforzando su fidelidad y mejorando la imagen de marca.


## Habilidades demostradas en este proyecto

**1. Automatización de procesos con Make​ (Integromat)**

- Diseño de flujos automatizados multi-condicionales.

- Uso de routers, filtros, y conexiones entre aplicaciones externas (Google Sheets, Gmail, OpenAI).

​
**2. Integración de herramientas no-code**

- Conexión entre Google Forms, Sheets, Gmail y OpenAI a través de Make.

- Configuración de flujos sin necesidad de desarrollo tradicional.

​
**3. Análisis de sentimiento con IA**

- Uso de modelos GPT para analizar texto y clasificar el tono del feedback.

- Diseño de prompts efectivos para obtener respuestas consistentes y clasificables.


**4. Toma de decisiones automatizada**

- Activación de acciones distintas en función de puntuación y sentimiento detectado.

- Generación de respuestas personalizadas y envío de alertas críticas sin intervención humana.

​
**​5. Diseño de sistemas escalables y reutilizables**

- Arquitectura de un flujo que puede adaptarse fácilmente a nuevos formularios, áreas o canales.

- Preparación del sistema para integrar análisis en Power BI o dashboards de satisfacción.


**6. Pensamiento de negocio**

- Enfoque orientado a mejorar la experiencia del cliente, reducir tiempos de respuesta y optimizar procesos de soporte.

## Propósito y contexto del proyecto

Este proyecto tiene como objetivo diseñar una automatización con Make que permita capturar en tiempo real las valoraciones y comentarios de los clientes, almacenar los datos de forma estructurada y generar alertas inmediatas ante feedback negativo. Su propósito principal es actuar de manera proactiva ante señales de insatisfacción, reduciendo los tiempos de respuesta del equipo de soporte, optimizando la gestión de incidencias y mejorando la experiencia global del cliente.



 ## Desarrollo técnico de la automatización
 
 A continuación se detalla el proceso técnico seguido para construir la automatización del feedback, desde el diseño del formulario hasta la activación de acciones automáticas en función del análisis de las respuestas.
 

El sistema se desarrolló utilizando Make como plataforma principal de integración y automatización, junto con Google Forms, Google Sheets, Gmail y OpenAI GPT. Cada fase responde a una necesidad concreta del proceso de atención al cliente, optimizando la gestión de opiniones y facilitando una respuesta rápida y personalizada.


 ### Fases del desarrollo del proyecto
 
 ![Captura de pantalla 2025-05-26 134113](https://github.com/user-attachments/assets/9ea61be1-956b-4590-a9a5-8a2e516b30fd)

**1. Diseño del formulario de recogida de feedback**

Se creó un formulario en Google Forms para capturar la opinión del cliente tras su experiencia. Incluye campos como puntuación general, comentarios positivos y aspectos a mejorar, además de nombre y correo electrónico opcionales.

**2. Almacenamiento automático en Google Sheets**

El formulario se conectó con una hoja de cálculo en Google Sheets, donde cada nueva respuesta se almacena de forma estructurada en tiempo real, sirviendo como base de datos para la automatización.

​
**3. Creación del escenario en Make**

Se diseñó un escenario en Make para vigilar constantemente la llegada de nuevas respuestas al formulario. Este flujo se activa automáticamente con cada nueva fila añadida en la hoja.

![Captura de pantalla 2025-05-26 134207](https://github.com/user-attachments/assets/f8877ee4-0fdf-4d27-a045-a28e0b5f57ed)


**4. Detección de puntuaciones bajas**

Se añadió un filtro en el flujo de Make para identificar las respuestas con puntuaciones iguales o inferiores a 3, lo que indica una experiencia insatisfactoria o potencialmente crítica.

**5. Envío automático de alerta al equipo de soporte**

Cuando se detecta una puntuación baja, se activa un módulo de Gmail que envía automáticamente un correo de alerta al equipo de atención al cliente, con todos los detalles de la opinión para su seguimiento inmediato.

![Captura de pantalla 2025-05-26 134228](https://github.com/user-attachments/assets/644cc978-8f8b-4a82-a650-6cec00b205e4)


**6. Análisis de sentimiento con OpenAI GPT**

A continuación, el texto del comentario es enviado a la API de OpenAI GPT, que clasifica automáticamente el sentimiento del cliente como positivo, neutral o negativo. Esto permite una categorización más precisa basada en el contenido, no solo en la puntuación.

![Captura de pantalla 2025-05-26 134255](https://github.com/user-attachments/assets/36cebe93-b169-44d1-9adc-43c43af44ca2)


**7. Enrutamiento de acciones según el sentimiento detectado**

Mediante un router en Make, el flujo se divide en tres ramas dependiendo del resultado del análisis de sentimiento:

- Positivo: Se envía automáticamente un correo de agradecimiento al cliente.

- Neutral: Se registra el feedback para análisis posterior.

- Negativo: Se refuerza la alerta y se almacena la opinión en una hoja específica para hacer seguimiento.

![Captura de pantalla 2025-05-26 134311](https://github.com/user-attachments/assets/74af9eda-c489-410c-93ae-7d2131fe40f4)


**8. Registro estructurado para análisis posterior**

Todas las respuestas son almacenadas en distintas pestañas de Google Sheets según su categoría de sentimiento. Esto permite construir informes, dashboards o análisis en Power BI con segmentaciones relevantes y accionables.

![Captura de pantalla 2025-05-26 134328](https://github.com/user-attachments/assets/05e5da42-4e3a-4ca7-9ad4-f9cb7bd63eb8)

## Reflexiones finales y aprendizajes

Este proyecto ha sido una oportunidad para aplicar de forma práctica y combinada muchas de las competencias que estoy desarrollando como analista de datos y profesional orientada a la **automatización inteligente de procesos**. A través de herramientas no-code, servicios cloud e inteligencia artificial, he podido construir una **solución que automatiza por completo la gestión del feedback, desde su captura hasta la respuesta personalizada según el tipo de sentimiento.**


Uno de los principales aprendizajes ha sido la importancia de diseñar flujos centrados en el usuario final, donde **cada dato recogido se traduce en una acción concreta que aporta valor**, ya sea mejorando la experiencia del cliente o facilitando el trabajo del equipo interno. 
​

Además, este proyecto me ha permitido consolidar habilidades de diseño modular de escenarios, aplicación de lógica condicional, integración entre plataformas y estructuración de datos para su análisis posterior.


La experiencia de construir este sistema de principio a fin me ha reafirmado en la importancia de automatizar con propósito: **no solo para ahorrar tiempo, sino para tomar decisiones más informadas, rápidas y efectivas.**


## Contacto
