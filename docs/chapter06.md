# Capítulo VI: Product Implementation, Validation & Deployment

## 6.1 Software Configuration Management

### 6.1.1 Software Development Environment Configuration  
### 6.1.2 Source Code Management  
### 6.1.3 Source Code Style Guide & Conventions  
### 6.1.4 Software Deployment Configuration  

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

| Repository             | Branch | Commit Id | Commit Message                    | Commit Message Body                                                     | Commited on (Date) |
|------------------------|--------|-----------|-----------------------------------|-------------------------------------------------------------------------|--------------------|
| FabianTG25/LandingPage | main   |           | Implementación de la Landing Page | Se implementó la Landing Page con todas las funcionalidades requeridas. | 2025/05/14         |

Enlace al repositorio: https://github.com/1ACC0238-2510-346-G3-EazyLogistics/LandingPage

### 6.2.1.4 Testing Suite Evidence for Sprint Review  
Para este sprint, no se han realizado pruebas automatizadas, ya que el equipo ha decidido enfocarse en la implementación de la Landing Page y no se han desarrollado pruebas unitarias o de integración. Sin embargo, se han realizado pruebas manuales para asegurar que la Landing Page funcione correctamente y cumpla con los requisitos establecidos.
Se podrían implementar pruebas automatizadas utilizando herramientas como Selenium en futuros sprints, pero por el momento, el equipo ha optado por realizar pruebas manuales para asegurar la calidad del producto.

### 6.2.1.5 Execution Evidence for Sprint Review  
En este Sprint 1, el equipo ha desarrollado y desplegado la Landing Page, asegurando que cumpla con los requisitos establecidos y funcione correctamente. A continuación, se presentan las evidencias de ejecución del Sprint 1, que incluyen capturas de pantalla y descripciones de las funcionalidades implementadas.

### 6.2.1.6 Services Documentation Evidence for Sprint Review  
Este sprint 1 tuvo como enfoque principal la implementación de la Landing Page, por lo que no se han desarrollado Web Services. La documentación de Endpoints con OpenAPI y los detalles relacionados con Web Services serán relevantes en sprints futuros cuando se aborde la implementación y documentación de estos servicios. 

### 6.2.1.7 Software Deployment Evidence for Sprint Review  
En este Sprint 1, el equipo ha desplegado la Landing Page utilizando github pages. A continuación, se presentan las evidencias de despliegue del Sprint 1, que incluyen capturas de pantalla y pasos detallados del proceso de despliegue.
1. **Creación del Repositorio**: Se creó un repositorio en GitHub para alojar el código de la Landing Page. El repositorio se llama "LandingPage" y está disponible en la cuenta de GitHub del equipo.
<br> ![Landing Page Repository](../images/landing_page_repository.png)
<br> url del repositorio: https://github.com/1ACC0238-2510-346-G3-EazyLogistics/LandingPage

2. **Configuración de GitHub Pages**: Se habilitó la opción de GitHub Pages en la configuración del repositorio. Esto permite que el contenido del repositorio se publique como una página web estática.
<br> ![GitHub Pages Configuration](../images/github_pages_configuration.png)

3. **Despliegue de la Landing Page**: Se subió el código HTML y CSS de la Landing Page al repositorio. GitHub Pages generó automáticamente una URL para acceder a la página.
<br> ![Landing Page Deployment](../images/landing_page_deployment.png)

4. **Acceso a la Landing Page**: La Landing Page se puede acceder a través de la URL proporcionada por GitHub Pages. Esta URL es pública y permite que cualquier persona acceda a la página.
<br> ![Landing Page Access](../images/landing_page_access.png)
<br> url de la landing page: https://1acc0238-2510-346-g3-eazylogistics.github.io/LandingPage/

### 6.2.1.8 Team Collaboration Insights during Sprint  
Para el desarrollo de este sprint, el equipo se dividió las actividades de implementación de la Landing Page, asegurando que cada miembro del equipo se encargara de una parte específica del proyecto.

GitHub insights:


## 6.3 Validation Interviews  
### 6.3.1 Diseño de Entrevistas  
### 6.3.2 Registro de Entrevistas  
### 6.3.3 Evaluaciones según heurísticas  

## 6.4 Video About-the-Product
