# CAPÍTULO V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

### 5.1.1. Software Development Environment Configuration

### 5.1.2. Source Code Management

### 5.1.3. Source Code Style Guide & Conventions

### 5.1.4. Software Deployment Configuration

## Descripción

La configuración de despliegue de software describe cómo se distribuyen los componentes de la **Plataforma Web de Alquiler de Bicicletas** en los diferentes nodos necesarios para su funcionamiento.

La solución utiliza una arquitectura cliente-servidor. El usuario accede a la plataforma mediante un navegador web, mientras que el servidor de aplicación procesa las solicitudes y ejecuta la lógica de negocio.

El servidor de aplicación se comunica con el servidor de base de datos y con los servicios externos de geolocalización y procesamiento de pagos.

---

## Nodos de despliegue

### 1. Dispositivo del Usuario

Corresponde al dispositivo utilizado por el usuario para acceder a la plataforma.

Dentro de este nodo se encuentran:

- Navegador web.
- Interfaz de la plataforma.
- Componentes de presentación.

El usuario puede utilizar este dispositivo para registrarse, iniciar sesión, consultar bicicletas, realizar viajes y gestionar su cuenta.

La comunicación con el servidor se realiza mediante **HTTPS**.

---

### 2. Servidor de Aplicación

El servidor de aplicación contiene la aplicación web y la lógica de negocio del sistema.

Entre sus principales responsabilidades se encuentran:

- Gestionar usuarios.
- Gestionar bicicletas.
- Gestionar zonas.
- Gestionar viajes.
- Gestionar suscripciones Premium.
- Registrar kilómetros recorridos.
- Calcular las tarifas.
- Verificar el estado Premium.
- Comunicarse con la base de datos.
- Comunicarse con el servicio de geolocalización.
- Comunicarse con la pasarela de pagos.

Este servidor recibe las solicitudes provenientes del cliente web, procesa la información y devuelve las respuestas correspondientes.

---

### 3. Servidor de Base de Datos

El servidor de base de datos almacena la información persistente necesaria para el funcionamiento de la plataforma.

Entre los principales datos almacenados se encuentran:

- Usuarios.
- Bicicletas.
- Zonas.
- Puntos de recogida.
- Puntos de devolución.
- Viajes.
- Kilómetros recorridos.
- Tarifas.
- Pagos.
- Suscripciones Premium.

El servidor de aplicación es el encargado de realizar las consultas y actualizaciones sobre la base de datos.

---

### 4. Servicio de Geolocalización

El servicio de geolocalización corresponde a un servicio externo utilizado por la plataforma.

Su función principal es proporcionar información relacionada con:

- Ubicación de las bicicletas.
- Ubicación durante el viaje.
- Distancia recorrida.
- Información necesaria para determinar los kilómetros del recorrido.

La información obtenida puede ser utilizada posteriormente por la lógica de negocio para calcular la tarifa del viaje.

---

### 5. Pasarela de Pagos

La pasarela de pagos corresponde a un servicio externo encargado de procesar las operaciones económicas.

Se utiliza para:

- Procesar pagos de los viajes.
- Procesar pagos de las suscripciones Premium.
- Confirmar el resultado de las operaciones.
- Informar si una operación fue procesada correctamente.

La plataforma no ejecuta directamente el procesamiento financiero, sino que delega esta responsabilidad a la pasarela correspondiente.

---

## Diagrama de Despliegue

```markdown
```plantuml
@startuml
title 5.1.4. Software Deployment Configuration

node "Dispositivo del Usuario" {
    artifact "Navegador Web" as Browser
    artifact "Interfaz de la Plataforma" as Frontend
}

node "Servidor de Aplicación" {
    artifact "Aplicación Web" as App
    artifact "Lógica de Negocio" as Business
}

database "Servidor de Base de Datos" as DB

node "Servicio de Geolocalización" as Geo

node "Pasarela de Pagos" as Payment

Browser --> Frontend : HTTPS
Frontend --> App : Solicitudes HTTPS

App --> Business : Procesamiento

Business --> DB : Consultas y actualización
DB --> Business : Datos

Business --> Geo : Solicitar ubicación\ny distancia
Geo --> Business : Ubicación y distancia

Business --> Payment : Solicitar pago
Payment --> Business : Resultado del pago

@enduml

## 5.2. Landing Page, Services & Applications Implementation

### 5.2.1. Sprint 1

#### 5.2.1.1. Sprint Planning 1

#### 5.2.1.2. Aspect Leaders and Collaborators

#### 5.2.1.3. Sprint Backlog 1

#### 5.2.1.4. Development Evidence for Sprint Review

#### 5.2.1.5. Execution Evidence for Sprint Review

#### 5.2.1.6. Services Documentation Evidence for Sprint Review

#### 5.2.1.7. Software Deployment Evidence for Sprint Review

#### 5.2.1.8. Team Collaboration Insights during Sprint

## 5.3. Validation Interviews

### 5.3.1. Diseño de Entrevistas

### 5.3.2. Registro de Entrevistas

### 5.3.3. Evaluaciones según heurísticas

## 5.4. Video About-the-Product
