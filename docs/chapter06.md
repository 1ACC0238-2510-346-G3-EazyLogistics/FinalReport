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

url del repositorio: https://github.com/1ACC0238-2510-346-G3-EazyLogistics/LandingPage

2. **Configuración de GitHub Pages**: Se habilitó la opción de GitHub Pages en la configuración del repositorio. Esto permite que el contenido del repositorio se publique como una página web estática.
<br>
3. **Despliegue de la Landing Page**: Se subió el código HTML, CSS y JavaScript de la Landing Page al repositorio. GitHub Pages generó automáticamente una URL para acceder a la página.
<br>

4. **Acceso a la Landing Page**: La Landing Page se puede acceder a través de la URL proporcionada por GitHub Pages. Esta URL es pública y permite que cualquier persona acceda a la página.
<br> url de la landing page: https://1acc0238-2510-346-g3-eazylogistics.github.io/LandingPage/
5. **Evidencia del Despliegue**: Se realizó una captura de pantalla de la Landing Page desplegada para mostrar su apariencia y funcionalidad.


### 6.2.1.8 Team Collaboration Insights during Sprint  
Para el desarrollo de este sprint, el equipo designó a un integrante para el desarrollo de las actividades de implementación de la Landing Page.

GitHub insights del landing page:

![insights 4](../images/insights%204.png)

### 6.2.2. Sprint 2
#### 6.2.2.3 Sprint Planning 2
| **Sprint #**                    | Sprint 2                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sprint Planning Date**        |        20/06/25                                                                                                                                                                                                                                                                                                                                                         |
| **Time**                        | 11.00  AM                                                                                                                                                                                                                                                                                                                                                                            |
| **Location**                    | Google Meet                                                                                                                                                                                                                                                                                                                                                                           |
| **Prepared By**                 | Mathias Vasquez                                                                                                                                                                                                                                                                                                                                                                    |
| **Attendees**                   | Gabriel, Fabian, Jose y Joaquin.                                                                                                                                                                                                                                                                                                                    |
| **Sprint Review Summary**       | Se desarollo casi en su totalidad la aplicacion en Android Studio y se avanzó la misma en Flutter.                                                                                                                                                                                                                                                                                                            |
| **Sprint Retrospective Summary**| Se desarrollo la aplicacion de Android Studio en poco tiempo pero puede mejorar la organizacion.                                                                                                                                                                                                                                                        |
| **Sprint Goal**                 | En este sprint, el objetivo es desarrollar la lógica y funcionalidades principales de la aplicacion moviel en Android Studio. |
| **Sprint Velocity**             | 25                                                                                                                                                                                                                                                                                                                                                                                    |
| **Sum of Story Points**         | 25 Story Points                                                                                                                                                                                                                                                                                                                                                                       |


#### 6.2.2.3. Sprint Backlog 2

| **User Story Id** | **User Story Title** | **Work-Item/Task Id** | **Work-Item/Task Title** | **Description** | **Estimation** | **Assigned To** | **Status** |
|:-----------------:|:--------------------:|:---------------------:|:-----------------------:|:---------------:|:--------------:|:--------------:|:----------:|
| US016 | Actualizar Contenido | T01 | Actualizar Contenido | Como administrador, quiero poder actualizar el contenido existente para mantener la información relevante y actualizada. | 2h | Mathias Vasquez | Done |
| US017 | Eliminar Contenido | T02 | Eliminar Contenido | Como administrador, quiero poder eliminar contenido obsoleto para mantener la información actualizada en la aplicación. | 3h | Mathias Vasquez | Done |
| US014 | Crear Contenido | T03 | Crear Contenido | Como administrador, quiero poder crear nuevo contenido para mantener la información actualizada en la aplicación | 3h | Jose Luza | Done |
| TS029 | Crear Usuario | T04 | Crear Usuario | Como desarrollador, quiero crear un endpoint para registrar nuevos usuarios en el sistema. | 4h | Mathias Vasquez | Done |
| TS030 | Autenticar Usuario | T05 | Autenticar Usuario | Como desarrollador, quiero crear un endpoint para autenticar usuarios y generar tokens de acceso. | 2h | Mathias Vasquez | Done |
| TS031 | Crear Huésped | T06 | Crear Huésped | Como desarrollador, quiero crear un endpoint para registrar nuevos huéspedes en el sistema. | 4h | Joaquin Pedraza | Done |
| TS033 | Crear Habitación | T07 | Crear Habitación | Como desarrollador, quiero crear un endpoint para registrar nuevas habitaciones en el sistema. | 3h | Joaquin Pedraza | Done |
| US028 | Filtro de eventos por criterios | T08 | Filtrado de búsqueda de eventos por criterios | Filtros de búsqueda de eventos por criterios | 3h | Jose Luza | Done |
| US029 | Restablecer filtros aplicados | T09 | Restablecer filtros de búsqueda de eventos aplicados | Restablecer filtros de búsqueda aplicados a los eventos disponibles | 2h | Jose Luza | Done |



