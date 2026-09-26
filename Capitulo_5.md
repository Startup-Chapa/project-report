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
| Entorno de Desarrollo | WebStorm | Entorno utilizado para editar y organizar los archivos del proyecto, trabajar con Git y desarrollar los componentes web de biciGO. | [https://www.jetbrains.com/webstorm/](https://www.jetbrains.com/webstorm/) |
| Control de Versiones | Git | Sistema utilizado para registrar cambios, trabajar mediante ramas y mantener el historial del proyecto. | [https://git-scm.com/](https://git-scm.com/) |
| Repositorio Remoto | GitHub | Plataforma utilizada para almacenar el proyecto y facilitar el trabajo colaborativo entre los integrantes. | [https://github.com/](https://github.com/) |
| Documentación | Markdown | Formato utilizado para redactar y mantener los capítulos del informe, tablas, enlaces, imágenes y demás documentación del proyecto bajo un enfoque Docs-as-Code. | [https://www.markdownguide.org/](https://www.markdownguide.org/) |
| Gestión Ágil | Trello | Herramienta utilizada para organizar el Sprint Backlog, distribuir tareas y dar seguimiento al avance del equipo durante el Sprint. | [https://trello.com/invite/b/6aac96a6ce176e2f9d496d31/ATTI96186798f26dde57c47e51ca96f0fff04FDD51DF/sprint-web-1](https://trello.com/invite/b/6aac96a6ce176e2f9d496d31/ATTI96186798f26dde57c47e51ca96f0fff04FDD51DF/sprint-web-1) |
| Gestión del Producto | Product Backlog | Permite organizar y priorizar las User Stories y Technical Stories que forman parte del desarrollo de biciGO. | [https://trello.com/invite/b/6aac96a6ce176e2f9d496d31/ATTI96186798f26dde57c47e51ca96f0fff04FDD51DF/sprint-web-1](https://trello.com/invite/b/6aac96a6ce176e2f9d496d31/ATTI96186798f26dde57c47e51ca96f0fff04FDD51DF/sprint-web-1) |

### 5.1.2. Source Code Management
Para el control de versiones y la organización ordenada del código de nuestro proyecto BiciGo, el equipo utiliza GitHub como plataforma principal. GitHub nos permite almacenar código fuente de la Landing Page, Front-End, Back-End llevar un registro histórico de cambios, colaborar de manera estructurada y garantizar trazabilidad durante todo el ciclo de desarrollo. Por ende, creamos la organización Minex-Organization, que incluye los siguientes repositorios:
| Solución  | Nombre del repositorio  |  Enlace  |
|---|---|---|
| report | bicigo-report  | https://github.com/Startup-Chapa/project-report |
| website  | bicigo-website  |  https://github.com/Startup-Chapa/Landing-Page |
| webapp  |  bicigo-webapp  |  |
| platform  | bicigo-platform   |  |

Nuestro equipo de trabajo ha adoptado el flujo GitFlow, basado en el artículo “A successful Git branching model” de Vincent Driessen. La organización del repositorio se estructura en dos ramas principales y permanentes: master, que contiene las versiones estables listas para entrega, y develop, que funciona como la rama de integración continua del desarrollo. A partir de la rama develop, se crean ramas de tipo feature siguiendo la nomenclatura feature/chapter-#-description, por ejemplo: feature/chapter-ii-interviews. Estas ramas permiten que cada miembro del equipo desarrolle funcionalidades o secciones específicas de manera aislada. En casos donde un integrante desarrolla un capítulo completo, se utiliza una convención como feature/chapter-#-content. Una vez finalizado el trabajo, estas ramas se integran nuevamente en develop, asegurando una consolidación ordenada de los avances.

Cuando el producto se aproxima a una fecha de entrega, se genera una rama release a partir de develop. En esta etapa se realizan ajustes menores, como corrección de errores o mejoras finales. Posteriormente, la rama release se fusiona tanto en master como en develop, garantizando que los cambios aplicados se mantengan en futuras iteraciones del proyecto. En cuanto a la gestión de versiones, se utiliza Semantic Versioning mediante ramas con el formato release/vX.Y.Z. Asimismo, las correcciones críticas se gestionan a través de ramas hotfix, con la nomenclatura hotfix/vX.Y.Z, permitiendo resolver errores urgentes directamente sobre la versión en producción.

Adicionalmente, el equipo aplica la convención Conventional Commits, la cual estandariza los mensajes de confirmación para mejorar la trazabilidad y comprensión de los cambios. Cada commit sigue una estructura clara, por ejemplo:

git commit -m "docs(chapter-#): add ..."

Este enfoque facilita la generación automática de historiales de cambios y permite mantener un registro organizado y semántico del desarrollo.

En síntesis, cada nueva funcionalidad se desarrolla en una rama feature, las versiones listas para entrega se gestionan mediante release branches, y las correcciones urgentes a través de hotfix branches. Todo ello, junto con el uso de Conventional Commits, asegura un flujo de trabajo estructurado, colaborativo y alineado con buenas prácticas para el desarrollo del proyecto BiciGo.

**Repositorio report**
![report-screenshoot](./Resources/chapter-images/chapter-5/report.png)


**Repositorio  website**
![landing-screenshoot](./Resources/chapter-images/chapter-5/landing.png)


**Repositorio webapp**
![frontend-screenshoot](./Resources/chapter-images/chapter-5/webapp.png)

**Repositorio platform**
![backend-screenshoot](./Resources/chapter-images/chapter-5/platform.png)

## 5.2. Landing Page, Services & Applications Implementation

### 5.2.1. Sprint 1

El Sprint 1 corresponde a la primera entrega del proyecto (AV1 – Sprint Review) y tiene como alcance la implementación y el despliegue de la primera versión del **Landing Page** de BiciGO. El Landing Page presenta el modelo de negocio y el propósito de la plataforma a los visitantes de los segmentos objetivo (ciudadanos urbanos que realizan trayectos cortos e instituciones que desean promover el uso de la bicicleta), y es el punto de entrada hacia las aplicaciones. Los Web Services y las Frontend Web Applications se implementarán en los siguientes Sprints, según el cronograma de entregas del curso.

#### 5.2.1.1. Sprint Planning 1

El Sprint Planning Meeting del Sprint 1 definió el objetivo del Sprint, las tareas necesarias para publicar la primera versión del Landing Page y la distribución del trabajo entre los integrantes de Chapa. Como insumos se utilizaron los artefactos de los capítulos anteriores: el Lean UX Canvas (Capítulo I), los segmentos objetivo, las User Personas, el wireframe y el mock-up del Landing Page (Capítulo IV) y la guía de estilos general y web (sección 4.1).

| Sprint # | Sprint 1 |
|---|---|
| **Sprint Planning Background** | |
| Prepared By | Aguirre Ramos, Eduardo Manuel |
| Attendees (to planning meeting) | Aguirre Ramos, Eduardo Manuel / Armestar Felipa, Adrian Andres / Ayllon Pauccar, Juan David / Franco del Carpio, José María / Velasquez Velasquez, Rodrigo |
| Sprint 0 Review Summary | No aplica. El Sprint 1 es el primer Sprint del proyecto. Antes de iniciarlo, el equipo completó la documentación de los Capítulos I al IV (Startup Profile, Requirements Elicitation, Requirements Specification y diseño del Landing Page) y creó los repositorios `project-report` y `Landing-Page`. |
| Sprint 0 Retrospective Summary | No aplica. El Sprint 1 es el primer Sprint del proyecto. |
| **Sprint Goal & User Stories** | |
| Sprint 1 Goal | *Our focus is on publishing the first deployed version of the BiciGO Landing Page, available in English and Latin American Spanish and responsive on mobile and desktop screens.*<br>*We believe it delivers a clear understanding of the service (mission, vision, benefits and how it works) and a direct way to get in touch with the team to urban citizens who make short trips and to institutions interested in promoting cycling.*<br>*This will be confirmed when the Landing Page is publicly reachable at its GitHub Pages URL, every section can be read on a 390 px and on a 1440 px wide screen without horizontal scrolling, and a visitor can switch the whole interface between English and Spanish.* |
| Sprint 1 Velocity | No aplica en Story Points. Las tareas del Sprint 1 no provienen de User Stories del Product Backlog (que describen funcionalidades de las aplicaciones), sino de tareas asociadas a las restricciones del Landing Page. El esfuerzo se planifica en horas: **76 horas** en total (ver Sprint Backlog 1). |
| Sum of Story Points | 0 |

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

Las tareas no derivan de User Stories del Product Backlog, ya que estas describen funcionalidades de las aplicaciones. Por ese motivo se registran como tareas adicionales asociadas a las restricciones del Landing Page (responsive design, i18n, accesibilidad, SEO, términos y condiciones, y despliegue). Cada tarea está estimada en un rango de 4 a 8 horas.

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
| --- | --- | --- | --- | --- |
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

![landing-hero-desktop](./Resources/chapter5/landing-hero-desktop.png)

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