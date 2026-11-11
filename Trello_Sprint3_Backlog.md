# Trello — Sprint 3: Backend biciGO (contenido listo para pegar)

> **Cómo usar este archivo:** crea el tablero, las 4 listas y las etiquetas; luego crea cada tarjeta copiando el **Título** y la **Descripción** indicados, asigna al **Responsable** y colócala en la **Lista** indicada. Al finalizar, copia el enlace del tablero y pégalo en el marcador `PENDIENTE DE ENLACE` de la sección **5.2.3.3** del `Capitulo_5.md`, junto con una captura del tablero.

**Nombre del tablero:** `Sprint 3 — Backend biciGO (backend-bicigo)`
**Repositorio asociado:** https://github.com/Startup-Chapa/backend-bicigo

---

## 1. Listas del tablero

1. `To-do`
2. `In-Process`
3. `To-Review`
4. `Done`

## 2. Etiquetas sugeridas

| Etiqueta | Color sugerido | Uso |
|---|---|---|
| `shared` | Amarillo | Persistencia, seeder y OpenAPI (transversal) |
| `iam` | Verde | Users y notificaciones |
| `trip` | Azul | Ciclo de alquiler y QR |
| `billing` | Naranja | Pagos, métodos, planes y suscripciones |
| `fleet` | Morado | Bicicletas, puntos y asignaciones |
| `maintenance` | Rojo | Reportes e historial de estados |
| `qa-docs` | Gris | Pruebas locales y documentación del informe |

## 3. Miembros del tablero

| Integrante | Usuario GitHub | Contexto liderado |
|---|---|---|
| Armestar Felipa, Adrian Andres | Adrian5102 | IAM |
| Franco del Carpio, José María | VoltTrd | Trip Management |
| Ayllon Pauccar, Juan David | JuanDPAUC | Billing & Subscriptions |
| Aguirre Ramos, Eduardo Manuel | TheEngineEdu | Maintenance |
| Velasquez Velasquez, Rodrigo | Rodrigov233 | Fleet & Station Management |

> **Nota de rotación:** respecto al Sprint 2, Fleet y Maintenance rotaron intencionalmente entre Eduardo Aguirre y Rodrigo Velasquez (Rodrigo → Fleet, Eduardo → Maintenance).

## 4. Distribución de tarjetas en las listas

- **To-Review:** T3-19 (pruebas locales de la API, pendiente de adjuntar capturas).
- **Done:** todas las demás tarjetas (T3-01 a T3-18 y T3-20), correspondientes al trabajo ya implementado en `backend-bicigo`.
- **To-do / In-Process:** vacías al cierre del Sprint (usarlas si se replanifica algún trabajo).

---

## 5. Tarjetas (20)

### Transversal — Shared (etiqueta `shared`)

**Tarjeta T3-01 — [SHARED][BACK] Solución y estructura por Bounded Contexts**
- Lista: `Done` · Etiqueta: `shared` · Responsable: Equipo
- Descripción:
  > Crear la solución .NET 10 con las carpetas Iam, Trip, Billing, Fleet, Maintenance y Shared, y registrar los servicios de cada contexto en Program.cs.
- Checklist:
  - [x] Carpetas por bounded context creadas
  - [x] Program.cs registra repos, servicios de comando/consulta y UnitOfWork

**Tarjeta T3-02 — [SHARED][BACK] AppDbContext MySQL y repositorios base**
- Lista: `Done` · Etiqueta: `shared` · Responsable: Equipo
- Descripción:
  > Configurar AppDbContext con MySQL (MySql.EntityFrameworkCore), UnitOfWork, BaseRepository y AuditableEntityInterceptor.
- Checklist:
  - [x] Connection string `DefaultConnection` en appsettings.json
  - [x] UnitOfWork y BaseRepository funcionales

**Tarjeta T3-03 — [SHARED][BACK] Seeder y tablas normalizadas**
- Lista: `Done` · Etiqueta: `shared` · Responsable: Equipo
- Descripción:
  > Implementar DatabaseSeeder y la creación idempotente de plan_features, user_notifications, bicycle_assignments, trip_users, trip_route_points, trip_photo_evidences y maintenance_status_histories.
- Checklist:
  - [x] DatabaseSeeder aplicado al arranque
  - [x] CREATE TABLE IF NOT EXISTS para las 7 tablas

**Tarjeta T3-04 — [SHARED][DOCS] OpenAPI 3.1.1 y Scalar**
- Lista: `Done` · Etiqueta: `shared` · Responsable: Equipo
- Descripción:
  > Habilitar AddOpenApi/MapOpenApi y MapScalarApiReference para documentar y explorar la API en el entorno local.