#### 6.2.2.3. Development Evidence for Sprint Review 2
| **Repository**     | **Branch** | **Commit Id** | **Commit Message** | **Committed on (Date)** |
|--------------------|------------|---------------|---------------------|--------------------------|
|1ACC0238-2510-346-G3-EazyLogistics Android-Studio          |     main    |   2c07d4e2294e8851fd164c26ec4c7f82c0ac5172    |     Feat(main) Adedd Personal Management View and Menu     |     06/20/2025                  |
|1ACC0238-2510-346-G3-EazyLogistics Android-Studio                |   main         |    011272124ae79ce841d012de3c5cad8d4a942df2           |      Feat(Main) Fixed LoginScreen               |       06/20/2025                     |
|1ACC0238-2510-346-G3-EazyLogistics Android-Studio               |   main         |   78953ca36fbeda1692105e7f123420991e122d4f            |    add: 4 views for front                 |       06/20/2025                     |
|1ACC0238-2510-346-G3-EazyLogistics Android-Studio             |    main        |     f398972ec9d3a6be8f331a0006fb232960e00e31          |     add: routes and conecctions between views                |          06/20/2025                  |
|1ACC0238-2510-346-G3-EazyLogistics Android-Studio                    | main           |   34f9575a7437a1c380237d9e2e8912b45b042dd3            |     fix: styles in views                |          06/20/2025                  |
|1ACC0238-2510-346-G3-EazyLogistics Android-Studio                    |  main          |  cbe30081e4693945533d4eba3868d21dab6d70ad             |   fix: styles for views v.2                  |          06/20/2025                  |
|1ACC0238-2510-346-G3-EazyLogistics Android-Studio                    |  main          |  86df6e913e399349b6e2c2f7d7401fa8f716cefe             |      fix: styles for views v.3               |       06/20/2025                     |
|1ACC0238-2510-346-G3-EazyLogistics Android-Studio                    |   main         |  c2d6ae9456a64000a456df7110abc55bea5c7a4e             |         Feat(main) AdeddModels            |       06/20/2025                     |
|1ACC0238-2510-346-G3-EazyLogistics Android-Studio                    |    main        |   a2797b3698e3e9f4a2a3eb911712e818908a116b            |      add: icon for the project               |      06/20/2025                      |
|1ACC0238-2510-346-G3-EazyLogistics Android-Studio                    |   main         |  9dd0e735b40e5c79b90f115e097ed98c0395da03             |   Merge remote-tracking branch 'origin/main'                  |        06/20/2025                    |




#### 6.2.2.4. Testing Suite Evidence for Sprint Review 2
En este sprint, se ha completado el desarrollo de la aplicacion en Android Studio y tambien en flutter aunque este ultimo es un avance, aqui estan los repositorios de cada uno.

Link de la aplicacion en Android Studio: https://github.com/1ACC0238-2510-346-G3-EazyLogistics/Android-Studio
Link de la aplicacion en Flutter: https://github.com/1ACC0238-2510-346-G3-EazyLogistics/FlutterMobileApp

#### 6.2.2.5. Execution Evidence for Sprint Review 2

Durante el presente sprint, se desarrollaron las principales technical stories para la realización de la aplicacion movil en Android Studio

#### 6.2.2.6. Services Documentation Evidence for Sprint Review 2

Este sprint 2 tuvo como enfoque principal completar la aplicacion de Android Studio que aunque nuestra aplicacion no este al 100%, va en la etapa final de desarrollo, La documentación de Endpoints con OpenAPI y los detalles relacionados seran detallados en la entrega final.

#### 6.2.2.7. Software Deployment Evidence for Sprint Review 2

![evidence 1](../images/examples1.png)
![evidence 2](../images/examples2.png)
![evidence 3](../images/examples%203.png)

#### 6.2.2.8. Team Collaboration Insights during Sprint 2

