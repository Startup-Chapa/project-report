# CAPÍTULO IV: PRODUCT DESIGN

## 4.1. Style Guidelines

### 4.1.1. General Style Guidelines

### 4.1.2. Web Style Guidelines

## 4.2. Information Architecture

### 4.2.1. Organization Systems

### 4.2.2. Labeling Systems

### 4.2.3. SEO Tags and Meta Tags

### 4.2.4. Searching Systems

### 4.2.5. Navigation Systems

## 4.3. Landing Page UI Design

### 4.3.1. Landing Page Wireframe

### 4.3.2. Landing Page Mock-up

## 4.4. Web Applications UX/UI Design

### 4.4.1. Web Applications Wireframes

### 4.4.2. Web Applications Wireflow Diagrams

### 4.4.2. Web Applications Mock-ups

### 4.4.3. Web Applications User Flow Diagrams

## 4.5. Web Applications Prototyping

## 4.6. Domain-Driven Software Architecture

### 4.6.1. Design-Level EventStorming

### 4.6.2. Software Architecture Context Diagram

# 4.6.2. Software Architecture Context Diagram

## Descripción

El diagrama de contexto de la arquitectura de software representa la interacción entre la **Plataforma Web de Alquiler de Bicicletas** y los principales actores y servicios externos que participan en su funcionamiento.

La plataforma permite a los usuarios registrarse, consultar bicicletas disponibles, seleccionar zonas de recogida y devolución, iniciar y finalizar viajes y consultar el historial de sus recorridos.

El sistema también contempla usuarios con una suscripción **Premium**, quienes pueden utilizar el servicio sin pagar la tarifa correspondiente al kilometraje durante la vigencia de dicha suscripción.

Además, la plataforma se comunica con servicios externos para obtener información de ubicación y distancia recorrida, así como para procesar las operaciones de pago.

---

## Actores y sistemas externos

### Usuario

El usuario interactúa directamente con la plataforma para:

- Registrarse e iniciar sesión.
- Consultar bicicletas disponibles.
- Consultar las zonas habilitadas.
- Seleccionar una bicicleta.
- Seleccionar una zona de recogida.
- Iniciar un viaje.
- Finalizar un viaje.
- Devolver la bicicleta.
- Consultar los kilómetros recorridos.
- Consultar el costo de sus viajes.
- Revisar el historial de viajes.

### Usuario Premium

El usuario Premium dispone de las mismas funcionalidades que un usuario regular, pero cuenta adicionalmente con los beneficios de una suscripción Premium.

Durante la vigencia de la suscripción:

- Puede realizar viajes normalmente.
- El sistema verifica su estado Premium al finalizar el viaje.
- No se aplica el cobro correspondiente al kilometraje recorrido.
- Puede gestionar y consultar el estado de su suscripción.

### Administrador

El administrador utiliza la plataforma para gestionar los principales elementos del servicio:

- Usuarios.
- Bicicletas.
- Zonas habilitadas.
- Puntos de recogida.
- Puntos de devolución.
- Viajes.
- Suscripciones Premium.

### Servicio de Geolocalización

El servicio de geolocalización es un sistema externo que proporciona información relacionada con la ubicación y la distancia recorrida.

La plataforma puede utilizar esta información para:

- Obtener la ubicación de las bicicletas.
- Registrar la ubicación durante un viaje.
- Determinar la distancia recorrida.
- Utilizar los kilómetros registrados para calcular la tarifa correspondiente.

### Pasarela de Pagos

La pasarela de pagos es un servicio externo encargado de procesar las operaciones económicas realizadas mediante la plataforma.

Puede utilizarse para:

- Procesar el pago de los viajes.
- Procesar el pago de las suscripciones Premium.
- Informar el resultado de una operación de pago.

---

## Sistema central

El sistema central corresponde a la:

**Plataforma Web de Alquiler de Bicicletas**

Esta plataforma concentra las funcionalidades principales del servicio y actúa como intermediario entre los usuarios, el administrador y los servicios externos.

Entre sus responsabilidades se encuentran:

- Gestión de usuarios.
- Gestión de bicicletas.
- Gestión de zonas.
- Gestión de viajes.
- Registro de kilómetros recorridos.
- Cálculo de tarifas.
- Gestión de suscripciones Premium.
- Procesamiento de solicitudes de pago.
- Integración con el servicio de geolocalización.

---

## Diagrama de Contexto

```plantuml
@startuml
title 4.6.2. Software Architecture Context Diagram

left to right direction

actor "Usuario" as Usuario
actor "Usuario Premium" as Premium
actor "Administrador" as Admin

rectangle "Plataforma Web de\nAlquiler de Bicicletas" as Sistema

rectangle "Servicio de\nGeolocalización" as Geo
rectangle "Pasarela de Pagos" as Pago

Usuario --> Sistema : Registro, consultas,\nalquiler y viajes

Premium --> Sistema : Gestión de viajes\ny beneficios Premium

Admin --> Sistema : Gestión de usuarios,\nbicicletas, zonas y suscripciones

Sistema --> Geo : Solicitar ubicación\ny registrar distancia

Geo --> Sistema : Ubicación y distancia\nrecorrida

Sistema --> Pago : Solicitar procesamiento\nde pagos

Pago --> Sistema : Resultado de la operación

@enduml


### 4.6.3. Software Architecture Container Diagrams

### 4.6.4. Software Architecture Components Diagrams

## 4.7. Software Object-Oriented Design

### 4.7.1. Class Diagrams

## 4.8. Database Design

### 4.8.1. Database Diagrams
