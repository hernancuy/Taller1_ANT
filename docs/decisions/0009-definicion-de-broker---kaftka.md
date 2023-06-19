# Definicion de Broker - Kaftka

* Status: accepted
* Deciders: Hernan Cuy
* Date: 2023-06-19

Technical Story: Definición de broker de mensajería

## Context and Problem Statement

Se hace necesario definir un Broker que sea capaz de gestionar la mensajería de eventos usado por los sensores y las comunicaciones en general de la aplicacion. o

## Decision Drivers

* RF-7. Sistema de mensajería de suscripción

## Considered Options

* MQTT
* Kaftka

## Decision Outcome

Chosen option: "Kaftka", because Tiene baja latencia en la entrega de mensajes, ai bien requiere una curva de aprendizaje, contamos con desarrolladores capacitados en esta tecnología.

## Pros and Cons of the Options

### MQTT

Es el sistema de back-end que coordina los mensajes entre los diferentes clientes  Las responsabilidades del agente incluyen recibir y filtrar mensajes, identificar a los clientes suscritos a cada mensaje y enviarles los mensajes.

* Good, because Es liviano, requiere un mínimo ancho de banda en la trasmision de datos
* Good, because Se requiere poco espacio de memoria RAM para operar
* Good, because Amplia comunidad de usuarios
* Good, because Una Biblioteca con amplia gamma de opciones
* Good, because Permite la conexion persistentes entre los clientes y el broker, facilitando la comunicacion continua
* Bad, because Tiene dificultades para escalarse con grandes volumenes de datos
* Bad, because No proporciona retención a largo plazo de los mensajes

### Kaftka

Apache Kafka es una plataforma distribuida para la transmisión de datos que permite publicar, almacenar y procesar flujos de eventos de forma inmediata y tambien suscribirse a ellos. Está diseñada para administrar los flujos de datos de varias fuentes y enviarlos a distintos usuarios

* Good, because Kafka es una plataforma de transmisión distribuida que se enfoca en la transmisión de datos con alto rendimiento, es tolerante a fallas y escalable.
* Good, because Permite el almacenamiento de los mensajes por un tiempo definido
* Good, because Baja latencia en la entrega de mensajes
* Bad, because Complejo de configurar y administrar
* Bad, because Tiene una curva de aprendizaje a tener en cuenta

## Links

* https://www.hivemq.com/blog/mqtt-vs-kafka-real-time-bidirectional-data-processing/