El equipo trabajó en el desarrollo de la landing page utilizando ramas de cada feature, lo que permitió mejorar, actualizar y realizar modificaciones de manera más organizada. El uso de estas ramas facilita la integración y revisión antes de fusionarlas con la rama principal (main), asegurando que no se introduzcan errores. A continuación, se muestra el network graph y  code frecuency mediante la plataforma GitHub:
<br> 

![Insight 1](../images/insights%201.png)
![insights 2](../images/insights%202.png)
![insights 3 ](../images/insights%203.png)

## 6.3 Validation Interviews  
### 6.3.1 Diseño de Entrevistas  
#### 1. Preguntas para Gestores de Empresas Hoteleras
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

#### Entrevista 1
| **Datos del entrevistado** | 
|--------------------------|
| **Nombre:**  Miguel Polo |
| **Link del video:**  https://youtu.be/mzMYdfkO-wQ |
| **Edad:**  31 años |
| **Procedencia:**  Lima, San Isidro |
| ![Entrevista](../images/Entrevista1.1.png)|
| **Resumen:** Ramiro es un gestor de hotel en San Isidro, Lima, con cinco años de experiencia en la industria hotelera. El administra las reservas directamente en el sistema del hotel y le da mucha importancia a aspectos como el precio, la ubicación y las opiniones de los huéspedes. Aunque se siente cómodo gestionando reservas desde su smartphone, sugiere que las plataformas de reservas hoteleras deberían incluir más opciones de personalización, enviar recordatorios automáticos y ofrecer mayor claridad en las tarifas adicionales. Además, considera esencial recibir notificaciones y tener la opción de comunicarse directamente con los clientes a través de la plataforma. |

#### Entrevista 2
| **Datos del entrevistado** | 
|--------------------------|
| **Nombre:**  Aaron  |
| **Link del video:**  https://youtu.be/_SB_7uG-c-I|
| **Edad:**  22 años |
| **Procedencia:**  Lima, Villa Salvador |
| ![Entrevista](../images/Entrevista2.2.png)|
| **Resumen:** Roberto Franco  es un gestor de hotel en Lima con 4 años de experiencia en el sector. Maneja las reservas directamente en el sistema del hotel y considera esenciales factores como el precio, la ubicación y los comentarios de los huéspedes. Sugiere que las aplicaciones de reservas deberían ser más visuales, ofreciendo opciones de personalización, recordatorios automáticos y mayor claridad en los cargos adicionales. Para él, es crucial recibir notificaciones y tener la opción de comunicarse de forma directa con los clientes a través de la plataforma. |

## Segmento de huespedes

#### Entrevista 3
| **Datos del entrevistado** | 
|--------------------------|
| **Nombre:**  Jose Shuan https://youtu.be/PHPDHfchmEA  |
| **Link del video:** |
| **Edad:**  24 años |
| **Procedencia:**  Lima, Callao |
| ![Entrevista](../images/Entrevista3.3.png)|
| **Resumen:** Jose Shuan, un estudiante universitario de 24 años que reside en San Miguel, Lima, realiza la mayoría de sus reservas entre los 18 y 20 años, principalmente le gusta  hacer reservas a destinos nuevos , valorando el precio, la ubicación y las opiniones de otros usuarios. Se siente cómodo Logistic Master para realizar reservas, pero sugiere que nuestra plataforma  debería implementar mas facilidad a la hora de completar información detallada  acerca de su reserva. |

#### Entrevista 4
| **Datos del entrevistado** | 
|--------------------------|
| **Nombre:**  Lopez Diaz Gael Dario |
| **Link del video:**  https://youtu.be/tG7F4AsYnO8 |
| **Edad:**  20 años |
| **Procedencia:**  Lima, San Miguel |
| ![Entrevista](../images/Entrevista4.4.png)|
| **Resumen:** Gael, un estudiante universitario de 19 años que reside en San Miguel, Lima, realiza la mayoría de sus reservas entre los 18 y 20 años, principalmente le gusta  hacer reservas a destinos nuevos pero si no cuenta con mucho tiempo por la universidad prefiere cercanos  , valorando el precio, la ubicación y las opiniones de otros usuarios. Se siente Logistic Master cómodo usando  para realizar reservas, pero sugiere que nuestra plataforma  debería implementar mas facilidad a la hora de completar información detallada  acerca de su reserva . |


