# Definición de algoritmo de optimización

* Status: proposed
* Date: 2023-06-19

Technical Story: Definición de algoritmo de optimización

## Context and Problem Statement

Se necesita de un algoritmo que permita optimizar las ordenes de trabajo al reducir el tiempo de ejecución y el costo de producción. Es decir, se debe especificar la capacidad aprovechada en cada máquina.

-	Este algoritmo debe analizar los datos relevantes, como la cantidad de órdenes de trabajo disponibles y la capacidad de las líneas de trabajo.
-	Utilizando técnicas de optimización, el algoritmo debe determinar la asignación óptima de las órdenes de trabajo a las líneas de trabajo disponibles, maximizando la eficiencia y el rendimiento general del sistema.
-	El algoritmo debe tener en cuenta restricciones adicionales, como los tiempos de procesamiento, los recursos necesarios y cualquier otra limitación específica del contexto.

## Decision Drivers

* RF-6.1 Algoritmo volúmenes de ordenes de trabajo
* RF-6.2 Algoritmo fallos de trabajo

## Considered Options

* El patrón Strategy

## Decision Outcome

Chosen option: "El patrón Strategy", because Permite la modificacion de un algoritmo (estrategia) sin necesidad de cambiar toda la programación.

## Pros and Cons of the Options

### El patrón Strategy

Strategy es un patrón de diseño de comportamiento que permite definir una familia de algoritmos, colocar cada uno de ellos en una clase separada y hacer sus objetos intercambiables dinamicamente

* Good, because El patrón Strategy permite alterar indirectamente el comportamiento del objeto durante el tiempo de ejecución asociándolo con distintos subobjetos que pueden realizar subtareas específicas de distintas maneras
* Bad, because Los clientes deben conocer las diferencias entre estrategias para poder seleccionar la adecuada
