# Capítulo VI: Product Implementation, Validation & Deployment

## 6.1 Software Configuration Management

Esta sección aborda de manera detallada la gestión de configuración del software, un componente clave en el desarrollo y mantenimiento de cualquier sistema tecnológico. Su propósito principal es asegurar la integridad y trazabilidad de todos los artefactos producidos a lo largo del ciclo de vida del software, permitiendo que el equipo de desarrollo pueda trabajar de manera coordinada y estructurada. A través de políticas claras de versionado, control de cambios, definición de entornos y procedimientos estandarizados, se garantiza que cada integrante tenga acceso a configuraciones consistentes y actualizadas. Además, se establecen mecanismos para documentar y validar las modificaciones realizadas, lo que reduce significativamente la posibilidad de errores o incompatibilidades en las etapas de integración y despliegue.

La correcta implementación de una estrategia de gestión de configuración no solo mejora la calidad del producto final, sino que también optimiza la colaboración entre equipos multidisciplinarios, agiliza la detección de problemas y fortalece la estabilidad del sistema en entornos de producción.

### 6.1.1 Software Development Environment Configuration

En esta sub-sección se describe la configuración técnica del entorno de desarrollo utilizado durante el proyecto. Se especifican las herramientas de software instaladas, sus versiones, rutas de acceso y cualquier dependencia necesaria para asegurar un entorno de trabajo homogéneo para todos los miembros del equipo. Esta documentación resulta esencial para prevenir discrepancias durante la ejecución de tareas, evitar conflictos entre versiones y facilitar la incorporación de nuevos integrantes al proyecto.

Asimismo, se detallan las configuraciones iniciales requeridas para compilar, ejecutar y probar el sistema, incluyendo ajustes en IDEs, variables de entorno, gestores de paquetes, y posibles contenedores o entornos virtualizados (como Docker). Este enfoque garantiza que el entorno de desarrollo se mantenga alineado con el entorno de producción, contribuyendo a una transición fluida entre etapas de desarrollo, pruebas y despliegue.



- **Visual Studio Code**: Editor de código utilizado para desarrollar la Landing Page. Su entorno ligero, personalizable y con soporte para múltiples lenguajes facilitó la colaboración entre desarrolladores y la implementación ágil de componentes web.

<div style="text-align: center;">
  <img src="../images/visualstudio.png" alt="Visual Studio Code" style="width:10%;"/>
</div>

- **HTML5**: Lenguaje de marcado base para estructurar el contenido de la Landing Page. Permitió organizar la información de forma semántica y accesible, mejorando la navegación y la experiencia del usuario.

<div style="text-align: center;">
  <img src="../images/html5.png" alt="HTML 5" style="width:10%;"/>
</div>

- **CSS3**: Utilizado para aplicar estilos visuales a la Landing Page. Ayudó a mantener una identidad gráfica coherente, responsiva y atractiva, lo cual es clave para captar la atención del usuario final.

<div style="text-align: center;">
  <img src="../images/css3.png" alt="CSS 3" style="width:10%;"/>
</div>

- **JavaScript**: Lenguaje que permitió incorporar lógica e interactividad a la Landing Page, como animaciones, validaciones y mejoras en la experiencia dinámica del usuario.

<div style="text-align: center;">
  <img src="../images/js.png" alt="JavaScript" style="width:10%;"/>
</div>

- **GitHub**: Plataforma de control de versiones que centralizó el código del proyecto. Facilitó el trabajo colaborativo del equipo, permitió el seguimiento de cambios y mejoró la trazabilidad del desarrollo.

<div style="text-align: center;">
  <img src="../images/github.png" alt="Github" style="width:10%;"/>
</div>

- **LucidChart**: Herramienta usada para crear diagramas de flujo, wireflows y modelos conceptuales. Contribuyó a la claridad en el diseño funcional y ayudó a definir la lógica de interacción entre pantallas y procesos.

<div style="text-align: center;">
  <img src="../images/lucidchart.png" alt="LucidChart" style="width:10%;"/>
</div>

- **Figma**: Plataforma de diseño colaborativo utilizada para la creación de wireframes y prototipos visuales de alta fidelidad. Permitió validar la interfaz gráfica con antelación y alinear al equipo de desarrollo con la visión de diseño.

<div style="text-align: center;">
  <img src="../images/figma.png" alt="Figma" style="width:10%;"/>
</div>

- **Android Studio**: Entorno de desarrollo para la aplicación móvil. Proporcionó las herramientas necesarias para programar, depurar, probar y empaquetar la app en dispositivos Android.

<div style="text-align: center;">
  <img src="../images/androidstudio.png" alt="CSS 3" style="width:10%;"/>
</div>

