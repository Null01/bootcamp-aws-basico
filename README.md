# bootcamp-aws-basico

<div align="center">
  <img height="350" width="1080"  src="img/fondo-aws-project.png"  />
</div>

<h1 align="center">Proyecto AWS</h1>

<p>
    Bienvenidos a nuestro proyecto. Elaborado por Jose Navarro - Julio - Andres 
    donde diseñé e implementé una arquitectura basada en la nube utilizando Amazon Web Services (AWS). 
    Este proyecto tenía como objetivo crear una infraestructura escalable, segura y eficiente para implementar modelos de aprendizaje profundo.
    A través de este proyecto, demostré mis habilidades en computación en la nube, diseño de arquitectura y prácticas de DevOps.

    En este repositorio encontrarás una documentación detallada de mi proyecto, incluyendo las fases de planificación, ejecución y seguimiento.
    Utilicé servicios de AWS como CloudFormation, Pipeline y CloudWatch para diseñar e implementar una arquitectura sólida y confiable.
    Además, seguímos el marco de buena arquitectura de AWS para garantizar las prácticas recomendadas en seguridad, rendimiento y optimización de costos.

</p>

<h3 saling="center">
    <a href="https://git.io/typing-svg">
        <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=15&pause=1000&color=F7F7F7&random=false&width=435&lines=Requerimientos;How+vexingly+quick+daft+zebras+jump" alt="Typing SVG" />
    </a>
</h3>
<h2 aling="center"> Requerimientos Funcionles </h2>
<ul>
        <li>Creación de una VPC con un bloque CIDR específico y habilitación de nombres de host DNS.</li>
        <li>Conectividad a Internet a través de una puerta de enlace de Internet (IG) adjunta a la VPC.</li>
        <li>Creación de tablas de rutas públicas y privadas para enrutar tráfico hacia las subredes correspondientes. </li>
        <li>Uso de puertas de enlace NAT para permitir que las instancias en subredes privadas accedan a Internet.</li>
        <li>Asignación de direcciones IP elásticas a las puertas de enlace NAT. </li>
        <li>Creación de subredes públicas y privadas con bloques CIDR específicos.</li>
        <li>Asociación de tablas de rutas con subredes correspondientes.</li>
        <li>Creación de grupos de seguridad para controlar el tráfico hacia las instancias y recursos.</li>
        <li>Configuración de reglas de seguridad para permitir el tráfico SSH, HTTP y MySQL entre los grupos de seguridad.</li>
        <li>Creación de un Launch Template para lanzar instancias con configuración específica.</li>
        <li>Creación de un Target Group para enrutar tráfico hacia instancias específicas </li>
        <li>Configuración de un Auto Scaling Group para escalar instancias según la demanda.</li>
        <li>Creación de una instancia pública con configuración específica. </li>
        <li>Creación de un Application Load Balancer (ALB) para distribuir tráfico hacia instancias. </li>
        <li>Configuración de un Listener para enrutar tráfico hacia el Target Group </li>
        <li>Creación de una política de escalado para ajustar la capacidad del Auto Scaling Group según la utilización de CPU. </li>
</ul>

<h3 style="align-items: center;">
    <a href="https://git.io/typing-svg">
        <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=15&pause=1000&color=F7F7F7&random=false&width=435&lines=Diagrama+Arquitectura;How+vexingly+quick+daft+zebras+jump" alt="Typing SVG" />
    </a>
</h3>

<h3 style="align-items: center;">
    <a href="https://git.io/typing-svg">
        <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=15&pause=1000&color=F7F7F7&random=false&width=435&lines=Roles;How+vexingly+quick+daft+zebras+jump" alt="Typing SVG" />
    </a>
</h3>
