# Definición módulos de ordenes - Relacional

* Status: proposed
* Date: 2023-06-18

Technical Story: Módulo de ordenes

## Context and Problem Statement

RF-2 Módulo de ordenes de trabajo.
Se debe disponer de un módulo gestor de órdenes de trabajo donde se especifiquen las asignaciones de órdenes por operario y máquinas que van a fabricar cada componente, Cabe resaltar que al cambiar el estado de una orden el operario que se encargará de ella será asignado de acuerdo con la disponibilidad

Este módulo de ordenes requiere: 
TablaOrden
IdOrden
DescripciónOrden
FechaCreacionOrden
IdOperario
EstadoOrden
FechaInicioProduccion
FechaDespacho

TablaOrdenProducto
IdOrden
IdProducto

TablaProductosMaterial
idProducto
idMateriales

TablaMateriales
IdMaterial
DescripcionMaterial
CantidadMaterialInventario

## Decision Drivers

* RF-2 Módulo de ordenes de trabajo.
* RF-4 Almacenamiento de datos

## Considered Options

* Crear tablas relacionales: Orden, OrdenProducto, ProductosMaterial, Materiales
* Crear colecciones (no relacionales): Orden, OrdenProducto, ProductosMaterial, Materiales

## Decision Outcome

Chosen option: "Crear tablas relacionales: Orden, OrdenProducto, ProductosMaterial, Materiales", because Las bases relacionales tienen mejor consistencia de datos

## Pros and Cons of the Options

### Crear tablas relacionales: Orden, OrdenProducto, ProductosMaterial, Materiales

Se solicita la creacion de tablas relacionales Orden, OrdenProducto, ProductosMaterial, Materiales

* Good, because Las bases relacionales tienen mejor consistencia de datos
* Good, because El móduilo de ordenes consiste en informacion estructurada
* Bad, because Menos eficiencia que las bases de datos no relacionales

### Crear colecciones (no relacionales): Orden, OrdenProducto, ProductosMaterial, Materiales

Se solicita la creacion de colecciones Orden, OrdenProducto, ProductosMaterial, Materiales

* Good, because Por la naturaleza de los datos
* Good, because Por que la base de datos del procesamiento es informacion no relacional
* Bad, because Las bases relacionales tienen mejor consistencia de datos