- **Kotlin**: Lenguaje de programación moderno utilizado para desarrollar la aplicación móvil. Su sintaxis clara y concisa mejoró la eficiencia del código y la productividad del equipo, alineándose con las mejores prácticas de desarrollo en Android.

<div style="text-align: center;">
  <img src="../images/kotilin.png" alt="Kotlin" style="width:10%;"/>
</div>

- **Trello**: Plataforma de gestión de tareas basada en tableros y tarjetas, utilizada para organizar y hacer seguimiento del progreso del equipo durante el desarrollo del proyecto. Facilitó la planificación de sprints, la asignación de responsabilidades y la visualización del avance en tiempo real, promoviendo una colaboración efectiva y una mejor administración del tiempo.

<div style="text-align: center;">
  <img src="../images/Trello.png" alt="Trello" style="width:10%;"/>
</div>


Cada una de estas herramientas fue seleccionada estratégicamente para cumplir con los objetivos del proyecto, asegurando una solución tecnológica robusta, escalable y centrada en la experiencia del usuario.

### 6.1.2 Source Code Management

**Repositorio de la Landing Page:**  
Durante el desarrollo de la Landing Page, utilizamos un repositorio centralizado en GitHub para almacenar y gestionar el código fuente del proyecto. Esto permitió el trabajo colaborativo, el control de versiones y la trazabilidad de cambios en el desarrollo.

**Implementación de GitFlow:**  
Para nuestra estrategia de gestión de versiones con Git, nos basamos en el modelo de ramificación propuesto en el artículo _“A successful Git branching model”_ de Vincent Driessen. Adoptamos el enfoque **GitFlow**, el cual proporciona una estructura clara y organizada para el desarrollo colaborativo, facilitando la integración y el mantenimiento del código.

- **Rama Principal (`main`)**: Contiene la versión estable en producción.  
- **Rama de Desarrollo (`develop`)**: Integra los últimos avances y funcionalidades en desarrollo. Actúa como entorno de integración continua.  
- **Rama de Lanzamiento (`release`)**: Utilizada para preparar una nueva versión del producto, permitiendo ajustes finales antes de su despliegue.  
  - Deriva de: `develop`  
  - Se fusiona con: `develop` y `main`  
- **Rama de Características (`feature`)**: Destinada al desarrollo de nuevas funcionalidades específicas del producto.  
  - Deriva de: `develop`  
  - Se fusiona con: `develop`  
- **Rama de Corrección Rápida (`hotfix`)**: Diseñada para aplicar soluciones urgentes a errores críticos detectados en producción.  
  - Deriva de: `main`  
  - Se fusiona con: `develop` y `main`  
- **Rama de Alcance (`scope`)**: Rama personalizada creada para gestionar desarrollos relacionados con un módulo o funcionalidad específica de gran tamaño o impacto. Su objetivo es permitir el aislamiento de tareas que abarquen múltiples ramas `feature`, mejorando la organización y facilitando su integración progresiva.  
  - Deriva de: `develop`  
  - Puede actuar como contenedor de varias `feature`  
  - Se fusiona con: `develop` o `release`, según el caso
  
<div style="text-align: center;">
  <img src="../images/gitflow.png" alt="Ejemplo ramas Gitflow" style="width:70%;"/>
</div>

**Conventional Commits:**  
Para mantener claridad y consistencia en los mensajes de confirmación (`commits`), adoptamos la convención **Conventional Commits**, la cual estandariza la estructura semántica de cada mensaje, permitiendo una mejor comprensión del historial de cambios y una posible automatización en la generación de changelogs.

**Tipos de mensajes utilizados:**

- `feat`: Incorporación de nuevas funcionalidades.
- `fix`: Corrección de errores o bugs.
- `docs`: Cambios relacionados con la documentación.
- `style`: Ajustes de formato sin impacto funcional.
- `refactor`: Reestructuración del código sin alterar su comportamiento.
- `test`: Adición o modificación de pruebas automatizadas.
- `chore`: Tareas de mantenimiento y configuraciones del entorno.
- `perf`: Mejoras orientadas al rendimiento del sistema.    

### 6.1.3 Source Code Style Guide & Conventions

Para garantizar un código legible, consistente y de fácil mantenimiento, se adoptaron las convenciones propuestas por Google en sus guías oficiales de estilo para HTML/CSS, JavaScript y Kotlin. La aplicación de estos lineamientos facilita el trabajo colaborativo, mejora la comprensión del código entre distintos desarrolladores y reduce significativamente la probabilidad de errores durante el desarrollo y mantenimiento del sistema.

#### Convenciones para HTML/CSS (Google HTML/CSS Style Guide)

Durante la implementación de la Landing Page, se aplicaron las siguientes buenas prácticas recomendadas:

