# Definicion de motor de analitica de datos - Tableau

* Status: proposed
* Date: 2023-06-19

Technical Story: Definicion de motor de analitica de datos

## Context and Problem Statement

Se requiere un sistema capaz de tomar la informacion persistida por los sistemas de gestion de eventos de los sensores para realizar la visualización de datos.

## Decision Drivers

* RF-1 Visualizador del estado del proceso.
* RF-3 Sistema de monitoreo
* RF-6 Algoritmos predictivos

## Considered Options

* Tableau
* Power BI

## Decision Outcome

Chosen option: "Power BI", because Curva de aprendizaje, no se requiere analitica avanzada, es la alternativa de menos costo

## Pros and Cons of the Options

### Tableau

Software de análisis de datos con una capa de visualización y presentación, considerado por muchos como uno de los mejores programas para la presentación visual de datos.

* Good, because Manejo de altos volumenes de datos
* Good, because Cuenta con una amplia gama de capacidades análiticas (Regresiones, Analisis estadisticos, Modelos predictivos)
* Bad, because Costo
* Bad, because Requiere curva de aprendizaje

### Power BI

Es un sistema predictivo, inteligente y de gran apoyo, capaz de traducir los datos en gráficas, paneles o informes por sus cualidades como la capacidad gráfica de presentación de la información, o la integración de Power Query: el motor de extracción, transformación y carga (ETL) incluido en Excel.

* Good, because Integracion con el ecosistema de Microsoft
* Good, because Interfaz intuitiva y facil de usar
* Good, because Integracion con servicios en la nube
* Good, because Permite colaboracion entre usuarios.
* Good, because Permite definir y entrenar modelos de Machine Learning sobre la herramienta
* Bad, because Limitaciones en terminos de opciones de presentacion avanzada es decir pocas opciones de diseño avanzado