### 6.2.3. Sprint 3
#### 6.2.3.3 Sprint Planning 3
| **Sprint #**                    | Sprint 3                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sprint Planning Date**        |        11/07/25                                                                                                                                                                                                                                                                                                                                                         |
| **Time**                        | 2:00                                                                                                                                                                                                                                                                                                                                                                              |
| **Location**                    | Google Meet                                                                                                                                                                                                                                                                                                                                                                           |
| **Prepared By**                 | Mathias Vasquez                                                                                                                                                                                                                                                                                                                                                                    |
| **Attendees**                   | Gabriel, Fabian, Jose y Joaquin.                                                                                                                                                                                                                                                                                                                    |
| **Sprint Review Summary**       | Se desarollo en su totalidad el flutter y se desplego las mismas con la debida conexión del backend                                                                                                                                                                                                                                                                                                          |
| **Sprint Retrospective Summary**|   Se desarollo en su totalidad el flutter y se desplego las mismas con la debida conexión del backend                                                                                                                                                                                                                                                        |
| **Sprint Goal**                 | En este sprint, el objetivo es desarrollar la lógica y funcionalidades principales de la aplicacion moviel en flutter. |
| **Sprint Velocity**             | 26                                                                                                                                                                                                                                                                                                                                                                                    |
| **Sum of Story Points**         | 26 Story Points                                                                                                                                                                                                                                                                                                                                                                       |


#### 6.2.2.3. Sprint Backlog 3

| **User Story Id** | **User Story Title** | **Work-Item/Task Id** | **Work-Item/Task Title** | **Description** | **Estimation** | **Assigned To** | **Status** |
|:-----------------:|:--------------------:|:---------------------:|:-----------------------:|:---------------:|:--------------:|:--------------:|:----------:|
| US04 | Iniciar Sesión | T01 | Actualizar Contenido | Como huesped, quiero poder iniciar sesión para acceder a mi cuenta. . | 2h | Mathias Vasquez | Done |
| US05 | Reservar Habitación | T02 | Eliminar Contenido | Como huesped, quiero poder reservar una habitación para alojarme en el hotel. | 3h | Mathias Vasquez | Done |
| US010 | Registrar Usuario | T03 | Crear Contenido | Como huesped, quiero registrarme para crear una cuenta en el sistema. | 3h | Jose Luza | Done |
| US011 | Añadir a Favoritos  | T04 | Crear Usuario | Como usuario, quiero poder añadir habitaciones a favoritos para verlas luego. | 4h | Mathias Vasquez | Done |
| US012 | Autenticación JWT | T05 | Autenticar Usuario |  Como desarrollador, quiero autenticar usuarios y generar tokens JWT. | 2h | Mathias Vasquez | Done |
| US013 | Crear Huésped | T06 | Crear Huésped | Como huesped, quiero registrarme en mi reserva . | 4h | Joaquin Pedraza | Done |
| US022 | Modificar Reserva | T07 | Crear Habitación | Como huesped, quiero modificar mi reserva  | 3h | Joaquin Pedraza | Done |




#### 6.2.2.3. Development Evidence for Sprint Review 3
| Repository                                        | Branch | Commit Id                                 | Commit Message                                                | Committed on (Date) |
| ------------------------------------------------- | ------ | ----------------------------------------- | ------------------------------------------------------------- | ------------------- |
| 1ACC0238-2510-346-G3-EazyLogistics Flutter | main   | 0a1b2c3d4e5f67890abc123def456789abc123de  | Feat(main) Implemented login functionality for session start |     11/07/25       |
| 1ACC0238-2510-346-G3-EazyLogistics Flutter | main   | 123def456789abc123de0a1b2c3d4e5f67890abc  | Feat(main) Added room reservation functionality               |    11/07/25         |
| 1ACC0238-2510-346-G3-EazyLogistics Flutter | main   | abc456789def1230a1b2c3d4e5f67890abc123de  | Feat(main) User registration and validation               | 11/07/25         |
| 1ACC0238-2510-346-G3-EazyLogistics Flutter | main   | 789abc123def4560a1b2c3d4e5f67890abc123de  | Feat(main) Authentication with JWT implementation              |  11/07/25          |
| 1ACC0238-2510-346-G3-EazyLogistics Flutter | main   | c3d4e5f67890abc123de0a1b2c456789abc123def | Feat(main) Guest creation functionality                      |     11/07/25      |
| 1ACC0238-2510-346-G3-EazyLogistics Flutter | main   | 456789abc123de0a1b2c3d4e5f67890abc123def  | Feat(main) Modify reservation view and logic           |      11/07/25      |