- Declarar siempre el tipo de documento (`<!DOCTYPE html>`) al inicio.
- Usar minúsculas para los nombres de los elementos HTML (`<p>`, `<h1>`, `<section>`, etc.).
- Cerrar correctamente todos los elementos HTML (por ejemplo, `<p></p>`).
- Colocar entre comillas los valores de los atributos (por ejemplo, `<div class="container">`).
- Incluir los atributos `alt`, `width` y `height` en las imágenes para accesibilidad y rendimiento.
- Evitar líneas de código excesivamente largas para facilitar la lectura.
- No omitir el elemento `<title>` dentro del `<head>`.
- Incluir `meta tags` relevantes al inicio del documento, como codificación, viewport y descripciones.

Estas convenciones aseguran una estructura semántica clara y una mejor interpretación por parte de navegadores y motores de búsqueda, además de contribuir a una experiencia de usuario coherente.

#### Convenciones para JavaScript (Google JavaScript Style Guide)

Para el desarrollo de funcionalidades interactivas con JavaScript, se aplicaron las siguientes convenciones:

- Usar notación **camelCase** para nombrar variables y funciones (por ejemplo: `numberArray`, `calculateSum()`).
- Emplear **comillas simples** para definir cadenas de texto (`'Este es un string'`).
- Finalizar todas las sentencias con punto y coma (`;`) para evitar errores de interpretación.
- Evitar el uso de `var` para declarar variables, priorizando `let` o `const` según la necesidad de reasignación.

Estas prácticas ayudan a mantener un estilo uniforme en el código fuente y previenen errores comunes relacionados con el scope, la redeclaración de variables o la gestión de valores dinámicos.

#### Convenciones para Kotlin (Google Kotlin Style Guide)

En el desarrollo de la aplicación móvil, se utilizó **Android Studio** como entorno de desarrollo, y se siguieron las convenciones oficiales para Kotlin propuestas por Google, que permiten escribir código más limpio, expresivo y seguro. Las principales directrices aplicadas fueron:

- Usar **camelCase** para variables, funciones y nombres de métodos (`userName`, `getUserData()`).
- Declarar constantes con `val` y variables mutables con `var` solo cuando sea estrictamente necesario.
- Utilizar nombres significativos, claros y descriptivos para funciones y clases.
- Omitir el punto y coma (`;`) al final de las sentencias, dado que no es necesario en Kotlin.
- Aplicar sangrías de 4 espacios y mantener una estructura clara de bloques.
- Utilizar funciones de extensión, lambdas y expresiones funcionales donde sea apropiado, siguiendo el estilo idiomático de Kotlin.
- Dividir clases largas en archivos separados para mejorar la mantenibilidad y legibilidad del código.

Estas convenciones permitieron desarrollar una aplicación Android robusta, con código fácilmente entendible y adaptable por cualquier miembro del equipo. Además, se favoreció el uso de buenas prácticas modernas en el entorno Android, alineándose con los estándares actuales de la industria.

La aplicación sistemática de estas convenciones fortaleció la calidad del código entregado en todas las capas del proyecto, promoviendo la claridad, la eficiencia y la colaboración efectiva entre los integrantes del equipo.

### 6.1.4 Software Deployment Configuration

Para el despliegue de la Landing Page del proyecto, se utilizó **GitHub Pages**, una plataforma gratuita que permite publicar sitios web estáticos directamente desde un repositorio de GitHub. Esta herramienta facilitó la publicación rápida y eficiente del contenido web desarrollado en HTML, CSS y JavaScript, sin necesidad de utilizar servidores adicionales ni configuraciones complejas.

El proceso de despliegue se realizó vinculando el repositorio del proyecto con GitHub Pages, configurando la rama correspondiente y asegurando que el contenido de la carpeta raíz (o `/docs`, según el caso) contuviera todos los archivos necesarios para el funcionamiento del sitio.

