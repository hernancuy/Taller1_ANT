# Módulo de notificaciones

* Status: proposed
* Date: 2023-06-18

## Context and Problem Statement

RF-7 El sistema de la fábrica 4.0 debe contar con un sistema de mensajería interno que permita notificar de manera permanente a los operarios. Además, los operarios deben tener la capacidad de suscribirse a diferentes eventos y notificaciones, como actualizaciones de la producción, fallos en los sensores o sobrecarga en la producción según su rol se lo permita.

-	Sistema de mensajería interno: El sistema debe incluir un sistema de mensajería interno que sea confiable en términos de envío de mensajes. Algunas alternativas sugeridas son MQTT, Apache Kafka o una solución similar. La elección final del sistema de mensajería debe ser realizada considerando los requisitos y las características específicas del proyecto.

-	Suscripción a eventos y notificaciones: Los operarios deben tener la capacidad de suscribirse a eventos y notificaciones específicas que sean relevantes para su trabajo. Esto implica que el sistema debe permitir que los operarios seleccionen los eventos y notificaciones a los que desean estar suscritos y recibir notificaciones en tiempo real.

-	Manejo de dispositivos con fallas: Si el número de intentos de conexión con un dispositivo que falla supera un umbral predefinido, se deben suspender los intentos de conexión y considerar al dispositivo como fuera de servicio. Esto implica que el sistema debe monitorear los intentos de conexión y tomar la decisión de suspenderlos de manera automática cuando se supere el umbral establecido.

## Considered Options

* Se debe contar con un componente de notificaciones que permita mantener a los usuarios al tanto de los sucesos de importancia ocurridos dentro de la plataforma.

## Decision Outcome

Chosen option: "Se debe contar con un componente de notificaciones que permita mantener a los usuarios al tanto de los sucesos de importancia ocurridos dentro de la plataforma.", because SNS. El componente SNS de Amazon permite enviar notificaciones a los usuarios a traves de dispositivos moviles.
