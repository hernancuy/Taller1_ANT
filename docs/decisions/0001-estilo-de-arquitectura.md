# 0001.Estilo de arquitectura - Event Driven

* Status: accepted
* Deciders: Hernan Cuy
* Date: 2023-06-18

Technical Story: 0001.Estilo de arquitectura - Event Driven

## Context and Problem Statement

En la definicion vemos la necesidad de un sistema centralizado capaz de tomar los eventos enviados por los sensores de las máquinas y otros sistemas suscritos que los lean y tomen acción, algunos suscriptores toman la informacion para realizar la analitica de los procesos, otros para determinar en tiempo real el estado de la linea de producción y visualizarlos.

## Decision Drivers

* RF-1 Visualizador del estado del proceso.
* RF-7 Sistema de mensajería de suscripción.
* RF-9 Software de mensajería
* Por el volumen de informacion que tiene el sistema, solo alguna de ellas es de interés por sistemas especificos
* Por que se requiere un sistema realtime que atienda los eventos que se generan desde los sensores

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

* Good, because Es lo más usado en la web por tanto existe muchos ingenieros capacitados en el uso de este patrón
* Bad, because No modela correctamente la menera como los sensores interactuan con un sistema de informacion

## Links

* https://statics.teams.cdn.office.net/evergreen-assets/safelinks/1/atp-safelinks.html