**Enlace de la Landing Page:**  
🔗 [https://1acc0238-2510-346-g3-eazylogistics.github.io/LandingPage/](https://1acc0238-2510-346-g3-eazylogistics.github.io/LandingPage/)

Este enlace corresponde a la versión publicada de la Landing Page, accesible desde cualquier dispositivo con conexión a internet, permitiendo validar su funcionamiento y presentación visual.

#### Configuración del Despliegue

<div style="text-align: center;">
  <img src="../images/landing_page_repository.png" alt="Inicio de Repositorio" style="width:70%;"/>
</div>

<div style="text-align: center;">
  <img src="../images/github_pages_configuration.png" alt="Configuracion de Deploy" style="width:70%;"/>
</div>

<div style="text-align: center;">
  <img src="../images/Deploy Github.png" alt="Github Pages Configuration" style="width:70%;"/>
</div>

- Selección de rama (`main`).
- Ubicación del contenido (`root`).
- Confirmación del estado en la pestaña **Pages** del repositorio.
- Mensajes de confirmación de despliegue exitoso.

#### Resultado del Despliegue

<div style="text-align: center;">
  <img src="../images/Landing Face.png" alt="Evidencia del Deploy" style="width:70%;"/>
</div>

Este despliegue permitió contar con una presentación web funcional del producto desde las primeras etapas del desarrollo, facilitando su validación por parte de usuarios, stakeholders y evaluadores.


## 6.2 Landing Page & Mobile Application Implementation
En esta sección se detalla el proceso completo de implementación, pruebas, documentación y despliegue de la Landing Page, los Web Services y las Aplicaciones Móviles. Abarca desde la planificación inicial hasta la entrega final, asegurando que cada componente cumpla con los requisitos establecidos y funcione correctamente.

## 6.2.1 Sprint 1
En esta sección se registra y explica el avance en términos de producto y trabajo colaborativo para el Sprint 1. Durante este sprint, el equipo se enfocará en la implementación de la Landing Page, asegurando que cumpla con los requisitos establecidos y funcione correctamente.

### 6.2.1.1 Sprint Planning 1  
En esta sección se especifican los aspectos principales del Sprint Planning Meeting. Este encuentro es fundamental para definir los objetivos y tareas del Sprint 1, asegurando que todos los miembros del equipo estén alineados y preparados para comenzar el trabajo. A continuación, se presenta un cuadro resumen del Sprint Planning Meeting, que incluye los puntos clave discutidos y las decisiones tomadas.

| **Sprint #**                       | Sprint 1                                                                                                                                                                                                                                                                                                                           | 
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sprint Planning Background**     |                                                                                                                                                                                                                                                                                                                                    |
| Date:                              | 2025/05/10                                                                                                                                                                                                                                                                                                                         |
| Time:                              | 5:00 PM                                                                                                                                                                                                                                                                                                                            |
| Location:                          | Reunión virtual via Discord                                                                                                                                                                                                                                                                                                        |
| Prepared by:                       | Gabriel Braithuaite, Mathias Vasquez                                                                                                                                                                                                                                                                                               |
| Attendees (to planning meeting):   | Gabriel Braithuaite, Mathias Vasquez, Joaquin Pedraza, Jose Luza, Fabian Reyes                                                                                                                                                                                                                                                     |
| Sprint n – 1 Review Summary        | No aplica para Sprint 1                                                                                                                                                                                                                                                                                                            |
| Sprint n – 1 Retrospective Summary | No aplica para Sprint 1                                                                                                                                                                                                                                                                                                            |
| **Sprint Goal & User Stories**     |                                                                                                                                                                                                                                                                                                                                    | 
| Sprint 1 Goal                      | **Our focus is** on developing and implementing a functional and attractive Landing Page. <br> **We believe it delivers** a positive first impression and attracts potential users to explore more about our product. <br> **This will be confirmed when** the Landing Page is deployed and receives positive feedback from users. |
| Sprint 1 Velocity                  | Para este sprint 1, el equipo de EazyLogistics puede aceptar 18 Story Points, los cuales son abarcados en las User Stories de la primera EPIC.                                                                                                                                                                                     |
| Sum of Story Points                | 18                                                                                                                                                                                                                                                                                                                                 |

### 6.2.1.2 Sprint Backlog 1  
En esta sección se presenta el Sprint Backlog del Sprint 1, que incluye las tareas y actividades planificadas para el desarrollo de la Landing Page. Cada tarea está asociada a una User Story específica, lo que permite al equipo realizar un seguimiento del progreso y asegurarse de que se cumplan los objetivos del sprint.

Screenshot del Sprint Backlog del Sprint 1 en Trello: https://trello.com/b/xzXIrtZu/eazylogistics

| **Sprint #** | Sprint 1                                     |                |                                                                               |                                                                                                                                                                                                    |                       |              |        |
|--------------|----------------------------------------------|----------------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|--------------|--------|
| User Story   |                                              | Work Item/Task |                                                                               |                                                                                                                                                                                                    |                       |              |        |
| Id           | Title                                        | Id             | Title                                                                         | Description                                                                                                                                                                                        | Estimation<br>(Hours) | Assined To   | Status |
| US001        | Acceso a la sección de Resumen	              | WI001          | Implementación de acceso a la sección de Resumen                              | Desarrollar y configurar la sección de información de la página de resumen para que los visitantes puedan acceder fácilmente y obtener información clara sobre la aplicación.                      | 1 hora                | Fabian Reyes | Done   |
| US002        | Acceso a la sección de Características	      | WI002          | Implementación de acceso a la sección de Características                      | Desarrollar y configurar la página de "Características" para que los visitantes puedan acceder fácilmente y enterarse de las características claves de la aplicación.                              | 1 hora                | Fabian Reyes | Done   | 
| US003        | Envío de Correos a los CEO de Easylogistics  | WI003          | Implementación de envío de correos a los CEO de Easylogistics                 | Desarrollar y configurar la funcionalidad que permita a los visitantes enviar correos con información adicional sobre las funcionalidades de la aplicación a los CEO de Easylogistics.             | 1 hora                | Fabian Reyes | Done   |
| US004        | Registro de Nuevos Usuarios                  | WI004          | Implementación de registro de nuevos usuarios                                 | Desarrollar y configurar la funcionalidad que permita a los visitantes registrarse como usuarios para ponerse en contacto y utilizar la aplicación.                                                | 1 hora                | Fabian Reyes | Done   |
| US005        | Información de Funcionalidades               | WI005          | Implementación de la sección de Información de Funcionalidades                | Desarrollar y configurar un sector en la página que detalle todas las funcionalidades que ofrece la aplicación.                                                                                    | 1 hora                | Fabian Reyes | Done   |
| US006        | Sector de Planes Disponibles                 | WI006          | Implementación del sector de Planes Disponibles                               | Desarrollar y configurar un sector en la página que muestre los diferentes planes que ofrece la aplicación, permitiendo a los visitantes escoger el que mejor se adapte a sus necesidades.         | 1 hora                | Fabian Reyes | Done   |
| US007        | Sector de Preguntas Frecuentes               | WI007          | Implementación del sector de Preguntas Frecuentes                             | Desarrollar y configurar un sector en la página que permita a los visitantes acceder a preguntas frecuentes y obtener respuestas rápidas a dudas comunes.                                          | 1 hora                | Fabian Reyes | Done   |
| US008        | 	Conexión de Easylogistics con la Aplicación | WI008          | Implementación de la sección de Conexión de Easylogistics con LogisticsMaster | Desarrollar y configurar una sección en la página que explique cómo Easylogistics está conectado con la aplicación, proporcionando a los visitantes una comprensión clara de su propósito y origen | 1 hora                | Fabian Reyes | Done   |

### 6.2.1.3 Development Evidence for Sprint Review  
En esta sección se explican y presentan los avances en la implementación de los productos de la solución según el alcance del Sprint 1. Durante este sprint, el equipo se ha enfocado en la creación y despliegue de la Landing Page

| Repository             | Branch | Commit Id | Commit Message       | Commit Message Body                                                     | Commited on (Date) |
|------------------------|--------|-----------|----------------------|-------------------------------------------------------------------------|--------------------|
| FabianTG25/LandingPage | main   | 2511ded   | Add files via upload | Se implementó la Landing Page con todas las funcionalidades requeridas. | 2025/05/14         |

Enlace al repositorio: https://github.com/1ACC0238-2510-346-G3-EazyLogistics/LandingPage

### 6.2.1.4 Testing Suite Evidence for Sprint Review  
Para este sprint, no se han realizado pruebas automatizadas, ya que el equipo ha decidido enfocarse en la implementación de la Landing Page y no se han desarrollado pruebas unitarias o de integración. Sin embargo, se han realizado pruebas manuales para asegurar que la Landing Page funcione correctamente y cumpla con los requisitos establecidos.
Se podrían implementar pruebas automatizadas utilizando herramientas como Selenium en futuros sprints, pero por el momento, el equipo ha optado por realizar pruebas manuales para asegurar la calidad del producto.

### 6.2.1.5 Execution Evidence for Sprint Review  
En este Sprint 1, el equipo ha desarrollado y desplegado la Landing Page, asegurando que cumpla con los requisitos establecidos y funcione correctamente. A continuación, se presentan las evidencias de ejecución del Sprint 1, que incluyen capturas de pantalla y descripciones de las funcionalidades implementadas.

<br>**Hero Section**: La sección principal de la Landing Page, que incluye una barra de navegación, un título
atractivo, una imagen llamativa y un botón de llamada a la acción.
<br> ![Landing Page Access](../images/landing_page_access.png)
<br>**About Section**: La sección que proporciona información sobre la aplicación y sus características principales.
Incluye un título, una descripción y una imagen representativa. Además, tiene uan sección sobre el equipo de
desarrollo.
<br> ![Landing Page About Section](../images/landing_page_about_section.png)
<br> ![Landing Page About Team Section](../images/landing_page_about_team_section.png)
<br>**Subscriptions Section**: La sección que muestra los diferentes planes de suscripción disponibles para los
usuarios. Incluye un título, una descripción y nuestros dos planes con precios y características.
<br> ![Landing Page Subscriptions Section](../images/landing_page_subscriptions_section.png)
<br>**Customers Section**: La sección que muestra los clientes actuales de la aplicación. Incluye un título y una
descripción de nuestros dos segmentos objetivos.
<br> ![Landing Page Customers Section](../images/landing_page_customers_section.png)
<br>**Contact Section**: La sección que permite a los usuarios ponerse en contacto con el equipo de desarrollo.
Incluye un formulario de contacto con campos para el nombre, correo electrónico y mensaje.
<br> ![Landing Page Contact Section](../images/landing_page_contact_section.png)
<br>**Footer Section**: La sección que incluye un aviso de derechos de autor.
<br> ![Landing Page Footer Section](../images/landing_page_footer_section.png)

### 6.2.1.6 Services Documentation Evidence for Sprint Review  
Este sprint 1 tuvo como enfoque principal la implementación de la Landing Page, por lo que no se han desarrollado Web Services. La documentación de Endpoints con OpenAPI y los detalles relacionados con Web Services serán relevantes en sprints futuros cuando se aborde la implementación y documentación de estos servicios. 

### 6.2.1.7 Software Deployment Evidence for Sprint Review  
En este Sprint 1, el equipo ha desplegado la Landing Page utilizando github pages. A continuación, se presentan las evidencias de despliegue del Sprint 1, que incluyen capturas de pantalla y pasos detallados del proceso de despliegue.
1. **Creación del Repositorio**: Se creó un repositorio en GitHub para alojar el código de la Landing Page. El repositorio se llama "LandingPage" y está disponible en la cuenta de GitHub del equipo.
<br> ![Landing Page Repository](../images/landing_page_repository.png)
<br> url del repositorio: https://github.com/1ACC0238-2510-346-G3-EazyLogistics/LandingPage

2. **Configuración de GitHub Pages**: Se habilitó la opción de GitHub Pages en la configuración del repositorio. Esto permite que el contenido del repositorio se publique como una página web estática.
<br> ![GitHub Pages Configuration](../images/github_pages_configuration.png)

3. **Despliegue de la Landing Page**: Se subió el código HTML, CSS y JavaScript de la Landing Page al repositorio. GitHub Pages generó automáticamente una URL para acceder a la página.
<br> ![Landing Page Deployment](../images/landing_page_deployment.png)

4. **Acceso a la Landing Page**: La Landing Page se puede acceder a través de la URL proporcionada por GitHub Pages. Esta URL es pública y permite que cualquier persona acceda a la página.
<br> url de la landing page: https://1acc0238-2510-346-g3-eazylogistics.github.io/LandingPage/
5. **Evidencia del Despliegue**: Se realizó una captura de pantalla de la Landing Page desplegada para mostrar su apariencia y funcionalidad.
![Landing Page Deployment Evidence](../images/landing_page_deployed.png)

### 6.2.1.8 Team Collaboration Insights during Sprint  
Para el desarrollo de este sprint, el equipo designó a un integrante para el desarrollo de las actividades de implementación de la Landing Page.

GitHub insights del landing page:

![GitHub Insights](../images/github_insights.png)

## 6.3 Validation Interviews  
### 6.3.1 Diseño de Entrevistas  
## 1. Preguntas para Gestores de Empresas Hoteleras

#### 1.1 Información Demográfica

| **Categoría**                   | **Preguntas**                                                                                                                               |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Edad y género**               | - ¿Podrías indicarme tu edad y género?                                                                                                      |
|                                 | - ¿Consideras que tu perfil demográfico influye en tu familiaridad o preferencias al usar plataformas de gestión?                            |
| **Ubicación del hotel**         | - ¿En qué ciudad o región se encuentra tu hotel?                                                                                            |
|                                 | - ¿Tu ubicación influye en la necesidad de interacción digital con los huéspedes?                                                           |
| **Experiencia en el sector hotelero** | - ¿Cuántos años de experiencia tienes en la gestión hotelera?                                                                       |
|                                 | - ¿Qué cambios o actualizaciones esperas en plataformas de gestión con base en tu experiencia?                                              |

#### 1.2 Evaluación del Landing Page y Aplicaciones

| **Categoría**                   | **Preguntas**                                                                                                                               |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Navegación y facilidad de uso** | - ¿Qué tan fácil encontraste navegar en el landing page y la aplicación de Logistic Master?                                                   |
|                                 | - ¿Hubo alguna sección que te costara trabajo localizar o entender?                                                                        |
| **Funcionalidades clave**       | - ¿Qué características te parecen útiles en la gestión hotelera?                                                                           |
|                                 | - ¿Qué opinas de la funcionalidad de notificaciones push en la plataforma?                                                                  |
| **Eficiencia en la gestión**    | - ¿Crees que la plataforma te facilita la gestión de tu hotel de manera eficiente?                                                         |
|                                 | - ¿Hay alguna funcionalidad que agregarías o mejorarías para adaptarla mejor a tus necesidades?                                            |

### 2. Preguntas para Huéspedes

#### 2.1 Información Demográfica

| **Categoría**                   | **Preguntas**                                                                                                                               |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Edad y género**               | - ¿Podrías indicarme tu edad y género?                                                                                                      |
|                                 | - ¿Te sientes cómodo usando plataformas digitales para hacer reservas y recibir notificaciones?                                             |
| **Distrito de residencia**      | - ¿En qué distrito o ciudad resides actualmente?                                                                                            |
|                                 | - ¿Prefieres reservar en lugares cercanos a tu residencia o explorar destinos nuevos?                                                       |
| **Ocupación**                   | - ¿Cuál es tu ocupación actual?                                                                                                             |
|                                 | - ¿Crees que tu ocupación influye en la frecuencia o tipo de reservas que realizas?                                                         |

#### 2.2 Evaluación del Landing Page y Aplicaciones

| **Categoría**                   | **Preguntas**                                                                                                                               |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Interacción inicial**         | - ¿Fue fácil encontrar la información en el landing page y entender de qué trata Logistic Master?                                              |
|                                 | - ¿Tuviste problemas para registrarte o iniciar sesión en la aplicación?                                                                    |
| **Preferencias y expectativas** | - ¿Qué funcionalidades de la plataforma te resultaron más útiles para hacer reservas?                                                      |
|                                 | - ¿Te gustaría recibir más información personalizada o notificaciones sobre servicios disponibles en los hoteles?                          |
| **Experiencia de reserva**      | - ¿El flujo de reserva te pareció intuitivo? ¿Hubo algún paso que te generara dudas o frustración?                                         |
|                                 | - ¿Qué cambios sugerirías para mejorar la experiencia de reserva en la plataforma?                                                         |

### Conclusión de la Entrevista

| **Categoría**                   | **Pregunta**                                                                                                                                |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Pregunta Final**              | - ¿Hay algo más que consideres relevante compartir sobre tu experiencia interactuando con la plataforma y realizando reservas?             |


### 6.3.2 Registro de Entrevistas  
| **Datos del entrevistado** | 
|--------------------------|
| **Nombre:**  Roberto Franco |
| **Link del video:**   |
| **Edad:**  31 años |
| **Procedencia:**  Lima, San Isidro |
| ![Entrevista]()|
| **Resumen:** Roberto Franco es un gestor de hotel en San Isidro, Lima, con cinco años de experiencia en la industria hotelera. Ella administra las reservas directamente en el sistema del hotel y le da mucha importancia a aspectos como el precio, la ubicación y las opiniones de los huéspedes. Aunque se siente cómodo gestionando reservas desde su smartphone, sugiere que las plataformas de reservas hoteleras deberían incluir más opciones de personalización, enviar recordatorios automáticos y ofrecer mayor claridad en las tarifas adicionales. Además, considera esencial recibir notificaciones y tener la opción de comunicarse directamente con los clientes a través de la plataforma. |
#### Entrevista 2
| **Datos del entrevistado** | 
|--------------------------|
| **Nombre:**  Ramiro Guzman |
| **Link del video:**  https://drive.google.com/file/d/1uW_-4YnXXOg0ApA_ywYjW2uUettpJj5H/view?usp=sharing |
| **Edad:**  31 años |
| **Procedencia:**  Lima, San Isidro |
| ![Entrevista]()|
| **Resumen:** Gracie Romero es un gestor de hotel en San Isidro, Lima, con cinco años de experiencia en la industria hotelera. Ella administra las reservas directamente en el sistema del hotel y le da mucha importancia a aspectos como el precio, la ubicación y las opiniones de los huéspedes. Aunque se siente cómodo gestionando reservas desde su smartphone, sugiere que las plataformas de reservas hoteleras deberían incluir más opciones de personalización, enviar recordatorios automáticos y ofrecer mayor claridad en las tarifas adicionales. Además, considera esencial recibir notificaciones y tener la opción de comunicarse directamente con los clientes a través de la plataforma. |

#### Entrevista 3
| **Datos del entrevistado** | 
|--------------------------|
| **Nombre:**  Robert  |
| **Link del video:**  https://drive.google.com/file/d/1JdN6SU5CO-x4ZKly1RK6HmJvodzBH_jP/view?usp=sharing |
| **Edad:**  19 años |
| **Procedencia:**  Lima, San Miguel |
| ![Entrevista]()|
| **Resumen:** Sebastian Mendez es un gestor de hotel en Lima con 3 años de experiencia en el sector. Maneja las reservas directamente en el sistema del hotel y considera esenciales factores como el precio, la ubicación y los comentarios de los huéspedes. Sugiere que las aplicaciones de reservas deberían ser más visuales, ofreciendo opciones de personalización, recordatorios automáticos y mayor claridad en los cargos adicionales. Para él, es crucial recibir notificaciones y tener la opción de comunicarse de forma directa con los clientes a través de la plataforma. |

## Segmento de huespedes

#### Entrevista 1
| **Datos del entrevistado** | 
|--------------------------|
| **Nombre:**  Jose Shuan https://drive.google.com/file/d/12Gblup5lzNwCtT7oSoEso5_v_I2aiBNs/view?usp=sharing  |
| **Link del video:** |
| **Edad:**  24 años |
| **Procedencia:**  Lima, Callao |
| ![Entrevista]()|
| **Resumen:** Jose Shuan, un estudiante universitario de 24 años que reside en San Miguel, Lima, realiza la mayoría de sus reservas entre los 18 y 20 años, principalmente le gusta  hacer reservas a destinos nuevos , valorando el precio, la ubicación y las opiniones de otros usuarios. Se siente cómodo Logistic Master para realizar reservas, pero sugiere que nuestra plataforma  debería implementar mas facilidad a la hora de completar información detallada  acerca de su reserva. |

#### Entrevista 2
| **Datos del entrevistado** | 
|--------------------------|
| **Nombre:**  Lopez Diaz Gael Dario |
| **Link del video:**  https://drive.google.com/file/d/1fjwcqRZr4tD8PcLi_KTUrOpeGgFO1eLM/view?usp=sharing |
| **Edad:**  20 años |
| **Procedencia:**  Lima, San Miguel |
| ![Entrevista]()|
| **Resumen:** Gael, un estudiante universitario de 19 años que reside en San Miguel, Lima, realiza la mayoría de sus reservas entre los 18 y 20 años, principalmente le gusta  hacer reservas a destinos nuevos pero si no cuenta con mucho tiempo por la universidad prefiere cercanos  , valorando el precio, la ubicación y las opiniones de otros usuarios. Se siente cómodo usando KingReserve para realizar reservas, pero sugiere que nuestra plataforma  debería implementar mas facilidad a la hora de completar información detallada  acerca de su reserva . |

#### Entrevista 3
| **Datos del entrevistado** | 
|--------------------------|
| **Nombre:**  Marcel |
| **Link del video:** https://drive.google.com/file/d/1u0U2Ig1vQRH0oIEyu0Gsy4a9WKeeG95L/view?usp=sharing |
| **Edad:**  24 años |
| **Procedencia:**  Lima, San Miguel |
| ![Entrevista]()|
| **Resumen:** Gael, un estudiante universitario de 24 años que reside en Callao, Lima, realiza la mayoría de sus reservas entre los 18 y 20 años, principalmente le gusta  hacer reservas a destinos nuevos pero si no cuenta con mucho tiempo por la universidad prefiere cercanos  , valorando el precio, la ubicación y las opiniones de otros usuarios. Se siente cómodo usando Logistic Master para realizar reservas, pero sugiere que nuestra plataforma  debería implementar mas facilidad a la hora de completar información detallada  acerca de su reserva . |

### 6.3.3 Evaluaciones según heurísticas  
###Problemas detectados:

No parece haber suficientes notificaciones sobre el estado de las reservas
Los gestores de hotel mencionan la necesidad de recibir notificaciones automáticas
Falta de confirmación visual durante el proceso de reserva

###Recomendaciones:

Implementar un sistema de notificaciones en tiempo real sobre cambios en reservas
Mostrar indicadores claros del progreso durante el proceso de reserva
Incluir confirmaciones visuales cuando se completen acciones importantes

###2. Coincidencia entre el sistema y el mundo real
Problemas detectados:

Posible uso de terminología hotelera técnica no familiar para usuarios comunes
Falta de elementos visuales que representen conceptos hoteleros

Recomendaciones:

Utilizar un lenguaje claro y sencillo, evitando jerga técnica
Implementar iconografía intuitiva que represente conceptos hoteleros
Organizar la información siguiendo una lógica natural para los usuarios

3. Control y libertad del usuario
Problemas detectados:

Limitadas opciones de personalización mencionadas por los gestores
Posibles dificultades para editar o cancelar reservas ya realizadas

Recomendaciones:

Añadir opciones claras para deshacer acciones o volver atrás en el proceso
Implementar más opciones de personalización como sugieren los gestores
Facilitar la modificación o cancelación de reservas con procesos simples

## 6.4 Video About-the-Product