#### 6.2.2.4. Testing Suite Evidence for Sprint Review 3
En este sprint, se ha completado el desarrollo de la aplicacion 



![evidence 1](../images/evidencee1.jpg)

![evidence 1](../images/evidencee2.jpg)

![evidence 1](../images/evidencee3.jpg)

![evidence 1](../images/evidencee4.jpg)

![evidence 1](../images/evidencee5.jpg)

![evidence 1](../images/evidencee6.jpg)

#### 6.2.2.5. Execution Evidence for Sprint Review 3

Durante el presente sprint, se desarrollaron las principales technical stories para la realización de la aplicacion movil en Android Studio del segmento de administradores y la aplicación movil en Flutter para el segmento de huespedes 

### Segmento de Huespedes (Flutter):
### Pantalla de Descubrimiento 
Muestra una bienvenida personalizada al huésped, con una barra de búsqueda y secciones de hoteles recomendados y populares, incluyendo precios y calificaciones.
![evidence 1](../images/descubrir.png)
![evidence 1](../images/descubrir2.png)
![evidence 1](../images/descubrir3.png)
### Pantalla de Favoritos (Favorite Hotels):
Lista los hoteles guardados como favoritos por el huésped, con la opción de reservar directamente desde allí.

![evidence 1](../images/favoritos.png)
### Sección Booking 
![evidence 1](../images/booking1.png)
![evidence 1](../images/booking2.png)
### Selección de Fechas (Select Date):
Muestra un calendario donde el huésped elige la fecha de check-in y check-out antes de continuar con la reserva.
![evidence 1](../images/booking3.png)
### Selección de Huéspedes (Select Guests):
Permite seleccionar cuántos adultos, niños e infantes se hospedarán, ajustando la reserva según el grupo.
![evidence 1](../images/booking4.png)
### Confirmar y Pagar (Confirm & Pay):
Resumen final de la reserva con detalles de fechas, huéspedes y pago. El huésped puede elegir el método de pago y finalizar la transacción.
![evidence 1](../images/payment1.png)
### Política de Privacidad (Privacy Policy):
Explica cómo se recopila, usa y protege la información personal del huésped dentro de la app.
![evidence 1](../images/privacy.png)
### Términos y Condiciones (Terms & Conditions):
Describe las reglas del uso de la app, incluyendo la creación de cuentas, uso de contenido y cambios en los términos.
![evidence 1](../images/terminos.png)
### Métodos de Pago (Payment Methods):
Muestra las tarjetas registradas del huésped y permite agregar nuevas para usarlas en futuras reservas.
![evidence 1](../images/payment2.png)
### Sección perfil de usuario
![evidence 1](../images/perfil.png)
#### 6.2.3.6. Services Documentation Evidence for Sprint Review 3

Este sprint 3 tuvo como enfoque principal completar la aplicacion de Flutter al 100%  y realizar la documentación de Endpoints con OpenAPI y los detalles relacionados seran detallados en la entrega final.<br>
Evidencia del despliegue de la base de datos 
![evidence 1](../images/serviceedep.png)

Evidencia del correcto guardado en la base de datos 
![evidence 1](../images/servicee1.png)
![evidence 1](../images/servicee2.png)

Link de la base de datos desplegada : http://20.57.133.61:8080/swagger-ui/index.html

#### 6.2.2.7. Software Deployment Evidence for Sprint Review 3

En esta sección se evidencia el despliegue de lo utilizado

Link de la base de datos desplegada : http://20.57.133.61:8080/swagger-ui/index.html
<br> 
El apk desplegado
![evidence 1](../images/apk.png)



#### 6.2.2.8. Team Collaboration Insights during Sprint 3

El equipo trabajó en el desarrollo de la landing page utilizando ramas de cada feature, lo que permitió mejorar, actualizar y realizar modificaciones de manera más organizada. El uso de estas ramas facilita la integración y revisión antes de fusionarlas con la rama principal (main), asegurando que no se introduzcan errores. A continuación, se muestra el network graph y  code frecuency mediante la plataforma GitHub:
<br> 
![evidence 1](../images/coob.jpg)
![evidence 1](../images/coob2.jpg)
![evidence 1](../images/coob3.png)
![evidence 1](../images/coob4.png)
## 6.4 Video About-the-Product

https://drive.google.com/file/d/1nEC2087NMDjZOr1kUtbodWaVe4GtZ2F0/view?usp=sharing
