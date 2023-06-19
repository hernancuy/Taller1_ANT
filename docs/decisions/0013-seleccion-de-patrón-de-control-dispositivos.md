# Seleccion de patrón de control dispositivos

* Status: proposed
* Date: 2023-06-19

Technical Story: Seleccion de patrón de control dispositivos

## Context and Problem Statement

Los sensores deben estar supervisados por algún sistema que identifique que un sensor no se encuentra disponible, esto es, que luego de n intentos de conexión fallida los marque indisponible y genere una notificación al centro de notificaciones.

## Decision Drivers

* RF-9 Sistema de control dispositivos

## Considered Options

* Patron circuit braker

## Decision Outcome

Chosen option: "Patron circuit braker", because Permite implementar el control informado en el requisito

## Pros and Cons of the Options

### Patron circuit braker

Es una opción para detectar fallos y encapsula la lógica de prevenir que un fallo se repita constantemente debido a un fallo temporal de un sistema backend o dificultades inesperadas del sistema.

* Good, because El patrón Circuit Breaker impide congestionar un sistema debido a solicitudes que sabemos de antemano que van a fallar
* Bad, because Algunas peticiones pueden perderse, se debe contemplar su uso mientras esas peticiones no sean relevantes.
