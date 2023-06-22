# Definición módulos de IoT - Clases

* Status: accepted
* Deciders: Hernan Cuy
* Date: 2023-06-18

Technical Story: Definición módulos de IoT

## Context and Problem Statement

RF-5 Módulo de IoT
Se requiere un módulo de sensores que notifique el estado de las máquinas de acuerdo con la solicitud realizada por el operador. 

El software debe integrar dos familias de sensores IoT (sensores A y B), los cuales comparten cierta funcionalidad, pero presentan características diferentes dentro de cada familia. Específicamente, la familia de sensores A consta de tres sensores interconectados, donde el primer sensor envía información al segundo sensor, y a su vez, este segundo sensor envía información al tercer sensor.

ObjetoSensor
IdSensor
descripcion
tipoSensor
metaData
IdSensorPrerrequisito
IdSensorSiguiente

ObjetotipoSensor
idTipo
descripción
esAnidado

## Decision Drivers

* RF-5 Módulo de IoT
* RF-5.1 Familia sensores A
* RF-5.2	Familia sensores B

## Considered Options

* Utilizar patrón de arquitectura Chain of responsability

## Decision Outcome

Chosen option: "Utilizar patrón de arquitectura Chain of responsability", because Modela correctamente los requisitos de software descritos

## Pros and Cons of the Options

### Utilizar patrón de arquitectura Chain of responsability

Porque el patron change of responsability permite pasar solicitudes a lo largo de una cadena de controladores y al recibir la solicitud, cada controlador decide procesarla o pasarla al siguiente controlador de la cadena y ese es el comportamiento necesario para modelar los contraladores Tipo A

* Good, because Cada controlador puede decidir no pasar la solicitud más abajo en la cadena y detener el procesamiento posterior del mensaje.
* Bad, because Algunas solicitudes pueden terminar sin ser atendidas.
