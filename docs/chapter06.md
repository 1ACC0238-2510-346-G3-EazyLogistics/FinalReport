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

### 6.2.X.3 Development Evidence for Sprint Review  
### 6.2.X.4 Testing Suite Evidence for Sprint Review  
### 6.2.X.5 Execution Evidence for Sprint Review  
### 6.2.X.6 Services Documentation Evidence for Sprint Review  
### 6.2.X.7 Software Deployment Evidence for Sprint Review  
### 6.2.X.8 Team Collaboration Insights during Sprint  

## 6.3 Validation Interviews  
### 6.3.1 Diseño de Entrevistas  
### 6.3.2 Registro de Entrevistas  
### 6.3.3 Evaluaciones según heurísticas  

## 6.4 Video About-the-Product
