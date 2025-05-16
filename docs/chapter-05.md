# **CAPÍTULO V: SOLUTION UI/UX DESIGN**

## 5.1. Product design

En esta seccion definiremos los estilos de diseño front-end que serán la base para dar forma a nuestro producto, utilizando patrones que consideren los aspectos de arquitectura de la información y accesibilidad necesarios para la implementación exitosa de UrProvider tanto en una Landing Page como en una Aplicación Movil.

### 5.1.1. Style Guidelines

**Branding:** El branding del logo de nuestra plataforma “LogisticsMaster” es una combinación de elementos que transmiten una imagen sólida y confiable. Nos enfocamos en la confianza de nuestro clientes al momento de tomar un servicio prestado. El nombre “LogisticsMaster” se presenta en una tipografía elegante y profesional, mientras que la paleta de colores crea un contraste visual claro y transmite una sensación de miminalismo y profesionalismo. En resumen, este logo tiene un enfoque clásico y profesional, y podría ser un elemento distintivo en nuestro sitio web.


<img src="../assets/Logo Logistics Master 1.jpg">
<img src="../assets/Logo Logistics Master 2.jpg">


**Typography:** Al seleccionar la tipografía para nuestro proyecto, hemos optado por utilizar Roboto siguiendo las pautas de estilo general. Ya que ofrece una combinación única de legibilidad, versatilidad y modernidad que se alinea perfectamente con la identidad visual y los objetivos de LogisticsMaster. Su diseño limpio y contemporáneo proporciona una excelente lectura en una amplia gama de dispositivos, lo que garantiza una experiencia de usuario óptima para nuestros clientes, que incluyen tanto agencias de embarcaciones navieras como exportadores e importadores de alta rotacion.

<img src="../assets/Tipography-LogisticsMaster.png">

**Colors:** Hemos escogido una paleta basada en colores suaves y elegantes, algo fríos para dar sensación de ser una aplicacion "premium" . De tal modo, estos generan un ambiente profesional y acogedor para el usuario final. Los tonos más claros pueden ser utilizados para fondos o elementos de diseño amplios, mientras que los colores más oscuros serán para textos o detalles más específicos asegurando legibilidad y contraste entre ellos.

<img src="../assets/Colors-LogisticsMaster.png">

#### 5.1.1.1 General Style Guidelines

Para los generals style guidelines del "LogisticsMaster" se utilizó con mayor presencia los colores pasteles en base a una paleta de colores que genere confianza y un ambiente acogedor para el usuario. El logo genera presencia por la combinación de elementos que transmiten una imagen sólida y confiable. A su vez, se ideó un estilo minimalista en el desarrollo del Landing Page para que el usuario tenga la facilidad de navegar y pueda observar las secciones con mayor orden. El tipo de Roboto combina con los colores anteriormente seleccionados, ya que brinda mayor flexibilidad y versatilidad. Para el desarrollo de los mockups y wireframes se utilizó en base a desarrollo web para pantallas de escritorio.

### 5.1.2 Information Architecture

#### 5.1.2.1 Organization Systems

- **Segmento Huésped**

    - Registro y Acceso de Usuario: Sistema seguro que permite a los huéspedes registrarse e iniciar sesión, ofreciendo una experiencia personalizada y protegida, incluyendo opciones para recuperación de contraseñas y verificación de cuentas.

    - Gestión de Reservas: Los huéspedes pueden gestionar sus reservas, ver detalles de las mismas y realizar cambios si es necesario, proporcionando flexibilidad y control durante su estancia.

    - Configuración de Preferencias: Los huéspedes pueden establecer preferencias para tipos de habitaciones, comodidades y servicios, asegurando una experiencia personalizada durante su estancia.

    - Historial de Reservas: Un registro detallado de reservas anteriores permite a los huéspedes re-reservar fácilmente sus alojamientos favoritos y visualizar su historial de viajes.

- **Segmento Hotel**

    - Gestión de Ofertas y Promociones: Los hoteles pueden crear y gestionar ofertas especiales para atraer a los huéspedes, mejorando la lealtad de los clientes y aumentando las ventas.

    - Historial de Ventas: Una vista completa de todas las transacciones permite a los hoteles analizar tendencias de ventas y generar informes para la toma de decisiones estratégicas.

    - Gestión de Inventario y Disponibilidad: Este sistema ayuda a los hoteles a rastrear la disponibilidad de habitaciones y gestionar el inventario en tiempo real, optimizando las tasas de ocupación y minimizando el sobrecupo.

    - Sistema de Gestión de Reservas: Los hoteles pueden manejar de manera eficiente todas las reservas, incluidas cancelaciones y modificaciones, mejorando la eficiencia operativa y la satisfacción del cliente.

    - Gestión de Perfil del Hotel: Los hoteles pueden mantener un perfil detallado con información sobre comodidades, servicios y opiniones de clientes, lo cual ayuda a construir confianza y atraer a nuevos huéspedes.

#### 5.1.2.2 Labeling Systems

- **Segmento Huésped**

    - Etiqueta de Estado de Reserva: Muestra el estado de la reserva (por ejemplo, confirmada, pendiente, cancelada) junto con los horarios de check-in y check-out, ayudando a los huéspedes a mantenerse informados sobre sus reservas.

    - Etiqueta de Solicitud de Servicios: Permite a los huéspedes rastrear el estado de cualquier solicitud o servicio especial (por ejemplo, servicio a la habitación, limpieza), asegurando un cumplimiento oportuno.

    - Etiqueta de Preferencias de Reserva: Resalta las preferencias de los huéspedes para tipos de habitaciones, comodidades o servicios especiales, asegurando un servicio personalizado durante toda su estancia.

