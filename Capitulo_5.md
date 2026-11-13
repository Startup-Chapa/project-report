# CAPÍTULO V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

### 5.1.1. Software Development Environment Configuration

| Categoría | Herramienta | Propósito | Enlace |
|---|---|---|---|
| Diseño UX/UI | Figma | Elaboración de wireframes, mockups y prototipos utilizados para definir la interfaz y experiencia de usuario de biciGO. | [https://www.figma.com/design/FIUjx83bu9OhBxZ4EMqyfe/Sin-t%C3%ADtulo?node-id=0-1&t=2NPsUYYjUh7xKI3R-1](https://www.figma.com/design/FIUjx83bu9OhBxZ4EMqyfe/Sin-t%C3%ADtulo?node-id=0-1&t=2NPsUYYjUh7xKI3R-1) |
| Investigación UX | UXPressia | Herramienta utilizada para elaborar los User Personas de los segmentos objetivo de biciGO, permitiendo representar sus características, necesidades, frustraciones y objetivos. | [https://uxpressia.com/](https://uxpressia.com/) |
| Planeamiento del Producto | UXPressia | Herramienta utilizada para desarrollar el Impact Mapping de biciGO, relacionando el objetivo del negocio, actores, impactos esperados y entregables asociados. | [https://uxpressia.com/](https://uxpressia.com/) |
| Modelado de Base de Datos | Draw.io | Elaboración del diagrama de base de datos de biciGO, incluyendo entidades, atributos, claves y relaciones entre las tablas del sistema. | [https://drive.google.com/file/d/1frY_P-cg-4JuKiY2Jh8m85aaZD9V1CCT/view?usp=sharing](https://drive.google.com/file/d/1frY_P-cg-4JuKiY2Jh8m85aaZD9V1CCT/view?usp=sharing) |
| Modelado de Dominio | Canva | Desarrollo del Event Storming utilizado para identificar eventos, procesos y elementos principales del dominio de biciGO. | [https://canva.link/7coo689oj2nx3b7](https://canva.link/7coo689oj2nx3b7) |
| Desarrollo Web | GitHub Pages | Despliegue público de la Landing Page de biciGO. | [https://startup-chapa.github.io/Landing-Page/](https://startup-chapa.github.io/Landing-Page/) |
| Frontend Deployment | Firebase Hosting | Plataforma utilizada para publicar la Frontend Web Application de biciGO y proporcionar acceso mediante una URL pública. | [https://firebase.google.com/](https://firebase.google.com/) |
| Backend Deployment | Railway | Plataforma utilizada para publicar la API de biciGO con MySQL gestionado y exponer los Web Services mediante una URL pública. | [https://backend-bicigo-production.up.railway.app/scalar/v1](https://backend-bicigo-production.up.railway.app/scalar/v1) |
| Framework frontend | Vue 3 | Construcción de las interfaces reactivas y los componentes de la aplicación web. | https://vuejs.org/ |
| Bundler y entorno de desarrollo | Vite | Servidor local y generación de archivos optimizados de producción en `dist`. | https://vite.dev/ |
| Estado y navegación | Pinia y Vue Router | Estado compartido, navegación entre vistas y separación de rutas por módulo. | https://pinia.vuejs.org/ |
| Biblioteca de componentes | PrimeVue | Controles, formularios, tablas y componentes de interfaz usados en la SPA. | https://primevue.org/ |
| Internacionalización | Vue I18n | Recursos de idioma en español e inglés y actualización de textos de interfaz. | https://vue-i18n.intlify.dev/ |
| API simulada | JSON Server | Simulación local de recursos del frontend mientras se implementan los Web Services definitivos. | https://github.com/typicode/json-server |
| Entorno de Desarrollo | WebStorm | Entorno utilizado para editar y organizar los archivos del proyecto, trabajar con Git y desarrollar los componentes web de biciGO. | [https://www.jetbrains.com/webstorm/](https://www.jetbrains.com/webstorm/) |
| Control de Versiones | Git | Sistema utilizado para registrar cambios, trabajar mediante ramas y mantener el historial del proyecto. | [https://git-scm.com/](https://git-scm.com/) |
| Repositorio Remoto | GitHub | Plataforma utilizada para almacenar el proyecto y facilitar el trabajo colaborativo entre los integrantes. | [https://github.com/](https://github.com/) |
| Documentación | Markdown | Formato utilizado para redactar y mantener los capítulos del informe, tablas, enlaces, imágenes y demás documentación del proyecto bajo un enfoque Docs-as-Code. | [https://www.markdownguide.org/](https://www.markdownguide.org/) |
| Gestión Ágil | Trello | Herramienta utilizada para organizar el Sprint Backlog, distribuir tareas y dar seguimiento al avance del equipo durante el Sprint. | [https://trello.com/invite/b/6aac96a6ce176e2f9d496d31/ATTI96186798f26dde57c47e51ca96f0fff04FDD51DF/sprint-web-1](https://trello.com/invite/b/6aac96a6ce176e2f9d496d31/ATTI96186798f26dde57c47e51ca96f0fff04FDD51DF/sprint-web-1) |
| Gestión del Producto | Product Backlog | Permite organizar y priorizar las User Stories y Technical Stories que forman parte del desarrollo de biciGO. | [https://trello.com/invite/b/6aac96a6ce176e2f9d496d31/ATTI96186798f26dde57c47e51ca96f0fff04FDD51DF/sprint-web-1](https://trello.com/invite/b/6aac96a6ce176e2f9d496d31/ATTI96186798f26dde57c47e51ca96f0fff04FDD51DF/sprint-web-1) |

### 5.1.2. Source Code Management

El equipo de **BiciGO — Startup-Chapa** utiliza Git y GitHub para gestionar el código de la Landing Page, la Frontend Web Application y la documentación del proyecto. Los repositorios asociados son los siguientes:

| Solución | Repositorio | Enlace | Observación |
|---|---|---|---|
| Informe | `project-report` | https://github.com/Startup-Chapa/project-report | Documentación en Markdown y evidencias |
| Landing Page | `Landing-Page` | https://github.com/Startup-Chapa/Landing-Page | Sitio informativo publicado con GitHub Pages |
| Frontend Web Application | `frontend-bicigo` | https://github.com/Startup-Chapa/frontend-bicigo | SPA desarrollada con Vue 3 y Vite |
| Backend / Platform | `backend-bicigo` | https://github.com/Startup-Chapa/backend-bicigo | API REST por Bounded Contexts implementada en el Sprint 3 (.NET 10, EF Core y MySQL) |

El repositorio del frontend tiene `main` como rama principal y utiliza `develop` como rama de integración. El trabajo por funcionalidad se distribuye en ramas tales como `feature/iam`, `feature/trip-management`, `feature/billing-subscriptions`, `feature/fleet-station-management` y `feature/maintenance`. El repositorio también conserva una rama `feature/corrections`. La documentación de integración señala que se consolidaron archivos de los módulos sobre una base compartida; por tanto, no corresponde afirmar que todos los cambios se integraron exclusivamente mediante *merge* o Pull Requests.

El flujo se inspira en prácticas de GitFlow y utiliza, cuando corresponde, ramas de funcionalidad y revisión. Las ramas `release/*` y `hotfix/*` se consideran convenciones para versiones posteriores; **no se declara su uso efectivo en el Sprint 2** sin evidencia. Las confirmaciones de cambios procuran una convención comprensible, por ejemplo `feat(iam): add login view` o `feat: integrate BiciGO frontend modules`. Algunos commits existentes utilizan otra redacción y se conservan tal como figuran en el historial.

La aplicación se organiza por contextos funcionales y comparte en `src` el enrutador, el layout de navegación, Pinia e internacionalización. Para reproducir el entorno de integración local se siguen las instrucciones del [README del frontend](https://github.com/Startup-Chapa/frontend-bicigo/blob/develop/README.md), con una API simulada basada en JSON Server. Esta organización facilita las pruebas tempranas, aunque todavía no equivale a un despliegue integral con backend de producción.

**Evidencias de repositorios:**

![Repositorio del informe](./Resources/chapter-images/chapter-5/report.png)

*Figura: repositorio de documentación del proyecto.*

![Repositorio de la Landing Page](./Resources/chapter-images/chapter-5/landing.png)

*Figura: repositorio de la Landing Page.*

![Repositorio del frontend](./Resources/chapter-images/chapter-5/webapp.png)

*Figura: repositorio de la Frontend Web Application.*

![Repositorio de plataforma](./Resources/chapter-images/chapter-5/platform.png)

*Figura: captura histórica asociada a plataforma; confirmar su repositorio y alcance antes de presentarla como backend implementado.*

### 5.1.3. Source Code Style Guide & Conventions

El equipo usa convenciones de organización y nomenclatura para mantener consistente el código de la aplicación Vue. Estas pautas se relacionan con la guía de estilos del Capítulo IV y con la arquitectura modular documentada en la sección 4.6.

| Aspecto | Convención aplicada o recomendada |
|---|---|
| Organización | Agrupar el código por Bounded Context: IAM, Fleet & Station Management, Trip Management, Billing & Subscriptions y Maintenance. |
| Capas | Separar, según el módulo, `domain`, `application`, `infrastructure` y `presentation`; utilizar servicios y componentes compartidos cuando corresponda. |
| Componentes | Utilizar componentes Vue de responsabilidad específica y mantener separadas vistas, rutas y lógica de estado. |
| Estado | Centralizar el estado compartido en Pinia; evitar duplicar sesiones y datos de usuario entre contextos. |
| Navegación | Declarar rutas en Vue Router y usar guardas de interfaz para la experiencia de demostración. La autorización definitiva deberá verificarse en el backend. |
| HTTP | Emplear el cliente HTTP compartido y una variable de entorno (`VITE_BICIGO_API_URL`) para configurar el origen de la API. |
| Internacionalización | Mantener textos en recursos `vue-i18n` y evitar cadenas duplicadas en las vistas. |
| Diseño | Aplicar la paleta, tipografías, espaciado y estados de interacción definidos en 4.1; considerar mobile y desktop. |
| Commits | Utilizar, de preferencia, mensajes descriptivos con prefijos como `feat`, `fix` y `docs` para registrar las modificaciones. |
| Verificación | Compilar con `npm run build` y ejecutar las pruebas documentadas. No atribuir herramientas de *lint* o pruebas automáticas que aún no estén configuradas. |

Las decisiones de implementación deben preservar la trazabilidad con las User Stories, los escenarios **Given–When–Then** del Capítulo III y las pantallas del Capítulo IV. Para considerar una funcionalidad terminada no basta con tener una vista: deben verificarse sus estados, validaciones, navegación y persistencia según el alcance acordado para el Sprint.

### 5.1.4. Software Deployment Configuration

La arquitectura **diseñada** en el Capítulo IV contempla una SPA, una API, mecanismos de persistencia y servicios externos de geolocalización y pagos. Sin embargo, el **incremento del Sprint 2** se ejecuta principalmente como frontend de demostración. Es necesario distinguir ambos niveles para no presentar componentes proyectados como funcionalidades productivas.

| Componente | Implementación comprobable o documentada para Sprint 2 | Alcance |
|---|---|---|
| Frontend SPA | Vue 3, Vite, PrimeVue, Pinia, Vue Router y `vue-i18n` | Interfaz, navegación y estados de los módulos |
| API de desarrollo | JSON Server, ejecutado con `npm run dev:api` | Datos locales de prueba; no es el backend REST productivo |
| Persistencia de Maintenance | `localStorage` en el modo de demostración | Reportes y cambios simulados que persisten en el navegador |
| Autenticación | Sesión simulada y usuarios de prueba | No constituye autenticación ni autorización de backend |
| Hosting del frontend | Firebase Hosting, según las capturas de despliegue del informe | Publicación de los archivos estáticos de Vite |
| Geolocalización y pagos reales | Servicios previstos en la arquitectura | Integración productiva no acreditada en Sprint 2 |

**Flujo de despliegue y ejecución.** En desarrollo, el navegador accede a Vite en `127.0.0.1:5173` y el frontend consume datos de JSON Server en `127.0.0.1:3000/api/v1`, además de determinados estados locales. En despliegue, Vite genera el directorio `dist`, que es publicado por Firebase Hosting. La publicación de los archivos estáticos no significa por sí sola que la API local quede expuesta en Internet.

```plantuml
@startuml
title BiciGO - Despliegue del incremento frontend (Sprint 2)
actor "Usuario" as User
node "Navegador" {
  artifact "SPA Vue 3 + Vite\n(Vue Router, Pinia, i18n)" as SPA
  database "localStorage\n(demo Maintenance)" as Local
}
cloud "Firebase Hosting\n(archivos estaticos dist/)" as Firebase
node "Entorno de desarrollo" {
  component "JSON Server\nAPI simulada /api/v1" as MockAPI
  database "server/db.json\nDatos de prueba" as MockDB
}
cloud "API + servicios externos\n(previstos para siguiente iteracion)" as Future
User --> SPA : Interfaz web
Firebase --> SPA : Entrega de archivos estaticos
SPA --> MockAPI : HTTP local (desarrollo)
MockAPI --> MockDB
SPA --> Local : Persistencia demo
SPA ..> Future : Integracion futura
@enduml
```

*Figura: vista lógica de la configuración de despliegue del Sprint 2. El nodo de API simulada es local y el nodo de servicios productivos es proyectado, no desplegado.*

**Consideración de seguridad y operación.** La SPA utiliza navegación basada en fragmentos (`createWebHashHistory`), que permite resolver rutas del cliente sin configurar reglas de reescritura en Firebase. Los permisos de vistas o roles simulados no reemplazan controles de autorización en los Web Services definitivos. Los flujos de cobro y de ubicación en tiempo real se dejarán pendientes hasta contar con servicios integrados y pruebas específicas.

## 5.2. Landing Page, Services & Applications Implementation

### 5.2.1. Sprint 1

El Sprint 1 corresponde a la primera entrega del proyecto (AV1 – Sprint Review) y tiene como alcance la implementación y el despliegue de la primera versión del **Landing Page** de BiciGO. El Landing Page presenta el modelo de negocio y el propósito de la plataforma a los visitantes de los segmentos objetivo (ciudadanos urbanos que realizan trayectos cortos e instituciones que desean promover el uso de la bicicleta), y es el punto de entrada hacia las aplicaciones. Los Web Services y las Frontend Web Applications se implementarán en los siguientes Sprints, según el cronograma de entregas del curso.

#### 5.2.1.1. Sprint Planning 1

La planificación del Sprint 1 organiza la primera versión de la Landing Page de biciGO, tomando como insumos el Lean UX Canvas, los segmentos objetivo, las User Personas, el wireframe, el mock-up y la guía de estilos. Se consideran las seis historias de usuario y la historia técnica identificadas en el Sprint Backlog 1.

**Base de planificación:** la fecha y la hora se proponen para completar el registro; los story points y la velocidad planificada son estimaciones de referencia, no mediciones históricas.

**Sprint Planning Background**

| Campo | Sprint 1 |
|---|---|
| Sprint # | Sprint 1 |
| Date | 07/09/2026 (propuesta) |
| Time | 20:00–21:00 (hora de Lima; propuesta) |
| Location | Reunión virtual |
| Prepared By | Aguirre Ramos, Eduardo Manuel |
| Attendees (to planning meeting) | Aguirre Ramos, Eduardo Manuel / Armestar Felipa, Adrian Andres / Ayllon Pauccar, Juan David / Franco del Carpio, José María / Velasquez Velasquez, Rodrigo |
| Sprint 0 Review Summary | No aplica: este es el primer Sprint. Como antecedentes se consideran los artefactos de investigación, requisitos y diseño de los Capítulos I al IV, además de los repositorios del informe y de la Landing Page. |
| Sprint 0 Retrospective Summary | No aplica: no hubo un Sprint anterior. Como acuerdos iniciales de planificación se propone distribuir tareas por sección, registrar avances en Trello y revisar los cambios antes de integrarlos. |

**Sprint Goal & User Stories**

| Campo | Sprint 1 |
|---|---|
| Sprint 1 Goal | *Our focus is on publishing the first deployed version of the BiciGO Landing Page, available in English and Latin American Spanish and responsive on mobile and desktop screens.*<br>*We believe it delivers a clear understanding of the service (mission, vision, benefits and how it works) and a direct way to get in touch with the team to urban citizens who make short trips and to institutions interested in promoting cycling.*<br>*This will be confirmed when the Landing Page is publicly reachable at its GitHub Pages URL, every section can be read on a 390 px and on a 1440 px wide screen without horizontal scrolling, and a visitor can switch the whole interface between English and Spanish.* |
| Selected User Stories | US-LP01: navegación y presentación principal; US-LP02: funcionamiento del servicio; US-LP03: beneficios y métricas; US-LP04: tarifas y planes; US-LP05: preguntas frecuentes; US-LP06: contacto y validación del formulario. |
| Selected Technical Stories | TS-LP01: configuración del repositorio, despliegue en GitHub Pages y revisión responsive. |
| Sprint 1 Velocity | 16 story points por sprint (velocidad planificada inicial, sin historial previo). |
| Sum of Story Points | 16 story points: 13 de historias de usuario y 3 de la historia técnica. |
| Task Estimation | 38 horas, correspondientes a las 16 microtareas del Sprint Backlog 1. |

**Distribución estimada de Story Points**

| Story Id | Story Title | Story Points |
|---|---|---:|
| US-LP01 | Navegación y presentación principal (Navbar & Hero) | 3 |
| US-LP02 | Explicación del funcionamiento del servicio | 2 |
| US-LP03 | Presentación de beneficios y métricas | 2 |
| US-LP04 | Comparación de tarifas y planes | 2 |
| US-LP05 | Consulta de preguntas frecuentes | 2 |
| US-LP06 | Formulario de contacto y validación | 2 |
| TS-LP01 | Despliegue y revisión responsive | 3 |
| **Total** | **6 User Stories y 1 Technical Story** | **16** |

Los puntos se asignan a cada historia una sola vez; sus microtareas conservan las estimaciones en horas del backlog. La velocidad real requiere validar las historias terminadas frente a sus criterios de aceptación. La internacionalización se mantiene como condición transversal del Sprint Goal y requiere reflejar su trabajo en las tareas de las historias correspondientes, ya que el backlog disponible no la desglosa como tarea independiente.

#### 5.2.1.2. Aspect Leaders and Collaborators

Para el Sprint 1 se identificaron seis aspectos dentro del alcance. La Leadership-and-Collaboration Matrix (LACX) indica, para cada aspecto, quién lidera y quiénes colaboran. La organización de líderes y colaboradores guarda relación con la selección de tareas del Sprint Backlog 1.

- **Landing Page Structure & Content (HTML):** estructura semántica de las secciones y redacción de los contenidos.
- **Visual Style & Responsive Design (CSS):** aplicación de la guía de estilos del Capítulo IV y diseño adaptable a móvil y escritorio.
- **Internationalization (i18n):** diccionarios en inglés y español, y selector de idioma.
- **Deployment (GitHub Pages):** publicación del Landing Page en un sitio público.
- **Landing Page UI Design (Figma):** wireframe y mock-up que guían la implementación.
- **Report Documentation:** redacción de las secciones del Capítulo V correspondientes al Sprint.

| Team Member (Last Name, First Name) | GitHub Username | Structure & Content (HTML) | Visual Style & Responsive (CSS) | Internationalization (i18n) | Deployment (GitHub Pages) | UI Design (Figma) | Report Documentation |
|---|---|:---:|:---:|:---:|:---:|:---:|:---:|
| Aguirre Ramos, Eduardo Manuel | TheEngineEdu | C | C | C | C | C | L |
| Armestar Felipa, Adrian Andres | Adrian5102 | L | L | L | L | L | C |
| Ayllon Pauccar, Juan David | JuanDPAUC | C | C | C | C | C | C |
| Franco del Carpio, José María | VoltTrd [POR CONFIRMAR] | C | C | C | C | C | C |
| Velasquez Velasquez, Rodrigo | Rodrigov233 | C | C | C | C | C | C |

*L = Leader, C = Collaborator.*

La asignación de líderes y colaboradores se definió a partir de la participación de cada integrante en los repositorios `Landing-Page` y `project-report`.

#### 5.2.1.3. Sprint Backlog 1

El objetivo principal del Sprint 1 es publicar la primera versión del Landing Page de BiciGO, en inglés y español y con diseño responsive, para presentar el modelo de negocio a los visitantes. El Sprint Backlog 1 se gestiona en un tablero de Trello con las columnas To-do, In-Process, To-Review y Done.

Las tareas se agrupan bajo seis historias específicas de la Landing Page (US-LP01 a US-LP06) y una historia técnica (TS-LP01), diferenciadas de las historias de la aplicación web. El backlog disponible contiene 16 microtareas de 2 a 3 horas cada una, con una estimación total de **38 horas**. La estimación de referencia de sus historias suma **16 story points**, como se detalla en Sprint Planning 1.

**Trello del AV1**

![imagen trello](./Resources/chapter5/trello.png)

[https://trello.com/invite/b/6aac96a6ce176e2f9d496d31/ATTI96186798f26dde57c47e51ca96f0fff04FDD51DF/sprint-web-1](https://trello.com/invite/b/6aac96a6ce176e2f9d496d31/ATTI96186798f26dde57c47e51ca96f0fff04FDD51DF/sprint-web-1)

**Sprint #: Sprint 1**

| Epic / Story ID | Task ID | Título de la Microtarea | Descripción y Alcance Técnico | Estimación (Horas) | Asignado a | Estado |
| :--- | :--- | :--- | :--- | :---: | :--- | :---: |
| **US-LP01** | T-01.1 | `[US-LP01]` `[UI/UX]` Navbar & Hero Design | Diseñar el componente del Navbar con el isotipo biciGO y la sección Hero en Figma aplicando contraste de marca. | 2 h | Ayllon Pauccar, Juan David | Done |
| **US-LP01** | T-01.2 | `[US-LP01]` `[FRONT]` Navbar responsive layout | Maquetar el menú superior responsive con el logo de biciGO, enlaces de navegación y menú hamburguesa para móviles. | 3 h | Armestar Felipa, Adrian Andres | Done |
| **US-LP01** | T-01.3 | `[US-LP01]` `[FRONT]` Hero section CTA & Overlay | Construir el Hero Section con el título H1, subtítulo, imagen de fondo con overlay oscuro (#263238) y botones principales de acción (CTA). | 3 h | Armestar Felipa, Adrian Andres | Done |
| **US-LP02** | T-02.1 | `[US-LP02]` `[UI/UX]` "How it Works" Icons | Seleccionar y optimizar los 4 íconos SVG representativos del proceso (*Busca, Escanea, Muévete, Devuelve*). | 2 h | Velasquez Velasquez, Rodrigo | Done |
| **US-LP02** | T-02.2 | `[US-LP02]` `[FRONT]` "How it Works" 4-step grid | Maquetar el grid responsive de 4 pasos secuenciales aplicando la escala de espaciado `space-md` (16px) y textos explicativos. | 3 h | Ayllon Pauccar, Juan David | Done |
| **US-LP03** | T-03.1 | `[US-LP03]` `[FRONT]` Benefits cards layout | Maquetar las tarjetas de beneficios (Ahorro, Ecología, Rapidez) con bordes redondeados de 8px y sombras suaves. | 3 h | Velasquez Velasquez, Rodrigo | Done |
| **US-LP03** | T-03.2 | `[US-LP03]` `[FRONT]` Key metrics counter bar | Maquetar la barra de métricas destacadas (100+ estaciones, 500+ bicis, 100% ecofriendly) con números en Verde biciGO (#7BC617). | 2 h | Velasquez Velasquez, Rodrigo | Done |
| **US-LP04** | T-04.1 | `[US-LP04]` `[FRONT]` Pricing cards comparison | Maquetar la comparativa de tarifas (Pago por uso vs. Suscripción Pro) con la tabla de precios transparente. | 3 h | Franco Del Carpio, José María | Done |
| **US-LP04** | T-04.2 | `[US-LP04]` `[FRONT]` Pro plan highlight & CTA | Aplicar el estilo destacado (Fondo #263238, tag 'Recomendado' y botón #7BC617) a la tarjeta de suscripción mensual. | 2 h | Franco Del Carpio, José María | Done |
| **US-LP05** | T-05.1 | `[US-LP05]` `[FRONT]` FAQ accordion HTML/CSS | Maquetar la estructura de acordeón para las preguntas frecuentes sobre zonas de cobertura y métodos de pago. | 2 h | Armestar Felipa, Adrian Andres | Done |
| **US-LP05** | T-05.2 | `[US-LP05]` `[JS]` Accessible accordion logic | Implementar la interacción JavaScript para abrir/cerrar preguntas con soporte de teclado y atributos ARIA de accesibilidad. | 2 h | Armestar Felipa, Adrian Andres | Done |
| **US-LP06** | T-06.1 | `[US-LP06]` `[FRONT]` Contact form UI | Maquetar los campos del formulario (Nombre, Correo, Mensaje) asegurando una altura táctil mínima de 44px. | 2 h | Armestar Felipa, Adrian Andres | Done |
| **US-LP06** | T-06.2 | `[US-LP06]` `[JS]` Form validation & feedback | Implementar la validación básica de campos obligatorios e indicador de confirmación de envío en verde (#2E8B57). | 2 h | Armestar Felipa, Adrian Andres | Done |
| **TS-LP01** | T-07.1 | `[TS-LP01]` `[DEVOPS]` Git repo & GitHub Pages setup | Crear el repositorio en GitHub, configurar la rama `main` y habilitar el despliegue automático en GitHub Pages. | 2 h | Armestar Felipa, Adrian Andres | Done |
| **TS-LP01** | T-07.2 | `[TS-LP01]` `[DEVOPS]` Public URL & Domain check | Verificar el despliegue correcto de la URL pública (`https://startup-chapa.github.io/Landing-Page/`) y ruta de assets. | 2 h | Armestar Felipa, Adrian Andres | Done |
| **TS-LP01** | T-11.1 | `[TS-LP01]` `[QA]` Cross-device responsive test | Probar la adaptabilidad en resoluciones móviles (393x852px), tablets y monitores de escritorio (1200px max-width). | 3 h | Aguirre Ramos, Eduardo Manuel | Done |

#### 5.2.1.4. Development Evidence for Sprint Review

Durante el Sprint 1 se implementó la primera versión del Landing Page en el repositorio `Startup-Chapa/Landing-Page`: la estructura HTML, los estilos CSS responsive, los diccionarios de traducción en inglés y español y las imágenes de las secciones. En paralelo, en el repositorio `Startup-Chapa/project-report` se documentaron el wireframe y el mock-up del Landing Page (Capítulo IV) y la gestión del código fuente (Capítulo V), que sirvieron de base para la implementación. Los commits siguen la convención Conventional Commits descrita en la sección 5.1.2.

| Commit | Autor | Email | Fecha | Mensaje |
|---|---|---|---|---|
| `ef59cb5` | Adrian5102 | u202410084@upc.edu.pe | 2026-09-14 | feat: add info for BiciGo |
| `615a806` | Adrian5102 | u202410084@upc.edu.pe | 2026-09-14 | feat: add first version of Landing Page |
| `aeca1f3` | Adrian5102 | u202410084@upc.edu.pe | 2026-09-14 | feat: add index & css files |
| `ef218d4` | Eduardo Manuel Aguirre | enginedujob@gmail.com | 2026-08-30 | Initial commit |

![github-landing-commits](./Resources/chapter5/github-commits.png)

*Figura: historial de commits del repositorio Landing-Page en GitHub.*

#### 5.2.1.5. Execution Evidence for Sprint Review

El Landing Page de BiciGO está publicado y accesible en https://startup-chapa.github.io/Landing-Page/. La primera versión incluye las siguientes vistas:

- **Barra de navegación:** logotipo, enlaces a Home, About Us, Benefits, How does it work?, FAQs y Contact, selector de idioma EN/ES y botones Login y Sign Up.
- **Hero:** lema de la marca "MOVE | LIVE | LIMA", mensaje principal y botón de llamado a la acción *Get Started*.
- **Misión y visión:** textos de la propuesta de valor con fotografías de movilidad en Lima.
- **Beneficios:** seis tarjetas con los beneficios del servicio.
- **How does it work?:** explicación del recorrido del usuario, desde encontrar una bicicleta hasta finalizar el viaje.
- **Contacto:** formulario con nombre, teléfono, correo, tipo de usuario (estudiante, trabajador o ciudadano) y mensaje.
- **FAQs:** cinco preguntas frecuentes en formato acordeón, operables con el teclado.
- **Footer:** logotipo, íconos de redes sociales y aviso de derechos.

La interfaz está disponible en inglés (idioma por defecto) y en español latinoamericano, y se adapta a móvil y escritorio. En la verificación realizada, el ancho de la página coincide con el ancho de la pantalla tanto en 390 px como en 1440 px, es decir, sin desplazamiento horizontal.

**Vista de escritorio (1440 px)**

![landing-hero-desktop](./Resources/chapter5/hero-secction.png)

**Página completa en escritorio (1440 px)**

![landing-full-desktop](./Resources/chapter5/captura-completa-web.png)

**Página completa en móvil (390 px)**

![landing-full-mobile](./Resources/chapter5/captura-completa-mobile.png)

#### 5.2.1.6. Services Documentation Evidence for Sprint Review

En el Sprint 1 no se implementaron Web Services. El alcance de este Sprint se limitó al Landing Page, tal como establece la primera entrega del trabajo final, por lo que no existen endpoints documentados con OpenAPI ni commits de documentación de API en este Sprint.

Los endpoints que se implementarán en los siguientes Sprints están especificados como Technical Stories en el Capítulo III (por ejemplo, `GET /api/coverage` para la consulta de zonas de cobertura). Su documentación con OpenAPI (Swagger) se presentará en esta sección a partir del Sprint en que se implementen los Web Services.

#### 5.2.1.7. Software Deployment Evidence for Sprint Review

En el Sprint 1 se desplegó el Landing Page en **GitHub Pages**, directamente desde el repositorio `Startup-Chapa/Landing-Page`. Como el Landing Page es un sitio estático (HTML, CSS, JavaScript y archivos JSON), no requiere una etapa de compilación, y la publicación se realiza a partir del contenido de la rama `main`.

Los pasos realizados fueron los siguientes:

1. Se creó el repositorio `Landing-Page` en la organización Startup-Chapa de GitHub.
2. Se subieron a la rama `main` el archivo `index.html`, la hoja de estilos `style.css`, la carpeta `assets/images` y los diccionarios de la carpeta `i18n`.
3. En la configuración del repositorio (*Settings > Pages*) se habilitó GitHub Pages con la publicación desde la rama `main`.
4. GitHub ejecutó el flujo `pages build and deployment`, que finalizó correctamente el 14/09/2026 a las 23:42 (GMT-5), con una duración de 38 segundos, para el commit `ef59cb5`.
5. Se verificó el acceso público al sitio en https://startup-chapa.github.io/Landing-Page/.

| Producto | Plataforma | URL | Estado |
|---|---|---|---|
| Landing Page | GitHub Pages | https://startup-chapa.github.io/Landing-Page/ | Desplegado |
| Web Applications | Por definir (sección 5.1.4) | Sin desplegar en el Sprint 1 | No incluido en el alcance |
| Web Services | Por definir (sección 5.1.4) | Sin desplegar en el Sprint 1 | No incluido en el alcance |

![github-landing-actions](./Resources/chapter5/github-actions.png)

*Figura: ejecución del flujo pages build and deployment en GitHub Actions.*

#### 5.2.1.8. Team Collaboration Insights during Sprint

Las actividades del Sprint 1 se organizaron con el flujo GitFlow descrito en la sección 5.1.2: el trabajo del informe se realizó en ramas `feature/*` creadas a partir de `develop` e integradas mediante Pull Requests. La implementación del Landing Page se realizó en el repositorio `Landing-Page`. La siguiente tabla resume los commits de cada integrante, sin contar los commits de fusión (*merge*), en la rama `develop` al cierre de este informe.

| Integrante | Usuario de GitHub | Commits en Landing-Page | Commits en project-report |
|---|---|:---:|:---:|
| Aguirre Ramos, Eduardo Manuel | TheEngineEdu | 1 | 9 |
| Armestar Felipa, Adrian Andres | Adrian5102 | 3 | 18 |
| Ayllon Pauccar, Juan David | JuanDPAUC | 0 | 7 |
| Franco del Carpio, José María | VoltTrd | 0 | 1 |
| Velasquez Velasquez, Rodrigo | Rodrigov233 | 0 | 4 |

### 5.2.2. Sprint 2

El Sprint 2 corresponde al primer incremento integrado de la **Frontend Web Application de BiciGO**. Como referencia se utilizan el Product Backlog y los escenarios de aceptación actualizados del Capítulo III, la guía de estilos, los wireframes y mock-ups del Capítulo IV y las evidencias de código disponibles en el repositorio `Startup-Chapa/frontend-bicigo`.

El alcance real debe documentarse distinguiendo entre **interfaz integrada**, **flujo simulado** y **funcionalidad productiva**. Las pruebas locales con JSON Server o `localStorage` no demuestran por sí mismas una integración con el backend real.

#### 5.2.2.1. Sprint Planning 2

**Sprint Planning Background**

| Campo | Registro de Sprint 2 |
|---|---|
| Sprint # | Sprint 2 |
| Fecha de planificación | 28/09/2026, **fecha propuesta en el registro anterior; pendiente de confirmar** |
| Hora | 20:00–21:00, hora de Lima, **referencia propuesta** |
| Modalidad | Reunión virtual |
| Preparado por | Chapa Technologies / Startup-Chapa |
| Participantes | Aguirre Ramos, Eduardo Manuel; Armestar Felipa, Adrian Andres; Ayllon Pauccar, Juan David; Franco del Carpio, José María; Velasquez Velasquez, Rodrigo |
| Sprint 1 Review Summary | Se elaboró y publicó la primera versión de la Landing Page, con estructura responsive e internacionalización. |
| Sprint 1 Retrospective Summary | Se propuso mantener la asignación por responsables, actualizar el tablero y documentar mejor los commits y las evidencias individuales. Los acuerdos específicos deben validarse con el acta o tablero. |

**Sprint Goal & User Stories**

*Our focus is on integrating the first navigable version of the BiciGO Frontend Web Application using the user flows and interface guidelines defined in Chapters III and IV. We believe it delivers a coherent demonstration of account access, bicycle and station consultation, trip information, subscription plans and incident management to prospective users and operators. This will be confirmed when the integrated SPA can be executed, its main routes and validations can be demonstrated, and the team clearly documents which interactions use mock data or local persistence and which requirements remain pending.*

Las **15 User Stories** consignadas en el backlog anterior se mantienen como **selección originalmente planificada**, hasta que el equipo confirme formalmente si hubo cambios de alcance. La disponibilidad de un módulo integrado no demuestra automáticamente el cumplimiento de todos sus escenarios Given–When–Then.

| Indicador | Valor y criterio |
|---|---|
| Selected User Stories | IAM: US-01, US-02, US-03; Fleet: US-07, US-08, US-09; Trip: US-11, US-13, US-15; Billing: US-16, US-17, US-19; Maintenance: US-26, US-29, US-33. |
| Tareas transversales | T2-16 integración; T2-17 pruebas de interfaces y responsive; T2-18 publicación del frontend. |
| Suma de SP de la selección original con la línea base actualizada | **56 SP**, recalculados según las estimaciones actuales de **3.3 Product Backlog**; reemplazan la suma anterior de 30 SP, sin afirmar que sean velocidad real. |
| Estimación de tareas | **70 h**, correspondientes a 18 tareas; las horas son esfuerzo estimado y no una conversión de SP. |
| Velocidad real | **No determinada**: requiere el resultado de cada historia frente a sus criterios de aceptación y Definition of Done. |
| Alcance técnico | SPA Vue con integración de módulos y servicios de demostración. La API REST de producción permanece en una iteración posterior. |

**Correspondencia de estimaciones con el Capítulo III**

| Bounded Context | Story ID | Historia | SP del Product Backlog |
|---|---|---|---:|
| IAM | US-01 | Registro de usuario | 3 |
| IAM | US-02 | Inicio de sesión | 3 |
| IAM | US-03 | Recuperación de contraseña | 3 |
| Fleet & Station Management | US-07 | Visualización de bicicletas cercanas | 5 |
| Fleet & Station Management | US-08 | Consulta de información de bicicleta | 3 |
| Fleet & Station Management | US-09 | Búsqueda de bicicletas por zona | 3 |
| Trip Management | US-11 | Inicio de alquiler | 5 |
| Trip Management | US-13 | Consulta del viaje activo | 3 |
| Trip Management | US-15 | Finalización de alquiler | 5 |
| Billing & Subscriptions | US-16 | Registro de método de pago | 5 |
| Billing & Subscriptions | US-17 | Consulta de tarifa | 2 |
| Billing & Subscriptions | US-19 | Suscripción a plan mensual | 5 |
| Maintenance | US-26 | Reporte de bicicleta dañada | 3 |
| Maintenance | US-29 | Seguimiento de incidencias | 3 |
| Maintenance | US-33 | Gestión de incidencias de bicicletas | 5 |
| **Total** | **15 US** | **Selección originalmente planificada** | **56** |

**Observación de alcance.** Los módulos implementados también contienen vistas relacionadas con otras historias del Capítulo III, como consulta de perfil (US-21), historial de viajes (US-23), detalle de viaje (US-24) y administración de flota (US-31/US-32). Estas funcionalidades pueden mencionarse como evidencia adicional, **pero no se suman retroactivamente** a la velocidad del Sprint 2 sin una actualización aprobada del Sprint Backlog.

#### 5.2.2.2. Aspect Leaders and Collaborators

Para el Sprint 2 se organizó el desarrollo en cinco Bounded Contexts. Esta división facilita la identificación de responsables de implementación y permite integrar funcionalidades sobre una estructura de navegación compartida. Los Epics del Capítulo III no deben confundirse con los Bounded Contexts: un mismo contexto puede implementar historias pertenecientes a más de un Epic, como sucede con Maintenance (EP-06 y EP-07).

| Team Member | GitHub Username | IAM | Trip Management | Billing & Subscriptions | Fleet & Station Management | Maintenance |
|---|---|:---:|:---:|:---:|:---:|:---:|
| Armestar Felipa, Adrian Andres | Adrian5102 | L | C | C | C | C |
| Franco del Carpio, José María | VoltTrd | C | L | C | C | C |
| Ayllon Pauccar, Juan David | JuanDPAUC | C | C | L | C | C |
| Aguirre Ramos, Eduardo Manuel | TheEngineEdu | C | C | C | L | C |
| Velasquez Velasquez, Rodrigo | Rodrigov233 | C | C | C | C | L |

*L = Leader; C = Collaborator. Esta matriz refleja la asignación documentada y no constituye por sí misma un conteo de commits ni una validación del trabajo completado.*

#### 5.2.2.3. Sprint Backlog 2

El backlog organiza las tareas inicialmente asociadas a las 15 historias seleccionadas, más tres actividades transversales. El tablero de seguimiento se encuentra en [Trello — Sprint 2 Web Application](https://trello.com/invite/b/6ac5b1a35529b83a03b51a0b/ATTI93c275e0a7f8461177850a9425f1680415930B03/sprint-2-web-application).

![Tablero Trello de Sprint 2](./Resources/chapter5/trello2.png)

*Figura: captura del tablero de Sprint 2. Sus estados deben contrastarse con la versión actual del tablero.*

La columna **Revisión documental** de la tabla siguiente refleja lo que puede inferirse de la documentación del repositorio. **No reemplaza el estado oficial en Trello** ni equivale a la aceptación formal de cada User Story.

| Story ID | Task ID | Microtarea | Estimación | Responsable | Revisión documental |
|---|---|---|---:|---|---|
| US-01 | T2-01 | Implement Register View | 3 h | Adrian Armestar | Vista de registro documentada; flujo local de demostración |
| US-02 | T2-02 | Implement Login View | 3 h | Adrian Armestar | Vista y sesión simulada documentadas |
| US-03 | T2-03 | Implement Password Recovery | 3 h | Adrian Armestar | Recuperación de prueba; envío real no acreditado |
| US-07 | T2-04 | Implement Bicycle Map | 5 h | Eduardo Aguirre | Falta evidenciar mapa con bicicletas cercanas al usuario |
| US-08 | T2-05 | Implement Bicycle Detail | 3 h | Eduardo Aguirre | Fleet consulta bicicletas; validar detalle y criterios de US-08 |
| US-09 | T2-06 | Implement Zone Search | 3 h | Eduardo Aguirre | Falta evidenciar búsqueda por zona de usuario |
| US-11 | T2-07 | Implement Start Trip | 5 h | José María Franco | No se acredita inicio de alquiler; Trip documenta historial |
| US-13 | T2-08 | Implement Active Trip | 5 h | José María Franco | No se acredita vista o estado de viaje activo |
| US-15 | T2-09 | Implement Finish Trip | 5 h | José María Franco | No se acredita finalización de alquiler |
| US-16 | T2-10 | Implement Payment Method | 3 h | Juan David Ayllon | No se acredita registro de un método de pago real o simulado |
| US-17 | T2-11 | Implement Pricing View | 3 h | Juan David Ayllon | Existen vistas de planes; confirmar tarifa por alquiler |
| US-19 | T2-12 | Implement Subscription View | 5 h | Juan David Ayllon | Selección y compra simulada de plan documentadas |
| US-26 | T2-13 | Implement Damage Report | 3 h | Rodrigo Velasquez | Reporte de Maintenance en modo demo local |
| US-29 | T2-14 | Implement Incident Tracking | 5 h | Rodrigo Velasquez | Consulta de reportes demo; comprobar estados de incidencias |
| US-33 | T2-15 | Implement Incident Management | 5 h | Rodrigo Velasquez | Gestión local para rol de operador/administrador simulado |
| Transversal | T2-16 | Integrate Frontend | 5 h | Equipo completo | Integración modular documentada en `develop` |
| Transversal | T2-17 | Responsive Review | 3 h | Equipo completo | Pruebas de 390, 768 y 1440 px descritas en README de Maintenance; adjuntar resultados de ejecución |
| Transversal | T2-18 | Deploy Frontend | 3 h | Equipo completo | Capturas de publicación Firebase incluidas; comprobar la versión accesible |
| **Total** | **18 tareas** | | **70 h** | | **Pendiente de cierre validado** |

**Criterio para el cierre.** Cada historia solo debe pasar a `Done` cuando el equipo pueda demostrar todos los escenarios comprometidos para ese incremento o haya aprobado formalmente un alcance reducido. Los estados `To-do`, `In-Process`, `To-Review` y `Done` deben actualizarse desde el tablero real; aquí no se asignan estados inventados. Un mockup del Capítulo IV sirve como referencia visual, pero no equivale a una captura de ejecución de la aplicación.

#### 5.2.2.4. Development Evidence for Sprint Review

El desarrollo del Sprint 2 se documenta en el repositorio [Startup-Chapa/frontend-bicigo](https://github.com/Startup-Chapa/frontend-bicigo). La aplicación integrada contiene rutas y componentes de IAM, Trip Management, Billing & Subscriptions, Fleet & Station Management y Maintenance, además de un router, layout, cliente HTTP y estado compartidos.

| Bounded Context | Rama de desarrollo | Evidencia funcional identificada | Limitación relevante |
|---|---|---|---|
| IAM | `feature/iam` | Login, registro, perfil, sesión y recuperación de prueba | Autenticación y recuperación simuladas |
| Trip Management | `feature/trip-management` | Consulta del historial de viajes y acceso al reporte de incidencias desde un viaje | Inicio, viaje activo y cierre de alquiler no acreditados por el README |
| Billing & Subscriptions | `feature/billing-subscriptions` | Planes, selección y compra simulada de suscripción | No existe evidencia de pasarela de pagos productiva |
| Fleet & Station Management | `feature/fleet-station-management` | Gestión y consulta de estaciones y bicicletas mediante API local | No se demuestra por sí sola la geolocalización de bicicletas cercanas |
| Maintenance | `feature/maintenance` | Reportes, gestión administrativa y transiciones de estado de bicicleta en demo | Uso de `localStorage` sin contratos API productivos confirmados |

El archivo `src/router.js` usa `createWebHashHistory` para integrar la navegación y las rutas de los contextos; `src/main.js` registra Pinia, Vue Router, `vue-i18n` y PrimeVue. El README explica que parte de la integración se realizó por selección y combinación de archivos, de modo que las estadísticas de Pull Requests no representan toda la integración efectuada.

**Fuente de verificación técnica:** [README de integración](https://github.com/Startup-Chapa/frontend-bicigo/blob/develop/README.md), [Router de la aplicación](https://github.com/Startup-Chapa/frontend-bicigo/blob/develop/src/router.js), [README de Maintenance](https://github.com/Startup-Chapa/frontend-bicigo/blob/develop/src/maintenance/README.md).

**Historial aportado para la revisión inicial (instantánea de `develop`)**

La tabla conserva los mensajes y fechas registrados previamente en el informe. Las fechas de esta instantánea pertenecen al período **27/09/2026–07/10/2026**; no sustituyen un historial completo ni representan necesariamente el estado del repositorio en la última fecha de edición del informe. Como el extracto proporcionado carece de códigos SHA y cuerpos, estos datos permanecen identificados como no proporcionados, sin rellenarlos arbitrariamente.

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed on | GitHub User |
|---|---|---|---|---|---|---|
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | fix: modify db.json | No proporcionado | 07/10/2026 | TheEngineEdu |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | Merge branch 'develop' of https://github.com/Startup-Chapa/frontend-bicigo into develop | No proporcionado | 07/10/2026 | TheEngineEdu |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | Refactor JSON structure in db.json | No proporcionado | 07/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | Change localStorage key from 'bicigo_user' to 'users' | No proporcionado | 07/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | Merge branch 'develop' of https://github.com/Startup-Chapa/frontend-bicigo into develop | No proporcionado | 07/10/2026 | TheEngineEdu |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | db.json | No proporcionado | 06/10/2026 | VoltTrd |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat: integrate BiciGO frontend modules | No proporcionado | 06/10/2026 | Rodrigov233 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat:add configuration to the page | No proporcionado | 06/10/2026 | TheEngineEdu |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | Merge pull request #2 from Startup-Chapa/feature/iam | No proporcionado | 06/10/2026 | TheEngineEdu |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): add forgot password view | No proporcionado | 02/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): add final details for i18n | No proporcionado | 02/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): fixed great part of iam | No proporcionado | 02/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): trying to fix everything pls maybe hopefully | No proporcionado | 02/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): update layout | No proporcionado | 02/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | fix iam requirements | No proporcionado | 02/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): add iam routes | No proporcionado | 02/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): add authentication section component | No proporcionado | 02/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): add reset password view | No proporcionado | 02/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): add forgot password view | No proporcionado | 02/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): add register view | No proporcionado | 02/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): add login view | No proporcionado | 02/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): add pinia start | No proporcionado | 02/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): add i18n start | No proporcionado | 02/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): add iam store | No proporcionado | 02/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): add mock api for iam | No proporcionado | 02/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): add user assembler | No proporcionado | 01/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): add iam interceptor | No proporcionado | 01/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): add iam storage | No proporcionado | 01/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat(iam): add user entity | No proporcionado | 01/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat: add base entity | No proporcionado | 01/10/2026 | Adrian5102 |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat:add shared context to src | No proporcionado | 30/09/2026 | TheEngineEdu |
| Startup-Chapa/frontend-bicigo | `develop` | No proporcionado | feat:initial commit | No proporcionado | 27/09/2026 | TheEngineEdu |

El extracto original tiene **32 entradas**, incluidas **3 entradas de fusión**. La confirmación exacta de autoría, SHA y fecha de cada commit requiere consultar el historial completo, filtrando por el rango de Sprint y diferenciando commits propios de merges.

**GitHub Pulse: actividad del 30/09/2026 al 07/10/2026 (captura histórica)**

| Indicador de la captura | Valor |
|---|---:|
| Autores activos | 5 |
| Commits en todas las ramas | 62 |
| Commits en `main` | 2 |
| Pull Requests fusionados | 2 |
| Pull Requests abiertos | 0 |
| Archivos modificados en `main` | 14 |
| Líneas añadidas en `main` | 632 |
| Líneas eliminadas en `main` | 0 |

![GitHub Pulse - actividad de Sprint 2](./Resources/chapter5/pulse.png)

*Figura: GitHub Pulse del período indicado. Incluye los Pull Requests #1 (Trip Management) y #2 (IAM) fusionados, según la captura del informe.*

Estos datos **no deben presentarse como resultado final de todo el Sprint 2** si el equipo continuó trabajando después del 07/10/2026. Es necesario adjuntar, al cierre, una captura con el rango completo acordado para la evaluación.

#### 5.2.2.5. Execution Evidence for Sprint Review

Las evidencias de ejecución deben mostrar pantallas **reales de la SPA** y relacionarse con las User Stories y mockups de los Capítulos III y IV. Se conserva la estructura de archivos de imágenes existente, pero se corrige la asociación de contextos: la pantalla de perfil pertenece a gestión de cuenta y la pantalla de suscripciones no corresponde a Trip Management.

**Identity & Access Management (IAM)**

![Inicio de sesión](./Resources/chapter5/evidencia-bicigo/login-evidencia.png)

*Figura: vista de login (US-02). Comparar las validaciones de credenciales con los escenarios del Capítulo III; la autenticación actual es de demostración.*

![Registro de usuario](./Resources/chapter5/evidencia-bicigo/signup-evidencia.png)

*Figura: vista de registro (US-01); verificar campos obligatorios y prevención de duplicados con datos de prueba.*

![Perfil del usuario](./Resources/chapter5/evidencia-bicigo/profile.png)

*Figura: perfil (US-21, funcionalidad adicional a las 15 historias originalmente seleccionadas).* 

**Fleet & Station Management**

![Dashboard](./Resources/chapter5/evidencia-bicigo/dashboard.png)

*Figura: dashboard integrado; sirve como evidencia de navegación, pero no prueba geolocalización o estados en tiempo real.*

![Consulta de bicicletas](./Resources/chapter5/evidencia-bicigo/bycicles.png)

*Figura: vista de bicicletas. Contrastar sus campos con US-08 y añadir una captura específica si existe un mapa para US-07 o una búsqueda para US-09.*

**Trip Management**

El repositorio documenta una vista de historial y la navegación a reportes desde un viaje. **En el material adjunto no aparece una captura inequívoca** del inicio de alquiler (US-11), del viaje activo (US-13) o de su finalización (US-15). Antes de marcarlas `Done`, se requieren evidencias de esas pantallas o una replanificación documentada. Para el historial, puede añadirse una captura de `/#/app/trips` (US-23), indicando que es trabajo adicional al alcance inicial.

**Billing & Subscriptions**

![Planes y suscripciones](./Resources/chapter5/evidencia-bicigo/suscriptions.png)

*Figura: consulta de planes y suscripción simulada (US-19). No equivale a un pago procesado por pasarela real.*

![Vista de facturación](./Resources/chapter5/evidencia-bicigo/billing.png)

*Figura: vista de Billing. La captura por sí sola no confirma US-16 ni el cálculo de la tarifa de US-17.*

**Maintenance**

![Reporte de incidencia](./Resources/chapter5/evidencia-bicigo/report.png)

*Figura: formulario para reportar una bicicleta (US-26). En la implementación de demostración, los datos de Maintenance se mantienen mediante `localStorage`.*

Para completar las evidencias US-29 y US-33, agregar capturas de la consulta de incidencias y de la vista `/#/maintenance/management` utilizando un usuario operador de prueba. Una captura del cambio de estado `AVAILABLE → MAINTENANCE → AVAILABLE` debe identificarse expresamente como una simulación y no como una actualización de flota productiva.

**Video de ejecución**

Se debe incorporar un video que muestre, de manera continua, el recorrido por IAM, Fleet, Trip, Billing y Maintenance, indicando qué funcionalidades dependen de API simulada, cuáles usan almacenamiento local y cuáles están pendientes de integración. El enlace y el intervalo de tiempo del video **no figuran aún en el material recibido**:

```text
Microsoft Stream: PENDIENTE DE ENLACE
Minutos de demostración por contexto: PENDIENTES
```

#### 5.2.2.6. Services Documentation Evidence for Sprint Review

El Sprint 2 se centra en la Frontend Web Application. El entorno local utiliza JSON Server para ofrecer recursos de prueba mediante rutas bajo `/api/v1` y variables de entorno del frontend. Este mecanismo permite desarrollar y evaluar flujos sin depender del backend final. **No debe presentarse JSON Server como implementación de los Web Services productivos exigidos por las Technical Stories.**

En el Capítulo III se especifican Technical Stories de registro, login, flota, viajes, pagos e incidencias. La implementación y documentación OpenAPI/Swagger de esos endpoints corresponde a la iteración de backend que corresponda. Por ello, no se adjuntan aquí contratos OpenAPI atribuidos a servicios todavía no confirmados.

| Recurso | Estado documentado en Sprint 2 | Próximo paso |
|---|---|---|
| JSON Server / API de desarrollo | Disponible en desarrollo con datos de prueba | Verificar rutas y contratos de cada contexto |
| IAM | Sesión y recuperación de prueba | Conectar autenticación, autorización y recuperación reales |
| Billing | Compra simulada de planes | Integrar reglas de pago y pasarela verificada |
| Maintenance | Modo demo local; endpoints definitivos sin confirmar | Definir contrato y trasladar persistencia al backend |
| Fleet y Trip | Consumos y flujos parciales con API local | Vincular casos de uso y estados de alquiler con API definitiva |

Como evidencia complementaria se pueden enlazar `server/routes.json`, el archivo de datos de desarrollo y el README del proyecto, pero deben etiquetarse como **mock API** y no como Swagger de producción.

#### 5.2.2.7. Software Deployment Evidence for Sprint Review

En el informe se documenta la publicación de la versión frontend mediante **Firebase Hosting**. El procedimiento descrito se basa en un build de Vite y la subida de los archivos estáticos del directorio `dist`. El repositorio confirma que `firebase.json` configura `dist` como directorio público; el router implementa `createWebHashHistory`.

**Procedimiento registrado**

1. Preparar dependencias del proyecto y ejecutar `npm run build`.
2. Verificar que Vite genera los archivos de producción dentro de `dist`.
3. Autenticarse en Firebase CLI con `firebase login`.
4. Configurar Hosting para publicar `dist` y conservar el `index.html` generado.
5. Ejecutar `firebase deploy --only hosting`.
6. Validar el acceso por HTTPS y comprobar navegación, recursos estáticos y comportamiento en móvil y escritorio.

```bash
npm install
npm run build
firebase login
firebase deploy --only hosting
```

| Producto | Plataforma | URL o acceso | Estado de evidencia |
|---|---|---|---|
| Landing Page | GitHub Pages | https://startup-chapa.github.io/Landing-Page/ | Publicación documentada en Sprint 1 |
| Frontend Web Application | Firebase Hosting | https://example-pro-d6e84.web.app | URL reportada en captura del informe; **revalidar acceso y versión publicada** |
| API local de desarrollo | JSON Server | `http://127.0.0.1:3000/api/v1` | Solo para desarrollo; no accesible públicamente por estar en localhost |
| RESTful Web Services productivos | Pendiente | No disponible en la evidencia del Sprint 2 | No incluidos en el incremento actual |

**Evidencia del despliegue registrada por el equipo**

![Instalación e inicio de sesión en Firebase CLI](./Resources/chapter5/evidence5.jpeg)

*Figura: instalación y autenticación con Firebase CLI.*

![Inicio de compilación](./Resources/chapter5/evidence4.jpeg)

*Figura: autenticación y comando de compilación del frontend.*

![Inicialización de Firebase Hosting](./Resources/chapter5/evidence3.jpeg)

*Figura: generación del build e inicialización de Firebase Hosting.*

![Configuración de Hosting](./Resources/chapter5/evidence2.jpeg)

*Figura: selección de proyecto Firebase y directorio público `dist`.*

![Publicación del frontend](./Resources/chapter5/evidence1.jpeg)

*Figura: evidencia reportada del resultado de `firebase deploy --only hosting`.*

**Verificaciones pendientes.** La configuración de Hosting en el repositorio no agrega rewrites para rutas de SPA; por eso resulta relevante documentar que el frontend utiliza navegación hash. Además, el despliegue estático por sí solo no publica la API local ni valida compras, ubicación o autorizaciones productivas. Se debe comprobar desde una ventana privada y un dispositivo ajeno al equipo de desarrollo qué vistas funcionan con datos de producción y cuáles únicamente con datos simulados.

#### 5.2.2.8. Team Collaboration Insights during Sprint

La coordinación del equipo se distribuyó por cinco Bounded Contexts y se complementó con actividades compartidas de integración, verificación y documentación. La matriz de responsabilidades de 5.2.2.2 identifica liderazgo funcional; la actividad de GitHub presenta evidencia de contribuciones, pero debe interpretarse en función de la rama y el período observados.

| Integrante | GitHub Username | Contexto liderado | Rama relacionada |
|---|---|---|---|
| Adrian Andres Armestar Felipa | Adrian5102 | IAM | `feature/iam` |
| José María Franco del Carpio | VoltTrd | Trip Management | `feature/trip-management` |
| Juan David Ayllon Pauccar | JuanDPAUC | Billing & Subscriptions | `feature/billing-subscriptions` |
| Eduardo Manuel Aguirre Ramos | TheEngineEdu | Fleet & Station Management | `feature/fleet-station-management` |
| Rodrigo Velasquez Velasquez | Rodrigov233 | Maintenance | `feature/maintenance` |

**GitHub Contributors**

![GitHub Contributors: rama main](./Resources/chapter5/contributors.png)

*Figura: Contributors correspondiente a la rama `main` y al filtro de tres meses de la captura proporcionada, excluyendo commits de fusión.*

| Integrante visible en la captura | Usuario | Commits mostrados en `main` | Líneas añadidas | Líneas eliminadas |
|---|---|---:|---:|---:|
| Eduardo Manuel Aguirre Ramos | TheEngineEdu | 2 | 714 | 0 |
| José María Franco del Carpio | VoltTrd | 1 | 418 | 0 |

El panel de Contributors **no contabiliza necesariamente la actividad de las ramas `feature/*` y `develop`**. No corresponde registrar cero contribuciones para los demás miembros solo porque no aparezcan en esta captura. Del mismo modo, la captura de Pulse (5 autores y 62 commits en todas las ramas entre el 30/09 y el 07/10) no es directamente comparable con Contributors, porque mide otro conjunto de datos.

Para una evaluación completa de la colaboración se recomienda adjuntar una tabla de commits y Pull Requests filtrados por los límites reales del Sprint, con autor, rama de origen, SHA, fecha y referencia al aspecto desarrollado. Las cifras deberán actualizarse al cierre, sin inventar historiales ni atribuir aportes sin evidencia.

### 5.2.3. Sprint 3

#### 5.2.3.1. Sprint Planning 3

El Sprint 3 corresponde al primer incremento de backend de BiciGO: la implementación de los **RESTful Web Services** en el repositorio [`Startup-Chapa/backend-bicigo`](https://github.com/Startup-Chapa/backend-bicigo), una API REST desarrollada con **ASP.NET Core (.NET 10)**, **Entity Framework Core 10** y **MySQL**, organizada por **Bounded Contexts** (IAM, Trip, Billing, Fleet & Station Management, Maintenance y Shared) con capas Domain, Application, Infrastructure e Interfaces (REST). Los contratos se exponen mediante OpenAPI 3.1.1 con la interfaz **Scalar** en el entorno local `http://localhost:5267`.

**Sprint Planning Background**

| Campo | Registro de Sprint 3 |
|---|---|
| Sprint # | Sprint 3 |
| Date | 09/11/2026 (**propuesta original, por confirmar**) |
| Time | 20:00–21:00, hora de Lima (**propuesta**) |
| Location | Reunión virtual |
| Prepared By | Aguirre Ramos, Eduardo Manuel  |
| Attendees | Aguirre Ramos, Eduardo Manuel; Armestar Felipa, Adrian Andres; Ayllon Pauccar, Juan David; Franco del Carpio, José María; Velasquez Velasquez, Rodrigo |
| Sprint 2 Review Summary | Se integró y publicó la primera versión navegable de la Frontend Web Application con módulos por Bounded Context, API simulada (JSON Server) y Firebase Hosting. Quedaron pendientes de validar evidencias de algunos flujos (inicio, viaje activo y cierre de alquiler; método de pago). |
| Sprint 2 Retrospective Summary | Se acordó trasladar la lógica al backend real organizado por Bounded Contexts, asignar un líder por contexto, versionar la API bajo el prefijo `/api/v1` y documentar los contratos con OpenAPI antes de reintegrar el frontend. |

**Sprint Goal & User Stories**

*Our focus is on implementing and connecting the backend services required by BiciGO's priority user journeys. We believe it will replace key simulated operations with verifiable RESTful endpoints and allow the frontend and backend to work as a consistent application. This will be confirmed when the selected Technical Stories meet their acceptance criteria, API contracts are documented, and end-to-end scenarios can be demonstrated.*

| Campo | Situación |
|---|---|
| Selected Technical Stories | IAM: TS-15 (con cobertura parcial de TS-01). Trip: TS-08, TS-09, TS-10, TS-11. Billing: TS-12, TS-13, TS-14. Fleet: TS-05, TS-06. Maintenance: TS-17, TS-18, TS-19. Transversal: persistencia compartida, seeder y documentación OpenAPI (TS-SH01) y despliegue del backend en Azure App Service (TS-SH02). |
| Cobertura parcial | TS-02, TS-03 y TS-04 (login, recuperación y verificación) no cuentan con endpoints de autenticación dedicados; el registro se expone como `POST /api/v1/users` y el acceso por correo como `GET /api/v1/users?email=`. Su cierre se plantea para una iteración posterior. |
| Historias no incluidas | TS-07 (Search Coverage Zone) y TS-20 (Get Dashboard Metrics) quedan fuera del alcance del Sprint 3. |
| Sum of Story Points | 41 SP de Technical Stories + 8 SP del trabajo transversal (Shared y despliegue en Azure) = **49 SP** (escala 1, 2, 3 y 5). |
| Task Estimation | **67 h**, correspondientes a 21 microtareas. |
| Sprint 3 Velocity | Pendiente de validar contra los criterios de aceptación de cada Technical Story. |

**Distribución estimada de Story Points**

| Story Id | Story Title | Story Points |
|---|---|---:|
| TS-05 | Get Nearby Bikes (Fleet) | 3 |
| TS-06 | Get Bike Detail (Fleet) | 2 |
| TS-08 | Start Rental (Trip) | 5 |
| TS-09 | Unlock Bike (Trip) | 3 |
| TS-10 | Get Active Rental (Trip) | 2 |
| TS-11 | Finish Rental (Trip) | 5 |
| TS-12 | Register Payment Method (Billing) | 3 |
| TS-13 | Process Rental Payment (Billing) | 5 |
| TS-14 | Manage Subscription (Billing) | 3 |
| TS-15 | Get User Profile (IAM) | 2 |
| TS-17 | Create Incident (Maintenance) | 3 |
| TS-18 | Get Incident Status (Maintenance) | 2 |
| TS-19 | Manage Bike Status (Maintenance) | 3 |
| TS-SH01 | Persistencia compartida, seeder y OpenAPI (transversal) | 5 |
| TS-SH02 | Deploy Backend to Azure App Service (transversal) | 3 |
| **Total** | **13 Technical Stories + 2 transversales** | **49** |

#### 5.2.3.2. Aspect Leaders and Collaborators

La organización del Sprint 3 se encuentra basada en los cinco Bounded Contexts definidos durante el diseño de arquitectura.

Cada integrante lidera un contexto y participa como colaborador en los demás. Respecto al Sprint 2, Fleet y Maintenance rotaron **intencionalmente** entre Eduardo Aguirre y Rodrigo Velasquez: Rodrigo asume Fleet & Station Management y Eduardo asume Maintenance. El cambio fue acordado en la planificación para repartir el conocimiento de la capa de datos, ya que Fleet administra los agregados de bicicletas y estaciones, y Maintenance registra reportes e historial de estados sobre esas mismas unidades. El trabajo transversal del contexto Shared (persistencia, seeder y OpenAPI) se distribuyó entre todo el equipo según el backlog.

| Team Member | GitHub Username | IAM | Trip Management | Billing & Subscriptions | Fleet & Station Management | Maintenance |
|---|---|:---:|:---:|:---:|:---:|:---:|
| Armestar Felipa, Adrian Andres | Adrian5102 | L | C | C | C | C |
| Franco del Carpio, José María | VoltTrd | C | L | C | C | C |
| Ayllon Pauccar, Juan David | JuanDPAUC | C | C | L | C | C |
| Aguirre Ramos, Eduardo Manuel | TheEngineEdu | C | C | C | C | L |
| Velasquez Velasquez, Rodrigo | Rodrigov233 | C | C | C | L | C |

**L:** Leader  
**C:** Collaborator

La distribución permite implementar cada contexto de forma paralela sobre el repositorio `backend-bicigo` y luego exponer los recursos en una API común bajo el prefijo `/api/v1`.

#### 5.2.3.3. Sprint Backlog 3

El backlog organiza 21 microtareas agrupadas por Bounded Context y actividades transversales, con una estimación total de **67 horas**. Las tareas siguen la convención `T3-XX` y se asocian a las Technical Stories del Capítulo III.

**Trello del Sprint 3**

![Tablero Trello de Sprint 3](./Resources/chapter5/trello3.png)

[Sprint 3 — Trello](https://trello.com/invite/b/6af3d267ba7a4372b40bbdd6/ATTI31ef73f3a471df4c015b5d06485dd09712588AB8/sprint-3)



**Sprint #: Sprint 3**

| Epic / Story ID | Task ID | Título de la Microtarea | Descripción y Alcance Técnico | Estimación (Horas) | Asignado a | Estado |
| :--- | :--- | :--- | :--- | :---: | :--- | :---: |
| **TS-SH01** | T3-01 | Solución y estructura por Bounded Contexts | Crear la solución .NET 10 con las carpetas `Iam`, `Trip`, `Billing`, `Fleet`, `Maintenance` y `Shared`, y registrar los servicios de cada contexto en `Program.cs`. | 3 h | Equipo | Done |
| **TS-SH01** | T3-02 | AppDbContext MySQL y repositorios base | Configurar `AppDbContext` con MySQL (`MySql.EntityFrameworkCore`), `UnitOfWork`, `BaseRepository` y `AuditableEntityInterceptor`. | 3 h | Equipo | Done |
| **TS-SH01** | T3-03 | Seeder y tablas normalizadas | Implementar `DatabaseSeeder` y la creación idempotente de `plan_features`, `user_notifications`, `bicycle_assignments`, `trip_users`, `trip_route_points`, `trip_photo_evidences` y `maintenance_status_histories`. | 3 h | Equipo | Done |
| **TS-SH01** | T3-04 | OpenAPI 3.1.1 y Scalar | Habilitar `AddOpenApi`/`MapOpenApi` y `MapScalarApiReference` para documentar y explorar la API en el entorno local. | 2 h | Equipo | Done |
| **TS-15** | T3-05 | Dominio y aplicación de Users | Modelar el agregado `User` con sus comandos y consultas (registro, consulta por correo), su repositorio y los servicios de aplicación. | 3 h | Armestar Felipa, Adrian Andres | Done |
| **TS-15** | T3-06 | Users REST: CRUD y PATCH de perfil | Exponer `POST /api/v1/users` (201/400/409), `GET /api/v1/users?email=`, `GET /{id}`, `PATCH /{id}` (perfil, plan y balance) y `DELETE /{id}` con assemblers. | 3 h | Armestar Felipa, Adrian Andres | Done |
| **TS-15** | T3-07 | UserNotifications REST | Implementar `GET`/`POST /api/v1/user-notifications` y `PATCH /{id}/read` para las notificaciones del usuario. | 3 h | Armestar Felipa, Adrian Andres | Done |
| **TS-08** | T3-08 | Dominio y persistencia de Trips | Modelar el agregado `Trip` con sus estados, comandos y consultas, y su repositorio EFC. | 4 h | Franco del Carpio, José María | Done |
| **TS-08/10/11** | T3-09 | Trips REST: ciclo de alquiler | Exponer `POST /api/v1/trips` (inicio), `GET /{id}` (consulta), `PUT /{id}` (actualización y cierre), `DELETE /{id}` y el listado `GET /api/v1/trips`. | 4 h | Franco del Carpio, José María | Done |
| **TS-10** | T3-10 | TripUsers REST | Implementar `GET`/`POST /api/v1/trip-users` y `GET /{id}` para asociar usuarios al viaje. | 2 h | Franco del Carpio, José María | Done |
| **TS-11** | T3-11 | Route points y evidencias fotográficas | Implementar `api/v1/trip-route-points` y `api/v1/trip-photo-evidences` (consulta y registro). | 2 h | Franco del Carpio, José María | Done |
| **TS-09** | T3-12 | QrValidations REST | Implementar `GET`/`POST /api/v1/qr-validations` y `GET /{id}` para la validación QR del desbloqueo del alquiler vigente. | 3 h | Franco del Carpio, José María | Done |
| **TS-12** | T3-13 | PaymentMethods y Payments REST | Implementar `GET`/`POST /api/v1/payment-methods`, `GET/POST /api/v1/payments` y `GET /payments/{id}`. | 4 h | Ayllon Pauccar, Juan David | Done |
| **TS-14** | T3-14 | Plans, PlanFeatures y Subscriptions | Exponer `GET /api/v1/plans` y `GET /{id}`, `GET`/`POST /api/v1/plan-features` y `GET`/`POST /api/v1/subscriptions` (activación de plan). | 4 h | Ayllon Pauccar, Juan David | Done |
| **TS-05/06** | T3-15 | Bicycles REST y estados | Modelar el agregado `Bicycle` con el value object `BicycleStatus` y exponer `GET`/`POST`/`PUT`/`DELETE /api/v1/bicycles` (disponibilidad y detalle). | 4 h | Velasquez Velasquez, Rodrigo | Done |
| **TS-05** | T3-16 | BikePoints y BicycleAssignments | Implementar `GET`/`POST`/`PUT`/`DELETE /api/v1/bike-points` y `GET`/`POST /api/v1/bicycle-assignments` (ubicación y asignaciones). | 3 h | Velasquez Velasquez, Rodrigo | Done |
| **TS-17/18** | T3-17 | MaintenanceReports REST | Modelar el reporte de mantenimiento e implementar `GET`/`POST /api/v1/maintenance-reports` y `GET /{id}`. | 4 h | Aguirre Ramos, Eduardo Manuel | Done |
| **TS-19** | T3-18 | Cambio de estado e historial | Implementar `POST /api/v1/maintenance-reports/{bikeId}/status` y `GET`/`POST /api/v1/maintenance-status-histories` con el agregado `MaintenanceStatusHistory`. | 3 h | Aguirre Ramos, Eduardo Manuel | Done |
| **Transversal** | T3-19 | Pruebas locales de la API | Ejecutar la API con MySQL y verificar los contratos de cada contexto desde Scalar: al menos una respuesta exitosa y un caso de error por recurso. | 3 h | Equipo | To-Review |
| **Transversal** | T3-20 | Documentación del Sprint 3 en el informe | Redactar las secciones 5.2.3.1 a 5.2.3.8 y actualizar la tabla de repositorios de 5.1.2 con `backend-bicigo`. | 3 h | Aguirre Ramos, Eduardo Manuel | Done |
| **TS-SH02** | T3-21 | Despliegue del backend en Railway | Configurar el servicio `backend-bicigo` y la base MySQL gestionada en Railway (con volumen persistente), publicar la API desde GitHub mediante el Dockerfile del repositorio y registrar la URL pública verificada. | 4 h | Equipo | Done |

**Criterio para el cierre.** Una Technical Story solo pasa a `Done` cuando su recurso responde en el entorno local, el contrato figura en OpenAPI y sus escenarios se pueden reproducir contra la base MySQL con los datos del seeder. La cobertura parcial de autenticación (TS-02 a TS-04) queda fuera del cierre del Sprint 3. El despliegue del backend previsto en TS-SH02 se materializó en la plataforma **Railway**, en lugar del Azure App Service previsto inicialmente, y acreditó la URL pública del servicio (sección 5.2.3.7), por lo que T3-21 pasa a `Done`.

#### 5.2.3.4. Development Evidence for Sprint Review

El desarrollo se documenta en el repositorio [`Startup-Chapa/backend-bicigo`](https://github.com/Startup-Chapa/backend-bicigo). Cada contexto organiza sus capas como `Domain` (agregados, value objects, comandos y consultas), `Application` (servicios de comando y consulta), `Infrastructure` (repositorios EFC) e `Interfaces` (controllers, resources y assemblers REST), sobre el contexto `Shared`, que registra el `DbContext`, el unit of work y el seeder.

| Bounded Context | Carpeta | Recursos REST implementados | Agregados principales |
|---|---|---|---|
| IAM | `Iam/` | `users`, `user-notifications` | `User`, `UserNotification` |
| Trip Management | `Trip/` | `trips`, `trip-users`, `trip-route-points`, `trip-photo-evidences`, `qr-validations` | `Trip`, `TripUser`, `TripRoutePoint`, `TripPhotoEvidence`, `QrValidation` |
| Billing & Subscriptions | `Billing/` | `plans`, `plan-features`, `payments`, `payment-methods`, `subscriptions` | `Plan`, `Payment`, `Subscription` |
| Fleet & Station Management | `Fleet/` | `bicycles`, `bike-points`, `bicycle-assignments` | `Bicycle`, `BikePoint`, `BicycleAssignment` |
| Maintenance | `Maintenance/` | `maintenance-reports`, `maintenance-status-histories` | `MaintenanceReport`, `MaintenanceStatusHistory` |

`Program.cs` registra los servicios de cada contexto, configura MySQL mediante la cadena `DefaultConnection` y, al arrancar, ejecuta `EnsureCreated`, crea las siete tablas normalizadas con `CREATE TABLE IF NOT EXISTS` y aplica el `DatabaseSeeder`.

![Documentación Swagger del backend biciGO](./Resources/chapter5/backend-swagger-sprint3.png)

*Figura: documentación OpenAPI 3.1.1 de `backend-bicigo v1`, abierta en el entorno local `http://localhost:5267`.*

![Estructura del repositorio backend-bicigo](./Resources/chapter5/railway/railway-repo-estructura.jpeg)

*Figura: estructura de la rama `main` del repositorio `backend-bicigo`, con los Bounded Contexts (Billing, Fleet, Iam, Maintenance, Shared y Trip), el `Dockerfile` utilizado por Railway y los archivos de configuración por entorno.*

**Historial de commits del backend — PENDIENTE DE ADJUNTAR.** Esta sección debe completarse con la tabla de commits de la rama `develop` del backend (SHA, mensaje, autor y fecha) filtrada por el rango del Sprint 3 y la captura de GitHub Pulse del repositorio `backend-bicigo`, siguiendo el formato de las secciones 5.2.1.4 y 5.2.2.4.

#### 5.2.3.5. Execution Evidence for Sprint Review

La evidencia de ejecución debe mostrar solicitudes reales contra la API local. Para cerrar esta sección se requieren capturas por contexto que incluyan al menos una respuesta exitosa y un caso de error coherente con los criterios de aceptación del Capítulo III:

| Bounded Context | Solicitudes sugeridas para la evidencia |
|---|---|
| IAM | `POST /api/v1/users` (201), `POST /api/v1/users` con correo duplicado (409), `PATCH /api/v1/users/{id}` |
| Trip | `POST /api/v1/trips`, `GET /api/v1/trips/{id}`, `POST /api/v1/qr-validations` |
| Billing | `GET /api/v1/plans`, `POST /api/v1/payment-methods`, `POST /api/v1/payments` |
| Fleet | `GET /api/v1/bicycles`, `POST /api/v1/bicycle-assignments` |
| Maintenance | `POST /api/v1/maintenance-reports`, `POST /api/v1/maintenance-reports/{bikeId}/status` |

```text
Capturas de ejecución por contexto: PENDIENTES DE ADJUNTAR
Video de ejecución: PENDIENTE DE ENLACE
```

#### 5.2.3.6. Services Documentation Evidence for Sprint Review

La documentación se expone como **OpenAPI 3.1.1** (`backend-bicigo v1`) y se explora con **Scalar** en el servidor local `http://localhost:5267`. La siguiente tabla corresponde a las **60 operaciones implementadas en los 17 controllers** del repositorio, extraídas del código fuente:

| Bounded Context | Recurso | Operación | Método y ruta |
|---|---|---|---|
| IAM | Users | Registro de usuario | `POST /api/v1/users` |
| IAM | Users | Listado y filtro por correo | `GET /api/v1/users?email={email}` |
| IAM | Users | Usuario por identificador | `GET /api/v1/users/{id}` |
| IAM | Users | Actualización parcial (perfil, plan, balance) | `PATCH /api/v1/users/{id}` |
| IAM | Users | Eliminación de usuario | `DELETE /api/v1/users/{id}` |
| IAM | User Notifications | Notificaciones de usuario | `GET /api/v1/user-notifications` |
| IAM | User Notifications | Notificación por identificador | `GET /api/v1/user-notifications/{id}` |
| IAM | User Notifications | Crear notificación | `POST /api/v1/user-notifications` |
| IAM | User Notifications | Marcar como leída | `PATCH /api/v1/user-notifications/{id}/read` |
| Trip | Trips | Listado de viajes | `GET /api/v1/trips` |
| Trip | Trips | Viaje por identificador | `GET /api/v1/trips/{id}` |
| Trip | Trips | Inicio de alquiler | `POST /api/v1/trips` |
| Trip | Trips | Actualización y cierre | `PUT /api/v1/trips/{id}` |
| Trip | Trips | Eliminación de viaje | `DELETE /api/v1/trips/{id}` |
| Trip | Trip Users | Usuarios del viaje | `GET /api/v1/trip-users` · `GET /{id}` · `POST /` |
| Trip | Trip Route Points | Puntos de recorrido | `GET /api/v1/trip-route-points` · `GET /{id}` · `POST /` |
| Trip | Trip Photo Evidences | Evidencias fotográficas | `GET /api/v1/trip-photo-evidences` · `GET /{id}` · `POST /` |
| Trip | QR Validations | Validación QR para desbloqueo | `GET /api/v1/qr-validations` · `GET /{id}` · `POST /` |
| Billing | Plans | Listado y detalle de planes | `GET /api/v1/plans` · `GET /{id}` |
| Billing | Plan Features | Características de plan | `GET /api/v1/plan-features` · `GET /{id}` · `POST /` |
| Billing | Payments | Pagos | `GET /api/v1/payments` · `POST /` · `GET /{id}` |
| Billing | Payment Methods | Métodos de pago | `GET /api/v1/payment-methods` · `POST /` · `GET /{id}` |
| Billing | Subscriptions | Suscripciones | `GET /api/v1/subscriptions` · `GET /{id}` · `POST /` |
| Fleet | Bicycles | Flota de bicicletas | `GET /api/v1/bicycles` · `GET /{id}` · `POST /` · `PUT /{id}` · `DELETE /{id}` |
| Fleet | Bike Points | Estaciones y puntos | `GET /api/v1/bike-points` · `GET /{id}` · `POST /` · `PUT /{id}` · `DELETE /{id}` |
| Fleet | Bicycle Assignments | Asignaciones bicicleta–punto | `GET /api/v1/bicycle-assignments` · `GET /{id}` · `POST /` |
| Maintenance | Maintenance Reports | Reportes de mantenimiento | `GET /api/v1/maintenance-reports` · `GET /{id}` · `POST /` |
| Maintenance | Maintenance Reports | Cambio de estado de bicicleta | `POST /api/v1/maintenance-reports/{bikeId}/status` |
| Maintenance | Status Histories | Historial de estados | `GET /api/v1/maintenance-status-histories` · `GET /{id}` · `POST /` |

**Desalineación de prefijos.** El backend usa el prefijo `/api/v1/...`, mientras que los ejemplos del Capítulo III escriben `/api/...` con rutas como `/api/auth/register`, `/api/bikes/nearby` o `/api/rentals`. Antes del cierre, el equipo debe alinear los contratos de las Technical Stories con las rutas reales o documentar el mapeo entre ambas. La correspondencia funcional principal es: registro (`TS-01`) → `POST /api/v1/users`; detalle de bicicleta (`TS-06`) → `GET /api/v1/bicycles/{id}`; inicio de alquiler (`TS-08`) → `POST /api/v1/trips`; desbloqueo (`TS-09`) → `POST /api/v1/qr-validations`; consulta del viaje activo (`TS-10`) → `GET /api/v1/trips/{id}`; finalización (`TS-11`) → `PUT /api/v1/trips/{id}`; método de pago (`TS-12`) → `POST /api/v1/payment-methods`; pago del alquiler (`TS-13`) → `POST /api/v1/payments`; suscripción (`TS-14`) → `POST /api/v1/subscriptions`; reporte de incidencia (`TS-17`) → `POST /api/v1/maintenance-reports`; cambio de estado administrativo (`TS-19`) → `POST /api/v1/maintenance-reports/{bikeId}/status`.

#### 5.2.3.7. Software Deployment Evidence for Sprint Review

El backend del Sprint 3 se **ejecuta localmente** con MySQL y se encuentra **desplegado en producción en Railway** (tarea T3-21, `Done`). La evidencia comprende tres niveles: la ejecución local con documentación OpenAPI/Scalar en `localhost:5267`, el aprovisionamiento inicial de una base de datos MySQL en Azure como parte del plan de despliegue, y el despliegue productivo del servicio en Railway con su propio MySQL gestionado. No debe confundirse con la publicación del frontend en Firebase Hosting documentada para el Sprint 2.

**Aprovisionamiento inicial de la base de datos MySQL en Azure (12/11/2026)**

Como parte del plan de despliegue, el equipo aprovisionó en Azure una base de datos MySQL para el backend, mediante el servicio **Azure Database for MySQL Flexible Server**. Este aprovisionamiento fue preparatorio: el despliegue productivo finalmente se materializó en Railway con la base MySQL gestionada de esa plataforma (se describe más abajo), por lo que el servidor de Azure se mantuvo detenido para controlar los costos. Los pasos realizados y su evidencia son los siguientes:

1. Se creó el servidor `new-backend-bicigo` en el grupo de recursos `backend-project`, en la región **Chile Central**, con MySQL **8.4**, carga de trabajo *Dev/Test* y configuración *Burstable B1ms* (1 vCore, 2 GiB RAM, 20 GiB de almacenamiento).

![Creación del servidor MySQL Flexible Server en Azure](./Resources/chapter5/azure/azure-mysql-basics.jpeg)

*Figura: configuración básica del servidor `new-backend-bicigo` (región Chile Central, MySQL 8.4, Burstable B1ms).*

2. Se configuró la autenticación exclusiva de **MySQL** con el usuario administrador `backendroot`.

![Configuración de autenticación del servidor MySQL](./Resources/chapter5/azure/azure-mysql-auth.jpeg)

*Figura: método de autenticación "MySQL authentication only" y administrador del servidor.*

3. En la pestaña *Networking* se habilitó el **acceso público** con direcciones IP permitidas, el puerto **3306** y el acceso desde servicios de Azure.

![Configuración de red del servidor MySQL](./Resources/chapter5/azure/azure-mysql-networking.jpeg)

*Figura: conectividad pública del servidor MySQL Flexible Server y puerto 3306.*

4. Se agregó la regla de firewall necesaria para las conexiones del equipo durante la verificación inicial.

![Regla de firewall del servidor MySQL](./Resources/chapter5/azure/azure-mysql-firewall.jpeg)

*Figura: regla de firewall configurada para la verificación de conexiones.*

5. El servidor quedó aprovisionado el **12/11/2026 (16:14 UTC)** con el endpoint `new-backend-bicigo.mysql.database.azure.com`. Tras la verificación inicial, el servidor se detuvo (*Stop*) para controlar los costos del nivel *Dev/Test*; puede reiniciarse o eliminarse si el equipo decide migrar la persistencia productiva a Azure.

![Servidor MySQL creado en Azure](./Resources/chapter5/azure/azure-mysql-overview.jpeg)

*Figura: vista general del servidor `new-backend-bicigo` con su endpoint y la acción de detención.*

**Despliegue productivo del backend en Railway (T3-21 — `Done`)**

La plataforma final de despliegue fue **Railway**, donde la API quedó publicada y accesible públicamente con su documentación en:

[https://backend-bicigo-production.up.railway.app/scalar/v1](https://backend-bicigo-production.up.railway.app/scalar/v1)

El procedimiento realizado fue el siguiente:

1. Se creó el proyecto en Railway con dos servicios: `backend-bicigo` (API .NET 10) y **MySQL gestionado** con volumen persistente (`mysql-volume`).

![Proyecto en Railway con el servicio backend-bicigo y MySQL](./Resources/chapter5/railway/railway-project-mysql-tablas.jpeg)

*Figura: proyecto en Railway (entorno production) con los servicios MySQL y backend-bicigo en estado Online, y las tablas de la base de datos.*

2. Se configuró la red del servicio: dominio público `backend-bicigo-production.up.railway.app` (puerto 8080) y red privada `backend-bicigo.railway.internal`.

![Configuración de red pública del servicio backend-bicigo](./Resources/chapter5/railway/railway-dominio-publico.jpeg)

*Figura: dominio público y networking del servicio backend-bicigo en Railway.*

3. Se conectó el repositorio `backend-bicigo` para el despliegue automático desde GitHub mediante el `Dockerfile` del proyecto. Un primer intento de despliegue falló en los checks de Railway y se corrigió con el commit `fix:add final` sobre la rama `main`.

![Primer intento de despliegue con error de checks](./Resources/chapter5/railway/railway-repo-primer-intento.jpeg)

*Figura: commit `fix:add final` en la rama `main` del repositorio durante el proceso de despliegue, con el resultado fallido del primer intento.*

4. El despliegue finalizó correctamente: el deployment quedó **Active** con el estado *Deployment successful*.

![Despliegue exitoso del backend en Railway](./Resources/chapter5/railway/railway-deployment-exitoso.jpeg)

*Figura: deployment Active del servicio backend-bicigo en Railway tras el commit `fix:add final`.*

5. Al inicializar la API, se crearon las **17 tablas** del modelo de datos (users, user_notifications, trips, trip_users, trip_route_points, trip_photo_evidences, qr_validations, plans, plan_features, payments, payment_methods, subscriptions, bicycles, bike_points, bicycle_assignments, maintenance_reports y maintenance_status_histories) junto con los datos del seeder.

![Base de datos MySQL creada en Railway](./Resources/chapter5/railway/railway-mysql-tablas.jpeg)

*Figura: tablas de la base MySQL gestionada en Railway, creadas por la API al inicializar.*

6. Se verificó el acceso público a la documentación Scalar y a los contratos de cada contexto en la URL registrada.

| Producto | Plataforma | URL o acceso | Estado de evidencia |
|---|---|---|---|
| Backend API (Sprint 3) | Railway (producción) | https://backend-bicigo-production.up.railway.app | Desplegado; deployment Active |
| Documentación OpenAPI (producción) | Scalar en Railway | https://backend-bicigo-production.up.railway.app/scalar/v1 | URL pública verificada |
| Documentación OpenAPI (local) | Scalar (local) | `http://localhost:5267` | Captura incluida en 5.2.3.4 |
| Base de datos MySQL en Railway | MySQL gestionado + volumen en Railway | Red privada `backend-bicigo.railway.internal` | 17 tablas creadas al inicializar la API |
| Base de datos MySQL en Azure | Azure Database for MySQL Flexible Server | `new-backend-bicigo.mysql.database.azure.com` | Aprovisionada el 12/11/2026 como parte del plan; servidor detenido para control de costos |
| Frontend Web Application | Firebase Hosting | https://example-pro-d6e84.web.app | Publicación documentada en Sprint 2 |

**URL pública registrada.** Con el despliegue en Railway, la tarea T3-21 se cierra con la URL pública del backend y su documentación verificadas. El servidor MySQL de Azure permanece detenido como aprovisionamiento preparatorio y puede eliminarse o reiniciarse si el equipo decide migrar la persistencia productiva a Azure.

#### 5.2.3.8. Team Collaboration Insights during Sprint

El trabajo se distribuyó por Bounded Contexts según la matriz de 5.2.3.2, con la rotación intencional de Fleet y Maintenance respecto al Sprint 2. El contexto Shared (persistencia, seeder y documentación OpenAPI) se trabajó de forma transversal.

| Integrante | GitHub Username | Contexto liderado | Technical Stories principales |
|---|---|---|---|
| Armestar Felipa, Adrian Andres | Adrian5102 | IAM | TS-15 (y cobertura parcial de TS-01) |
| Franco del Carpio, José María | VoltTrd | Trip Management | TS-08, TS-09, TS-10, TS-11 |
| Ayllon Pauccar, Juan David | JuanDPAUC | Billing & Subscriptions | TS-12, TS-13, TS-14 |
| Aguirre Ramos, Eduardo Manuel | TheEngineEdu | Maintenance | TS-17, TS-18, TS-19 |
| Velasquez Velasquez, Rodrigo | Rodrigov233 | Fleet & Station Management | TS-05, TS-06 |

**Evidencia de contribución — PENDIENTE DE ADJUNTAR.** Al cierre se debe incorporar la captura de GitHub Pulse y la tabla de commits del repositorio `backend-bicigo` (autor, rama, SHA, fecha y Technical Story asociada) filtradas por el rango real del Sprint 3, sin atribuir aportes sin evidencia.

## 5.3. Validation Interviews.
### 5.3.1. Diseño de Entrevistas.

### 5.3.2. Registro de Entrevistas.

#### Entrevista 1

| Campo | Detalle |
|---|---|
| Entrevistado | Fernando Guere (nombre visible en la captura) |
| Segmento | Usuario de movilidad urbana que realiza trayectos cotidianos y recorridos cortos |
| Entrevistador | Juan David Ayllon |
| Video | [Ver entrevista en Microsoft Stream](https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241a860_upc_edu_pe/IQB7Vo7PzItDQZnS5a6Q6wJbAbt5YZamBytgUuFBTexmkEA?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=YgDPsl) |
| Tiempo | 00:00–17:35 (17 min 35 s) |

![Imagen 2. Evidencia de la entrevista de validación de BiciGO](./Resources/chapter5/entrevista-validacion.png)

*Resumen de apreciaciones:* El entrevistado consideró que la propuesta y la aplicación se entienden y valoró positivamente la facilidad para ubicar una unidad, iniciar y seguir un recorrido, así como conocer la tarifa estimada antes de confirmar. Como oportunidad de mejora para la Landing Page, señaló que algunos espacios se perciben desaprovechados y que la separación entre el contenido y las imágenes afecta el atractivo visual. Indicó que usaría el servicio sobre todo para trayectos cortos y destacó como posibles barreras la falta de conexión a Internet, la disponibilidad de unidades y las opciones de pago; además, propuso compartir el viaje en tiempo real y permitir dividir la tarifa. La transcripción también incluye referencias a mototaxis, conductores y placas, por lo que esas opiniones de seguridad no se consideran una validación directa del flujo de alquiler de bicicletas de BiciGO. La edad y el distrito del entrevistado no aparecen en la transcripción disponible.

#### Entrevista 2

| Campo | Detalle |
|---|---|
| Entrevistado | Mauricio |
| Segmento | Usuario de movilidad urbana que realiza trayectos cotidianos y recorridos cortos |
| Entrevistador | Adrian Armestar |
| Video | [Ver entrevista en Youtube](https://www.youtube.com/watch?v=KC9VsKTfLH0) |
| Tiempo | 00:00–06:18 (6 min 18 s) |

![Imagen 2. Evidencia de la entrevista de validación de BiciGO](./Resources/chapter5/entrevista-validacion2.png)

*Resumen de apreciaciones:* El entrevistado consideró que el proceso de ingresar el punto de partida y el destino en la aplicación BiciGO es sencillo y rápido, destacando que no genera distracciones innecesarias. Asimismo, valoro positivamente conocer la tarifa estimada antes de confirmar el viaje, ya que esta brinda transparencia y permite que cada usuario decida según su situación económica. Del mismo modo, señaló que utilizaría el servicio tanto para trasladarse a estudiar como para otros desplazamientos cotidianos, destacando la ventaja de las ciclovías frente al tráfico constante de Lima y el mayor control sobre sus tiempos de traslado en comparación con el transporte público. Como oportunidad de mejora, propuso incorporar puntos de interés en el mapa y durante los recorridos, como restaurantes, parques y tiendas, para enriquecer la experiencia e incentivar nuevos recorridos de manera que fomente el uso frecuente de la aplicación.

### 5.3.3. Evaluaciones según heurísticas.
 
| Campo | Detalle |
|-------|---------|
| CARRERA | Ingenieria de Software |
| CURSO | Aplicaciones Web |
| SECCIÓN | 8168 |
| PROFESORES | Todos |
| AUDITOR | Bicigo |
| CLIENTE(S) |  Aguirre, Eduardo & Armestar, Adrian & Ayllon, Juan David & Franco, José Maria & Velasquez, Rodrigo |
| SITE A EVALUAR | https://github.com/Startup-Chapa/project-report |
 
#### TAREAS A EVALUAR
 
El alcance de esta evaluación incluye la revisión de la usabilidad de las siguientes tareas:
 
1. Navegación general del Landing Page y comportamiento responsive del header
2. Cambio de idioma (EN/ES) en el Landing Page y en la Web Application
3. Lectura del contenido informativo del Landing Page (beneficios y "¿Cómo funciona?")
4. Inicio de sesión (login)
5. Registro de un nuevo usuario (correo, usuario, contraseña y teléfono)
6. Consulta y comparación de planes (Plan Tarifa / Suscripción Pro)
7. Registro de pago con tarjeta para la Suscripción Pro
8. Consulta y gestión de bicicletas (Fleet & Station Management)
9. Gestión de perfil y guardado de cambios
10. Navegación del dashboard y del sidebar
11. Uso del buscador del header
 
#### ESCALA DE SEVERIDAD
 
| Nivel | Descripción |
|-------|-------------|
| 1 | Problema superficial: puede ser fácilmente superado por el usuario u ocurre con muy poca frecuencia. No necesita ser corregido a menos que exista disponibilidad de tiempo. |
| 2 | Problema menor: puede ocurrir con más frecuencia o es algo más difícil de superar para el usuario. Se le debería asignar una prioridad baja resolverlo de cara al siguiente release. |
| 3 | Problema mayor: ocurre frecuentemente o los usuarios no son capaces de resolverlo. Es importante que sea corregido y se le debe asignar una prioridad alta. |
| 4 | Problema muy grave: un error de gran impacto que impide al usuario continuar con el uso de la herramienta. Es imperativo que sea corregido antes del lanzamiento. |
 
#### TABLA RESUMEN
 
| # | Problema | Severidad | Heurística / Principio violado | Plan afectado |
|---|----------|-----------|-------------------------------|---------------|
| 1 | En vista móvil, el header del Landing Page no ofrece menú hamburguesa y los enlaces de navegación desaparecen | 3 | Usability: Consistencia y estándares / Flexibilidad y eficiencia de uso | Todos |
| 2 | El selector de idioma EN/ES del Landing Page se ve como botones sin estilo, apilados y sin indicar el idioma activo | 2 | Usability: Visibilidad del estado del sistema / Consistencia y estándares | Todos |
| 3 | La sección "¿Cómo funciona?" es un único bloque de texto sin pasos y omite a los trabajadores | 2 | Usability: Reconocimiento antes que recuerdo / Coincidencia entre el sistema y el mundo real | Todos |
| 4 | Las tarjetas de beneficios son solo texto, sin íconos ni jerarquía visual | 1 | Usability: Diseño estético y minimalista | Todos |
| 5 | En el login, el selector de idioma está dentro de la fila de "Forgot Password?" y "Remember me" | 2 | Usability: Consistencia y estándares / Inclusive Design: Offer choice | Todos |
| 6 | El registro no muestra requisitos de contraseña, no pide confirmarla y el teléfono no indica formato | 2 | Usability: Prevención de errores / Ayuda y documentación | Todos |
| 7 | La comparación de planes no muestra la tarifa del Plan Tarifa ni explica por qué se recomienda la Suscripción Pro | 2 | Usability: Reconocimiento antes que recuerdo / Ayuda y documentación | Todos |
| 8 | El formulario de pago expone el botón "Generar datos aleatorios" | 3 | Usability: Prevención de errores / Coincidencia entre el sistema y el mundo real | Suscripción Pro |
| 9 | El formulario de pago tiene etiquetas inconsistentes y no guía el formato de tarjeta y CVV | 2 | Usability: Consistencia y estándares / Reconocimiento antes que recuerdo | Suscripción Pro |
| 10 | Las acciones de gestión de flota (crear, editar, eliminar bicicletas) aparecen en el mismo menú del usuario sin distinción de rol | 3 | Usability: Prevención de errores / Coincidencia entre el sistema y el mundo real | Todos |
| 11 | La vista de bicicletas muestra textos de relleno ("Bicycles Title" / "Bicycles Subtitle") | 2 | Usability: Coincidencia entre el sistema y el mundo real / Consistencia y estándares | Todos |
| 12 | Las acciones de cada bicicleta son íconos sin etiqueta y la columna "Actions" queda lejos de ellos | 2 | Usability: Reconocimiento antes que recuerdo | Todos |
| 13 | "Current Station" muestra un ID numérico y los códigos de bicicleta no siguen un mismo formato | 2 | Usability: Coincidencia entre el sistema y el mundo real / Consistencia y estándares | Todos |
| 14 | La contraseña se edita en el mismo formulario del perfil, sin un flujo de cambio seguro | 3 | Usability: Prevención de errores | Todos |
| 15 | La locación del perfil parece ser un campo de texto libre en lugar de una lista de opciones | 2 | Usability: Prevención de errores / Consistencia y estándares | Todos |
| 16 | El perfil solo ofrece "Save changes", sin opción de cancelar o restablecer | 1 | Usability: Control y libertad del usuario | Todos |
| 17 | La interfaz mezcla inglés y español aunque el idioma activo es EN | 3 | Usability: Consistencia y estándares / Inclusive Design: Offer choice | Todos |
| 18 | Las tarjetas del dashboard repiten el sidebar y todas usan el mismo botón genérico "Open" | 1 | Usability: Reconocimiento antes que recuerdo / Diseño estético y minimalista | Todos |
| 19 | El buscador del header ("Search...") no comunica qué se puede buscar | 2 | Usability: Reconocimiento antes que recuerdo / Ayuda y documentación | Todos |
 
#### DESCRIPCIÓN DE PROBLEMAS 
##### 1. Landing Page
 
**PROBLEMA #1:** En vista móvil, el header del Landing Page no ofrece menú hamburguesa y los enlaces de navegación desaparecen
 
- **Severidad:** 3
- **Heurística violada:** Usability — Consistencia y estándares / Flexibilidad y eficiencia de uso
- **Plan afectado:** Todos
**Problema:**
En el ancho de 390 px, el header solo muestra el logo, el selector de idioma y los botones "Iniciar sesión" y "Regístrate". Los enlaces de navegación que sí aparecen en escritorio (Inicio, Nosotros, Beneficios, ¿Cómo funciona?, Preguntas frecuentes, Contacto) desaparecen y no existe un menú hamburguesa que los reemplace. El usuario móvil pierde el acceso directo a las secciones y solo puede recorrer la página haciendo scroll.
 
**Recomendación:**
Agregar un menú hamburguesa por debajo de un breakpoint definido (por ejemplo, < 768px) que agrupe los enlaces de navegación, el selector de idioma y los botones de acceso, manteniendo visible solo el logo y el botón de menú en la barra.

**PROBLEMA #2:** El selector de idioma EN/ES del Landing Page se ve como botones sin estilo, apilados y sin indicar el idioma activo
 
- **Severidad:** 2
- **Heurística violada:** Usability — Visibilidad del estado del sistema / Consistencia y estándares
- **Plan afectado:** Todos
**Problema:**
En el header del Landing Page, los botones "EN" y "ES" aparecen uno encima del otro con la apariencia de botones nativos del navegador, sin el estilo del resto de la interfaz. Ambos se ven iguales, por lo que el usuario no sabe cuál es el idioma activo. Dentro de la aplicación, en cambio, el selector es una píldora horizontal que resalta el idioma seleccionado, lo que rompe la coherencia entre ambos sitios.
 
**Recomendación:**
Rediseñar el selector como un control horizontal compacto que resalte el idioma activo y sea idéntico al de la Web Application, de modo que el usuario reconozca el mismo componente en todo el producto.
 
**PROBLEMA #3:** La sección "¿Cómo funciona?" es un único bloque de texto sin pasos y omite a los trabajadores
 
- **Severidad:** 2
- **Heurística violada:** Usability — Reconocimiento antes que recuerdo / Coincidencia entre el sistema y el mundo real
- **Plan afectado:** Todos
**Problema:**
La sección presenta una sola tarjeta titulada "Estudiantes y ciudadanos" con un párrafo que describe todo el recorrido (ubicar la estación, escanear el QR, viajar, estacionar y finalizar desde la app). Al ser un proceso secuencial, el usuario debe leer y recordar el orden en lugar de reconocerlo de un vistazo. Además, el título deja fuera a los trabajadores, aunque el formulario de contacto del mismo sitio sí los considera como tipo de usuario.
 
**Recomendación:**
Presentar el flujo como pasos numerados e iconografiados (1. Ubica una bicicleta, 2. Escanea el QR, 3. Viaja, 4. Estaciona y finaliza) y reemplazar el título por uno que cubra a todos los segmentos (estudiantes, trabajadores y ciudadanos).
 
**PROBLEMA #4:** Las tarjetas de beneficios son solo texto, sin íconos ni jerarquía visual
 
- **Severidad:** 1
- **Heurística violada:** Usability — Diseño estético y minimalista
- **Plan afectado:** Todos
**Problema:**
Los seis beneficios se muestran como tarjetas idénticas con un párrafo corto, sin ícono, título ni énfasis en la idea principal. Esto dificulta el escaneo rápido de la propuesta de valor, ya que ningún beneficio destaca sobre otro.
 
**Recomendación:**
Añadir un ícono y un título breve a cada tarjeta (por ejemplo, "Rápido", "Sostenible", "Tarifas claras") y reducir el párrafo a una línea de apoyo.
 
##### 2. Autenticación (Login y Registro)
 
**PROBLEMA #5:** En el login, el selector de idioma está dentro de la fila de "Forgot Password?" y "Remember me"
 
- **Severidad:** 2
- **Heurística violada:** Usability — Consistencia y estándares / Inclusive Design — Offer choice
- **Plan afectado:** Todos
**Problema:**
El selector EN/ES de la pantalla de login está colocado entre el enlace "Forgot Password?" y la casilla "Remember me", en la misma fila de acciones del formulario. Su ubicación no es la habitual (en el header o en una esquina de la pantalla) y puede confundirse con un control relacionado con la sesión o la contraseña, por lo que el usuario difícilmente lo encuentra a tiempo.
 
**Recomendación:**
Mover el selector a una zona fija y reconocible de la pantalla de autenticación (esquina superior) y mantener la misma posición en login y registro, separado de las acciones del formulario.
 
**PROBLEMA #6:** El registro no muestra requisitos de contraseña, no pide confirmarla y el teléfono no indica formato
 
- **Severidad:** 2
- **Heurística violada:** Usability — Prevención de errores / Ayuda y documentación
- **Plan afectado:** Todos
**Problema:**
El formulario de registro solicita correo, nombre de usuario, contraseña y teléfono, pero no informa los requisitos de la contraseña (longitud, caracteres) ni solicita repetirla para confirmar. El campo de teléfono tampoco indica el formato esperado ni el código de país. Esto facilita errores de tipeo en credenciales y datos de contacto que el usuario solo descubrirá cuando no pueda ingresar o ser contactado.
 
**Recomendación:**
Mostrar los requisitos de contraseña junto al campo con validación en tiempo real, agregar un campo de confirmación, y aplicar al teléfono un formato guiado (prefijo +51, tipo `tel` y máscara) con mensajes de error claros.
 
##### 3. Suscripción y Pago
 
**PROBLEMA #7:** La comparación de planes no muestra la tarifa del Plan Tarifa ni explica por qué se recomienda la Suscripción Pro
 
- **Severidad:** 2
- **Heurística violada:** Usability — Reconocimiento antes que recuerdo / Ayuda y documentación
- **Plan afectado:** Todos
**Problema:**
En la pantalla de planes, la Suscripción Pro muestra su precio (S/ 30.00 al mes) y se marca como "Recomendado", pero el Plan Tarifa solo dice "Pago por uso" sin indicar cuánto cuesta cada viaje o minuto. Sin ese dato el usuario no puede comparar y decidir si le conviene pagar S/ 30.00. Además, el gráfico "Actividad Semanal" no tiene escala ni valores por día, y no se explica que la recomendación se basa en esa actividad.
 
**Recomendación:**
Mostrar la tarifa concreta del Plan Tarifa (por viaje o por minuto), agregar una estimación como "Con tus 28 viajes semanales pagarías S/ X en Plan Tarifa vs. S/ 30.00 en Pro" y añadir valores al gráfico y una leyenda que justifique la etiqueta "Recomendado".
 
**PROBLEMA #8:** El formulario de pago expone el botón "Generar datos aleatorios"
 
- **Severidad:** 3
- **Heurística violada:** Usability — Prevención de errores / Coincidencia entre el sistema y el mundo real
- **Plan afectado:** Suscripción Pro
**Problema:**
En el formulario "Datos de la tarjeta" aparece un botón "Generar datos aleatorios" que parece una herramienta de pruebas del equipo de desarrollo. Para un usuario real no tiene sentido en un pago, genera dudas sobre la seriedad y seguridad del proceso y puede llevar a enviar datos falsos creyendo que son válidos.
 
**Recomendación:**
Retirar el botón de la versión visible al usuario o limitarlo a un entorno de desarrollo mediante una variable de configuración, de modo que el formulario de pago solo contenga los campos reales de la tarjeta.
 
**PROBLEMA #9:** El formulario de pago tiene etiquetas inconsistentes y no guía el formato de tarjeta y CVV
 
- **Severidad:** 2
- **Heurística violada:** Usability — Consistencia y estándares / Reconocimiento antes que recuerdo
- **Plan afectado:** Suscripción Pro
**Problema:**
Solo el campo de vencimiento tiene una etiqueta visible ("Fecha de vencimiento"); número de tarjeta, nombre del titular y CVV dependen únicamente de un placeholder que desaparece al escribir. Tampoco se aprecia ayuda sobre el formato esperado (grupos de dígitos, longitud del CVV), lo que obliga al usuario a recordar qué campo era cuál y aumenta la probabilidad de errores.
 
**Recomendación:**
Usar etiquetas persistentes sobre todos los campos, aplicar máscaras de formato (número en grupos de 4, vencimiento MM/AA, CVV de 3–4 dígitos), mostrar el tipo de tarjeta detectado y validar cada campo con mensajes claros.
 
##### 4. App — Flota y Estaciones (Bicicletas)
 
**PROBLEMA #10:** Las acciones de gestión de flota aparecen en el mismo menú del usuario sin distinción de rol
 
- **Severidad:** 3
- **Heurística violada:** Usability — Prevención de errores / Coincidencia entre el sistema y el mundo real
- **Plan afectado:** Todos
**Problema:**
El sidebar del usuario ("Usuario Demo") incluye la opción "Bicycles", que abre una tabla con el botón "New Bicycle" y acciones de editar y eliminar por cada unidad. Estas son funciones de administración de la flota mezcladas con las de un usuario final (My trips, Subscriptions, Report a problem). Un usuario común podría crear, modificar o eliminar bicicletas por error, y la interfaz no deja claro quién debería usar esa vista.
 
**Recomendación:**
Separar la experiencia por rol: mostrar la gestión de bicicletas solo a administradores o personal de mantenimiento, y ofrecer al usuario final una vista de solo lectura de bicicletas disponibles y estaciones cercanas.
 
**PROBLEMA #11:** La vista de bicicletas muestra textos de relleno ("Bicycles Title" / "Bicycles Subtitle")
 
- **Severidad:** 2
- **Heurística violada:** Usability — Coincidencia entre el sistema y el mundo real / Consistencia y estándares
- **Plan afectado:** Todos
**Problema:**
El encabezado de la tabla de bicicletas muestra literalmente "Bicycles Title" y "Bicycles Subtitle", que son textos provisionales. El usuario no recibe un título ni una descripción útil de lo que está viendo, y la pantalla transmite que el producto está inacabado, a diferencia de las demás vistas, que sí tienen títulos reales (por ejemplo, "Planes para Usuario Demo").
 
**Recomendación:**
Reemplazar los textos provisionales por un título y subtítulo reales (por ejemplo, "Flota de bicicletas" / "Gestiona las unidades registradas") y revisar que no queden otras claves o textos de prueba en la aplicación.
 
**PROBLEMA #12:** Las acciones de cada bicicleta son íconos sin etiqueta y la columna "Actions" queda lejos de ellos
 
- **Severidad:** 2
- **Heurística violada:** Usability — Reconocimiento antes que recuerdo
- **Plan afectado:** Todos
**Problema:**
Cada fila ofrece cinco íconos pequeños (candado, ubicación, actualizar, editar y eliminar) sin texto visible, y el encabezado "Actions" está a la izquierda mientras los íconos están al extremo derecho de la tabla. El usuario debe adivinar qué hace cada ícono, incluyendo el de eliminar, que está junto a acciones inocuas, con riesgo de pulsar el equivocado.
 
**Recomendación:**
Alinear el encabezado "Actions" con los íconos, agregar tooltips o etiquetas a cada acción, separar visualmente la acción destructiva (eliminar) y pedir confirmación antes de ejecutarla.
 
**PROBLEMA #13:** "Current Station" muestra un ID numérico y los códigos de bicicleta no siguen un mismo formato
 
- **Severidad:** 2
- **Heurística violada:** Usability — Coincidencia entre el sistema y el mundo real / Consistencia y estándares
- **Plan afectado:** Todos
**Problema:**
En la columna "Current Station" una bicicleta muestra "1" en lugar del nombre de una estación, mientras otras muestran "Unassigned". Además, los códigos de bicicleta mezclan formatos ("BGO-1042", "BGO-2000" y "B1"). El usuario no puede ubicar la bicicleta con un dato que no corresponde al lenguaje de la ciudad (nombres de estaciones) ni confiar en un código uniforme para identificarla.
 
**Recomendación:**
Mostrar el nombre de la estación (con enlace a su detalle) en lugar del ID, y estandarizar el formato del código de bicicleta con una validación al crearla.
 
##### 5. App — Perfil
 
**PROBLEMA #14:** La contraseña se edita en el mismo formulario del perfil, sin un flujo de cambio seguro
 
- **Severidad:** 3
- **Heurística violada:** Usability — Prevención de errores
- **Plan afectado:** Todos
**Problema:**
La pantalla "My Profile" muestra el campo de contraseña dentro del mismo formulario que correo, usuario, teléfono y locación, y todo se guarda con un único botón. Cambiar una credencial junto con datos generales, sin pedir la contraseña actual ni verificar la identidad, aumenta el riesgo de modificaciones accidentales o no autorizadas y compromete la seguridad de la cuenta.
 
**Recomendación:**
Quitar la contraseña del formulario general y ofrecer una acción separada "Cambiar contraseña" que pida la contraseña actual y la nueva con confirmación; solicitar verificación adicional cuando se cambie el correo.
 
**PROBLEMA #15:** La locación del perfil parece ser un campo de texto libre en lugar de una lista de opciones
 
- **Severidad:** 2
- **Heurística violada:** Usability — Prevención de errores / Consistencia y estándares
- **Plan afectado:** Todos
**Problema:**
El campo "Location" del perfil tiene el aspecto de una caja de texto igual a las demás (con el valor "Lima"), sin señales de selección como una flecha de desplegable. Si es texto libre, se permiten errores de tipeo y distintas formas de escribir un mismo distrito, lo que dificulta filtrar o agrupar por zona de operación (San Isidro, Miraflores, Surco).
 
**Recomendación:**
Reemplazar el campo por un dropdown o autocomplete con los distritos donde opera BiciGo, garantizando valores válidos y consistentes.

**PROBLEMA #16:** El perfil solo ofrece "Save changes", sin opción de cancelar o restablecer
 
- **Severidad:** 1
- **Heurística violada:** Usability — Control y libertad del usuario
- **Plan afectado:** Todos
**Problema:**
La única acción disponible en el formulario del perfil es "Save changes". Si el usuario modifica un dato por error no encuentra un botón para cancelar o restablecer los valores originales, y su única salida es abandonar la pantalla o corregir manualmente.
 
**Recomendación:**
Agregar un botón secundario "Cancelar" o "Restablecer", deshabilitar "Save changes" mientras no haya cambios y mostrar un mensaje de éxito tras guardar.
 
##### 6. App — Navegación General
 
**PROBLEMA #17:** La interfaz mezcla inglés y español aunque el idioma activo es EN

- **Severidad:** 3
- **Heurística violada:** Usability — Consistencia y estándares / Inclusive Design — Offer choice
- **Plan afectado:** Todos
**Problema:**
Con el selector en "EN", el sidebar, el dashboard, el perfil y la tabla de bicicletas están en inglés, mientras que las pantallas "Planes para Usuario Demo" y "Realiza tu pago" están completamente en español. En login y registro, el formulario está en inglés pero el eslogan del panel derecho ("Una nueva forma de llegar a tu destino") está en español, y en la tarjeta del Plan Tarifa se muestran juntos "Plan Actual" y "Current plan". El usuario no puede predecir en qué idioma encontrará cada pantalla y el selector de idioma pierde credibilidad.
 
**Recomendación:**
Centralizar todos los textos en los diccionarios de traducción (sin cadenas escritas directamente en los componentes), revisar cada pantalla en ambos idiomas y garantizar que el idioma elegido se mantenga en todo el flujo, incluidos planes, pagos y paneles de marca.
  
**PROBLEMA #18:** Las tarjetas del dashboard repiten el sidebar y todas usan el mismo botón genérico "Open"
 
- **Severidad:** 1
- **Heurística violada:** Usability — Reconocimiento antes que recuerdo / Diseño estético y minimalista
- **Plan afectado:** Todos
**Problema:**
El dashboard muestra cuatro tarjetas (My trips, Plans and subscriptions, Stations, Report a problem) que duplican las opciones del sidebar y cada una tiene un botón idéntico "Open". El texto del botón no dice qué ocurre al pulsarlo, y la pantalla no destaca información útil como un viaje activo o las bicicletas disponibles cerca. Además, la cuarta tarjeta queda sola en una segunda fila.

**Recomendación:**
Usar botones con acciones concretas ("Ver mis viajes", "Ver planes", "Ver estaciones", "Reportar problema") o hacer clicable la tarjeta completa, y priorizar en el dashboard información accionable (viaje en curso, estaciones cercanas, plan actual).
 
**PROBLEMA #19:** El buscador del header ("Search...") no comunica qué se puede buscar
 
- **Severidad:** 
- **Heurística violada:** Usability — Reconocimiento antes que recuerdo / Ayuda y documentación
- **Plan afectado:** Todos
**Problema:**
El header de la Web Application incluye un buscador con el placeholder genérico "Search...", sin indicar si busca estaciones, bicicletas, viajes u opciones del menú. El usuario debe adivinar su alcance, lo que reduce su utilidad y genera incertidumbre sobre el resultado esperado.
 
**Recomendación:**
Usar un placeholder descriptivo del ámbito de búsqueda (por ejemplo, "Buscar estaciones, bicicletas o viajes...") y mostrar sugerencias o categorías de resultados al escribir.
## 5.4. Video About-the-Product.

El video de presentación del producto biciGO resume la propuesta de valor, los principales flujos de la aplicación web y el estado de la implementación alcanzado durante los Sprints del proyecto.

- **Enlace:** [https://youtu.be/V5GNY8Vs4wA](https://youtu.be/V5GNY8Vs4wA)

![Portada del video About-the-Product de biciGO](URL_PENDIENTE_PORTADA)

*Figura: portada del video About-the-Product de biciGO.*