- Checklist:
  - [x] OpenAPI 3.1.1 expuesto
  - [x] Scalar disponible en localhost:5267

### IAM (etiqueta `iam`)

**Tarjeta T3-05 — [IAM][BACK] Dominio y aplicación de Users**
- Lista: `Done` · Etiqueta: `iam` · Responsable: Adrian Armestar (Adrian5102)
- Descripción:
  > Modelar el agregado User con sus comandos y consultas (registro, consulta por correo), su repositorio y los servicios de aplicación.
- Checklist:
  - [x] Agregado User + value objects
  - [x] Repositorio y servicios de comando/consulta

**Tarjeta T3-06 — [IAM][BACK] Users REST: CRUD y PATCH de perfil**
- Lista: `Done` · Etiqueta: `iam` · Responsable: Adrian Armestar (Adrian5102)
- Descripción:
  > Exponer POST /api/v1/users (201/400/409), GET /api/v1/users?email=, GET /{id}, PATCH /{id} (perfil, plan y balance) y DELETE /{id} con assemblers.
- Checklist:
  - [x] Registro con 201/400/409
  - [x] Filtro por correo para login del frontend
  - [x] PATCH de perfil, plan y balance

**Tarjeta T3-07 — [IAM][BACK] UserNotifications REST**
- Lista: `Done` · Etiqueta: `iam` · Responsable: Adrian Armestar (Adrian5102)
- Descripción:
  > Implementar GET/POST /api/v1/user-notifications y PATCH /{id}/read para las notificaciones del usuario.
- Checklist:
  - [x] Listado y creación de notificaciones
  - [x] Marcar como leída

### Trip Management (etiqueta `trip`)

**Tarjeta T3-08 — [TRIP][BACK] Dominio y persistencia de Trips**
- Lista: `Done` · Etiqueta: `trip` · Responsable: José María Franco (VoltTrd)
- Descripción:
  > Modelar el agregado Trip con sus estados, comandos y consultas, y su repositorio EFC.
- Checklist:
  - [x] Agregado Trip + TripStatus
  - [x] Comandos y consultas de viaje

**Tarjeta T3-09 — [TRIP][BACK] Trips REST: ciclo de alquiler**
- Lista: `Done` · Etiqueta: `trip` · Responsable: José María Franco (VoltTrd)
- Descripción:
  > Exponer POST /api/v1/trips (inicio), GET /{id} (consulta), PUT /{id} (actualización y cierre), DELETE /{id} y el listado GET /api/v1/trips.
- Checklist:
  - [x] Inicio de alquiler (TS-08)
  - [x] Consulta del viaje (TS-10)
  - [x] Actualización y cierre (TS-11)

**Tarjeta T3-10 — [TRIP][BACK] TripUsers REST**
- Lista: `Done` · Etiqueta: `trip` · Responsable: José María Franco (VoltTrd)
- Descripción:
  > Implementar GET/POST /api/v1/trip-users y GET /{id} para asociar usuarios al viaje.
- Checklist:
  - [x] Registro de usuarios del viaje
  - [x] Consulta por identificador

**Tarjeta T3-11 — [TRIP][BACK] Route points y evidencias fotográficas**
- Lista: `Done` · Etiqueta: `trip` · Responsable: José María Franco (VoltTrd)
- Descripción:
  > Implementar api/v1/trip-route-points y api/v1/trip-photo-evidences (consulta y registro).
- Checklist:
  - [x] Puntos de recorrido con secuencia
  - [x] Evidencias fotográficas del viaje

**Tarjeta T3-12 — [TRIP][BACK] QrValidations REST**
- Lista: `Done` · Etiqueta: `trip` · Responsable: José María Franco (VoltTrd)
- Descripción:
  > Implementar GET/POST /api/v1/qr-validations y GET /{id} para la validación QR del desbloqueo del alquiler vigente.
- Checklist:
  - [x] Registro de validación QR (TS-09)
  - [x] Consulta de validaciones

### Billing & Subscriptions (etiqueta `billing`)

**Tarjeta T3-13 — [BILLING][BACK] PaymentMethods y Payments REST**
- Lista: `Done` · Etiqueta: `billing` · Responsable: Juan David Ayllon (JuanDPAUC)
- Descripción:
  > Implementar GET/POST /api/v1/payment-methods, GET/POST /api/v1/payments y GET /payments/{id}.
- Checklist:
  - [x] Registro de métodos de pago (TS-12)
  - [x] Procesamiento de pagos (TS-13)

