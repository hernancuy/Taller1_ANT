# 0001.Estilo de arquitectura - Event Driven

* Status: accepted
* Deciders: Hernan Cuy
* Date: 2023-06-18

Technical Story: 0001.Estilo de arquitectura - Event Driven

## Context and Problem Statement

En la definicion vemos la necesidad de un sistema centralizado capaz de capturar los eventos enviados por los sensores de las distintas máquinas y publicarlos a otros sistemas suscritos capaces de procesar los eventos en tiempo real, para efectos de monitorización o análisis, generando así insights que posteriormente serían presentados en diferentes dashboards para toma de decisiones y análisis del proceso productivo

## Decision Drivers

* RF-1 Visualizador del estado del proceso.
* RF-7 Sistema de mensajería de suscripción.
* RF-9 Software de mensajería
* Naturaleza de comunicacion de los sensores IoT
* Volumen de informacion que tiene el sistema, solo alguna de ellas es de interés por sistemas especificos

## Considered Options

* Sistema Event Driven
* Orientado a servicio

## Decision Outcome

Chosen option: "Sistema Event Driven", because Por que modela con mayor precision los requisitos del sistema, por la naturaleza asincrona de comunicacion de los sensores IoT que funcionan por eventos y por el alto volumen de informacion que tiene un sistema de factoria Inteligente 4.0 en la cual solo alguna es de interés por ciertos sistemas especificos que podrian suscribirse a la misma y procesarlos.

## Pros and Cons of the Options

### Sistema Event Driven

Las arquitecturas dirigidas por eventos (eda event-driven architectures) se basan en la detección, consumo y reacción a eventos, un evento representa un cambio significativo en el estado de un sistema, los eventos se transmiten entre sistema poco acoplados (“loosely coupled”) mediante mensajes

* Good, because Por la naturaleza asincrona de comunicacion de los sensores IoT
* Bad, because Los mensajes se publican y si no se gestionan correctamente los mensajes podrian perderse.
* Bad, because Complejidad de implementación

### Orientado a servicio

Rest or restful (representational state transfer) es utilizado en para acceso a servicios web y desarrollo web, es una arquitectura cliente-servidor sin estado (stateless), proporciona una interfaz uniforme

* Good, because Es lo más usado en la web por tanto existe mucho capital humano capacitado en el uso de este patrón
* Bad, because No modela correctamente la menera como los sensores interactuan con un sistema de informacion

## Links

* https://www.redhat.com/es/topics/integration/what-is-event-driven-architecture
* https://www.bbvanexttechnologies.com/blogs/que-es-una-arquitectura-event-driven/
