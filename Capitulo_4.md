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

El diagrama de contexto de la arquitectura de software representa la interacción entre la plataforma web de alquiler de bicicletas y los actores o servicios externos que participan en su funcionamiento.

El sistema central corresponde a la **Plataforma Web de Alquiler de Bicicletas**, la cual permite a los usuarios registrarse, consultar bicicletas disponibles, seleccionar zonas de recogida y devolución, iniciar y finalizar viajes y consultar su historial.

Los principales elementos externos que interactúan con la plataforma son:

- **Usuario:** utiliza la plataforma para registrarse, consultar bicicletas disponibles, realizar viajes y revisar el historial de sus recorridos.
- **Usuario Premium:** además de las funcionalidades habituales, cuenta con una suscripción Premium que le permite utilizar el servicio sin pagar la tarifa correspondiente al kilometraje durante la vigencia de su suscripción.
- **Administrador:** gestiona los usuarios, bicicletas, zonas habilitadas y suscripciones dentro de la plataforma.
- **Servicio de Geolocalización:** proporciona información de ubicación y permite determinar la distancia recorrida durante un viaje.
- **Pasarela de Pagos:** procesa los pagos correspondientes al servicio y las suscripciones Premium.

### Diagrama de Contexto

```plantuml
@startuml
title Software Architecture Context Diagram - Servicio de Bicicletas

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