- **Segmento Hotel**

    - Etiqueta de Reserva: Contiene información clave como nombres de huéspedes, asignaciones de habitaciones y fechas de reserva, ayudando al personal del hotel a gestionar las reservas sin problemas.

    - Etiqueta de Disponibilidad: Muestra la disponibilidad de habitaciones en tiempo real, ayudando al personal del hotel a tomar decisiones rápidas e informadas sobre las reservas.

    - Etiqueta de Pedidos: Rastrear los pedidos de servicios o comodidades adicionales de los huéspedes, asegurando una entrega precisa y oportuna por parte del personal.

    - Etiqueta de Promociones y Ofertas: Resalta promociones y ofertas actuales tanto para huéspedes como para el personal, fomentando las ventas adicionales y aumentando el compromiso de los huéspedes.

#### 5.1.2.3 SEO Tags and Meta Tags

Para la búsqueda eficiente de nuestra plataforma en los buscadores web se emplearon las siguientes tags:
- Title: LogisticsMaster
- Meta Tags:
    - Description: Plataforma de optimización de logistica para hoteles y huespedes.
    - Keywords: hoteles, huespedes, busqueda de hoteles, gestion de hotel, logistica, logistica de hoteles.
    - Author: LogisticsMaster

#### 5.1.2.4 Searching Systems

En esta parte, se indicarán los sistemas de búsqueda que se implementaran en la Landing Page y Mobile Application.

- **Segmento Huésped**

    - Búsqueda por Palabras Clave: Los huéspedes pueden usar una barra de búsqueda para encontrar hoteles específicos, habitaciones o comodidades por nombre o palabra clave, simplificando el proceso de reserva.

    - Búsqueda por Filtros: Los filtros permiten a los huéspedes reducir opciones por precio, ubicación, comodidades y más, ayudándolos a encontrar rápidamente el alojamiento perfecto.

- **Segmento Hotel**

    - Búsqueda por Palabras Clave: El personal del hotel puede buscar reservas específicas, huéspedes o servicios utilizando palabras clave, facilitando el acceso rápido a información importante.

    - Búsqueda por Filtros: Los filtros ayudan al personal a refinar los resultados de búsqueda por estado de reserva, tipo de habitación o preferencias de huéspedes, mejorando la eficiencia operativa.

#### 5.1.2.5 Navigation Systems

En esta parte, se indicará los sistemas de navegación que se utilizaron para la búsqueda rápida de las secciones que son de interés para los usuarios para el la landing page y la aplicación web.


- **Segmento Huésped**

    - Menú de Navegación: Un menú superior permite a los huéspedes acceder rápidamente a sus reservas, preferencias y configuraciones de cuenta, asegurando una experiencia de usuario fluida.

    - Enlaces Rápidos: Proporciona acceso fácil a funciones de uso frecuente como historial de reservas, soporte y ofertas especiales, mejorando la usabilidad.

- **Segmento Hotel**

    - Menú de Navegación: Un menú superior permite al personal del hotel navegar eficientemente entre reservas, inventario y promociones, optimizando su flujo de trabajo.

    - Enlaces Rápidos: Ofrece acceso rápido a funciones críticas como gestión de reservas, actualizaciones de inventario y configuración de promociones, aumentando la velocidad operativa.

## 5.1.3 Landing Page UI Design 
### 5.1.3.1 Landing Page Wireframe

<img src="../../assets/img/chapter-IV/wireframe-landing.jpg" style="width:700px; height:auto;" alt="wireframe landing page">

### 5.1.3.2 Landing Page Mock-up

<img src="../../assets/img/chapter-IV/mockup-landing.jpg" style="width:700px; height:auto;" alt="mock up landing page">

## 5.1.4 Mobile Applications UX/UI Design
### 5.1.4.1. Mobile Applications Wireframes

<img src="../assets/Mobile Wireframe1.png">
<img src="../assets/Mobile Wireframe2.png">
<img src="../assets/Mobile Wireframe3.png">

### 5.1.4.2. Mobile Applications Wireflow Diagrams

- **User Goal 1: Iniciar sesión**
<br>
<img src="../assets/UserGoal1.png">

- **User Goal 2: Asignar una tarea a un empleado**
<br>
<img src="../assets/UserGoal2.png">

- **User Goal 3: Añadir una reserva**
<br>
<img src="../assets/UserGoal4.png">

- **User Goal 4: Modificar una reserva existente**
<br>
<img src="../assets/UserGoal5.png">

- **User Goal 5: Cancelar una reserva**
<br>
<img src="../assets/UserGoal6.png">

- **User Goal 6: Generar reportes de estadísticas personalizadas**
<br>
<img src="../assets/UserGoal7.png">

### 5.1.4.3. Mobile Applications Mock-ups

<img src="../assets/Mockup1-LogisticsMaster.png">
<img src="../assets/Mockup2-LogisticsMaster.png">
<img src="../assets/Mockup3-LogisticsMaster.png">

### 5.1.4.4. Mobile Applications User Flow Diagrams

<img src="../assets/UserFlow1-LogisticsMaster.png">
<img src="../assets/UserFlow2-LogisticsMaster.png">
<img src="../assets/UserFlow3-LogisticsMaster.png">
<img src="../assets/UserFlow4-LogisticsMaster.png">
<img src="../assets/UserFlow5-LogisticsMaster.png">
<img src="../assets/UserFlow6-LogisticsMaster.png">


### 5.1.4.5. Mobile Applications Prototyping