**Tarjeta T3-14 — [BILLING][BACK] Plans, PlanFeatures y Subscriptions**
- Lista: `Done` · Etiqueta: `billing` · Responsable: Juan David Ayllon (JuanDPAUC)
- Descripción:
  > Exponer GET /api/v1/plans y GET /{id}, GET/POST /api/v1/plan-features y GET/POST /api/v1/subscriptions (activación de plan).
- Checklist:
  - [x] Catálogo de planes y características
  - [x] Activación de suscripción (TS-14)

### Fleet & Station Management (etiqueta `fleet`)

**Tarjeta T3-15 — [FLEET][BACK] Bicycles REST y estados**
- Lista: `Done` · Etiqueta: `fleet` · Responsable: Rodrigo Velasquez (Rodrigov233)
- Descripción:
  > Modelar el agregado Bicycle con el value object BicycleStatus y exponer GET/POST/PUT/DELETE /api/v1/bicycles (disponibilidad y detalle).
- Checklist:
  - [x] CRUD completo de bicicletas
  - [x] Estados de bicicleta (BicycleStatus)

**Tarjeta T3-16 — [FLEET][BACK] BikePoints y BicycleAssignments**
- Lista: `Done` · Etiqueta: `fleet` · Responsable: Rodrigo Velasquez (Rodrigov233)
- Descripción:
  > Implementar GET/POST/PUT/DELETE /api/v1/bike-points y GET/POST /api/v1/bicycle-assignments (ubicación y asignaciones).
- Checklist:
  - [x] CRUD de puntos/estaciones
  - [x] Asignaciones bicicleta–punto

### Maintenance (etiqueta `maintenance`)

**Tarjeta T3-17 — [MAINT][BACK] MaintenanceReports REST**
- Lista: `Done` · Etiqueta: `maintenance` · Responsable: Eduardo Aguirre (TheEngineEdu)
- Descripción:
  > Modelar el reporte de mantenimiento e implementar GET/POST /api/v1/maintenance-reports y GET /{id}.
- Checklist:
  - [x] Registro de reportes (TS-17)
  - [x] Consulta y seguimiento (TS-18)

**Tarjeta T3-18 — [MAINT][BACK] Cambio de estado e historial**
- Lista: `Done` · Etiqueta: `maintenance` · Responsable: Eduardo Aguirre (TheEngineEdu)
- Descripción:
  > Implementar POST /api/v1/maintenance-reports/{bikeId}/status y GET/POST /api/v1/maintenance-status-histories con el agregado MaintenanceStatusHistory.
- Checklist:
  - [x] Cambio de estado administrativo (TS-19)
  - [x] Historial de estados persistido

### QA y documentación (etiqueta `qa-docs`)

**Tarjeta T3-19 — [QA][BACK] Pruebas locales de la API**
- Lista: `To-Review` · Etiqueta: `qa-docs` · Responsable: Equipo
- Descripción:
  > Ejecutar la API con MySQL y verificar los contratos de cada contexto desde Scalar: al menos una respuesta exitosa y un caso de error por recurso. Adjuntar capturas para la sección 5.2.3.5 del informe.
- Checklist:
  - [ ] Capturas exitosas por contexto (IAM, Trip, Billing, Fleet, Maintenance)
  - [ ] Casos de error (p. ej., 409 en correo duplicado)
  - [ ] Video de ejecución con enlace

**Tarjeta T3-20 — [DOCS] Documentación del Sprint 3 en el informe**
- Lista: `Done` · Etiqueta: `qa-docs` · Responsable: Eduardo Aguirre (TheEngineEdu)
- Descripción:
  > Redactar las secciones 5.2.3.1 a 5.2.3.8 y actualizar la tabla de repositorios de 5.1.2 con backend-bicigo.
- Checklist:
  - [x] Secciones del Capítulo V redactadas
  - [x] Repositorio backend registrado en 5.1.2

---

## 6. Pasos finales

1. Crear el tablero con el nombre indicado y compartirlo con los 5 integrantes.
2. Crear las 4 listas y las 7 etiquetas.
3. Crear las 20 tarjetas con título, descripción, etiqueta, responsable y checklist según la sección 5.
4. Copiar el **enlace del tablero** y pegarlo en `Capitulo_5.md`, sección 5.2.3.3 (marcador `Trello Sprint 3: PENDIENTE DE ENLACE`).
5. Adjuntar una **captura del tablero** en `Resources/chapter5/` (sugerido: `trello3.png`) y referenciarla en 5.2.3.3.
