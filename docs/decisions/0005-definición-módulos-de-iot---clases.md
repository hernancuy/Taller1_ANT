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

* Crear las tablas: ObjetoSensor, ObjetotipoSensor

## Decision Outcome

Chosen option: "Crear las tablas: ObjetoSensor, ObjetotipoSensor", because Modela correctamente los requisitos de software
