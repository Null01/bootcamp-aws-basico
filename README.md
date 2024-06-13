    <div align="center">
<img height="350" width="1000"  src="img/fondo-aws-project.png"  />
</div>

<h1 align="center"> Proyecto AWS - El mundo de las Letras</h1>

<h3>
    Bienvenidos a nuestro proyecto. Elaborado por Jose Navarro | Julio | Andres Garcias donde diseñamos e implementamos una arquitectura basada en la nube utilizando Amazon Web Services (AWS). Este proyecto tenía como objetivo crear una infraestructura escalable, segura y eficiente para implementar modelos de aprendizaje profundo. A través de este proyecto, demostré mis habilidades en computación en la nube, diseño de arquitectura y prácticas de DevOps.En este repositorio encontrarás una documentación detallada de mi proyecto basada en AWS Well-Architected, incluyendo las fases de planificación, ejecución y seguimiento. Utilicé servicios de AWS como CloudFormation, Pipeline y CloudWatch para diseñar e implementar una arquitectura sólida y confiable. Además, seguímos el marco de buena arquitectura de AWS para garantizar las prácticas recomendadas en seguridad, rendimiento y optimización de costos.</h3>

> [!IMPORTANT]
>
> <h2> 1. Requerimientos </h2>

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=15&pause=1000&color=F7F7F7&center=true&vCenter=true&random=false&width=435&lines=1.1++Requerimiento+Funcionales" alt="Typing SVG" /></a>

<table>
    <tr>
      <th>Requisito</th>
      <th>Descripción</th>
    </tr>
    <tr>
      <td>1. Creación de VPC</td>
      <td>Creación de una VPC con un bloque CIDR específico y habilitación de nombres de host DNS.</td>
    </tr>
    <tr>
      <td>2. Conectividad a Internet</td>
      <td>Conectividad a Internet a través de una puerta de enlace de Internet (IG) adjunta a la VPC.</td>
    </tr>
    <tr>
      <td>3. Creación de tablas de rutas</td>
      <td>Creación de tablas de rutas públicas y privadas para enrutar tráfico hacia las subredes correspondientes.</td>
    </tr>
    <tr>
      <td>4. Uso de puertas de enlace NAT</td>
      <td>Uso de puertas de enlace NAT para permitir que las instancias en subredes privadas accedan a Internet.</td>
    </tr>
    <tr>
      <td>5. Asignación de direcciones IP elásticas</td>
      <td>Asignación de direcciones IP elásticas a las puertas de enlace NAT.</td>
    </tr>
    <tr>
      <td>6. Creación de subredes</td>
      <td>Creación de subredes públicas y privadas con bloques CIDR específicos.</td>
    </tr>
    <tr>
      <td>7. Asociación de tablas de rutas</td>
      <td>Asociación de tablas de rutas con subredes correspondientes.</td>
    </tr>
    <tr>
      <td>8. Creación de grupos de seguridad</td>
      <td>Creación de grupos de seguridad para controlar el tráfico hacia las instancias y recursos.</td>
    </tr>
    <tr>
      <td>9. Configuración de reglas de seguridad</td>
      <td>Configuración de reglas de seguridad para permitir el tráfico SSH, HTTP y MySQL entre los grupos de seguridad.</td>
    </tr>
    <tr>
      <td>10. Creación de Launch Template</td>
      <td>Creación de un Launch Template para lanzar instancias con configuración específica.</td>
    </tr>
    <tr>
      <td>11. Creación de Target Group</td>
      <td>Creación de un Target Group para enrutar tráfico hacia instancias específicas.</td>
    </tr>
    <tr>
      <td>12. Configuración de Auto Scaling Group</td>
      <td>Configuración de un Auto Scaling Group para escalar instancias según la demanda.</td>
    </tr>
    <tr>
      <td>13. Creación de instancia pública</td>
      <td>Creación de una instancia pública con configuración específica.</td>
    </tr>
    <tr>
      <td>14. Creación de Application Load Balancer (ALB)</td>
      <td>Creación de un Application Load Balancer (ALB) para distribuir tráfico hacia instancias.</td>
    </tr>
    <tr>
      <td>15. Configuración de Listener</td>
      <td>Configuración de un Listener para enrutar tráfico hacia el Target Group.</td>
    </tr>
    <tr>
      <td>16. Creación de política de escalado</td>
      <td>Creación de una política de escalado para ajustar la capacidad del Auto Scaling Group según la utilización de CPU.</td>
    </tr>
  </table>

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=14&pause=1000&color=F7F7F7&center=true&vCenter=true&random=false&width=435&lines=1.2++Requerimiento+no+Funcionales" alt="Typing SVG" /></a>

<ul>
    <li>Aplicacion en Python 3</li>
    <li>Base de Datos en MariaDB</li>
    <li>Etiquetado de recursos con nombres descriptivos para facilitar la identificación y gestión.</li>
    <li>Uso de nombres de host DNS habilitados para facilitar la resolución de nombres.</li>
    <li>Uso de puertas de enlace NAT para proteger las instancias en subredes privadas.</li>
    <li>Creación de múltiples subredes y puertas de enlace NAT para admitir un crecimiento futuro.</li>
    <li>Uso de nombres descriptivos y configuración de recursos para facilitar la gestión y mantenimiento de la infraestructura.</li>
</ul>

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=14&pause=1000&color=F7F7F7&center=true&vCenter=true&random=false&width=435&lines=Identificacion+de+Roles" alt="Typing SVG" /></a>

> [!IMPORTANT]
>
> <h3> A continuación, se presentan los roles y perfiles definidos mediante el servicio IAM. </h3>

<ul>
    <li>Administrador de nube y servidores: posee derechos de administración totales, con acceso a todos los recursos de AWS.</li>
    <li>Desarrollador: cuenta con acceso restringido solo a AWS Cloud9, sin permisos adicionales.</li>
    <li>Administrador de servidor Web y Base de Datos: tiene acceso completo a Amazon EC2, RDS y System Manager (Parameter Store), permitiéndole administrar y configurar los recursos correspondientes.    </li>
    <li>Equipo de soporte de Almacenamiento: solo puede visualizar los buckets creados en S3, sin permisos de escritura o edición.</li>
    <li>Usuario de Consulta: tiene acceso de solo lectura a Amazon EC2 y RDS, permitiéndole consultar y visualizar la información, pero sin capacidad de realizar cambios o modificaciones.</li>
    <li>Auditor: cuenta con acceso de solo lectura a Amazon EC2, RDS e IAM, permitiéndole revisar y auditar la configuración y los recursos, pero sin capacidad de modificarlos.
    </li>
</ul>

> [!IMPORTANT]
> Diagrama Arquitectura

<div align="center">
        <img height="350" width="500" src="img/aws-structure.png">
</div>

> [!NOTE]
> Seguimiento y Control Basado en AWS Well-Architected Framework

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=25&pause=1000&color=FFFFFF&center=true&vCenter=true&random=false&width=435&lines=Template+Network" alt="Typing SVG" /></a>

<h3 align="center">Excelencia Operativa</h3>
<table>
    <tr>
        <th>Requisito</th>
        <th>Descripción</th>
    </tr>
    <tr>
        <td>VPC</td>
        <td>Configurado con un bloque CIDR predeterminado y nombres de host DNS habilitados, lo que demuestra una
            configuración de infraestructura bien planificada y ejecutada.</td>
    </tr>
    <tr>
        <td>RouteTables</td>
        <td>Se crean varias tablas de rutas para subredes públicas y privadas, lo que garantiza un enrutamiento y una
            gestión de red eficientes.</td>
    </tr>
    <tr>
        <td>Asociación de tablas de rutas</td>
        <td>Las tablas de rutas están asociadas a las subredes correctas, lo que garantiza que el tráfico se enrute de
            forma correcta y eficiente.</td>
    </tr>
</table>
    
<h3 align="center">Seguridad</h3>
<table>
    <tr>
        <th>Requisito</th>
        <th>Descripción</th>
    </tr>
    <tr>
        <td>VPC</td>
        <td>La VPC está configurada con un bloque CIDR predeterminado, que ayuda a evitar el acceso no autorizado a la
            red.</td>
    </tr>
    <tr>
        <td>InternetGateway</td>
        <td>La puerta de enlace de Internet está conectada a la VPC, lo que proporciona un punto de entrada y salida
            seguro para el tráfico de Internet.</td>
    </tr>
    <tr>
        <td>NAT Gateway</td>
        <td>Se crean dos puertas de enlace NAT, cada una con su propia dirección IP elástica, lo que proporciona una
            forma segura y escalable de acceder a Internet desde subredes privadas.</td>
    </tr>
</table>
    
<h3 align="center">Fiabilidad</h3>
<table>
    <tr>
        <th>Requisito</th>
        <th>Descripción</th>
    </tr>
    <tr>
        <td>NAT Gateway</td>
        <td>Se crean dos puertas de enlace NAT, lo que proporciona redundancia y garantiza que, si una puerta de enlace
            falla, la otra pueda seguir proporcionando acceso a Internet a subredes privadas.</td>
    </tr>
    <tr>
        <td>RouteTable</td>
        <td>Se crean varias tablas de rutas, lo que proporciona redundancia y garantiza que si una tabla de rutas falla,
            la otra puede continuar enrutando el tráfico correctamente.</td>
    </tr>
    <tr>
        <td>Subredes</td>
        <td>Se crean seis subredes, que proporcionan una infraestructura de red escalable y flexible que puede adaptarse
            a las necesidades cambiantes del negocio.</td>
    </tr>
</table>
    
<h3 align="center">Optimización del rendimiento</h3>
<table>
    <tr>
        <th>Requisito</th>
        <th>Descripción</th>
    </tr>
    <tr>
        <td>Subredes</td>
        <td>Se crean seis subredes, cada una con su propio bloque CIDR, lo que proporciona una infraestructura de red
            escalable y flexible que puede adaptarse a las necesidades cambiantes del negocio.</td>
    </tr>
    <tr>
        <td>NAT Gateway</td>
        <td>Se crean dos puertas de enlace NAT, cada una con su propia dirección IP elástica, lo que proporciona una
            forma escalable y eficiente de acceder a Internet desde subredes privadas.</td>
    </tr>
    <tr>
        <td>Tablas de rutas</td>
        <td>Se crean varias tablas de rutas, lo que proporciona una gestión eficiente del enrutamiento y la red.</td>
    </tr>
</table>
<h3 align="center" >Optimización de costos</h3>
<table>
  <tr>
    <th>Requisito</th>
    <th>Descripción</th>
  </tr>
  <tr>
    <td>VPC</td>
    <td>La VPC está configurada con un bloque CIDR predeterminado, que ayuda a optimizar los recursos de la red y reducir los costos.</td>
  </tr>
  <tr>
    <td>NAT Gateway</td>
    <td>Se crean dos puertas de enlace NAT, cada una con su propia dirección IP elástica, lo que proporciona una forma rentable de acceder a Internet desde subredes privadas.</td>
  </tr>
  <tr>
    <td>Subredes</td>
    <td>Se crean seis subredes, cada una con su propio bloque CIDR, que proporcionan una infraestructura de red rentable y escalable que puede adaptarse a las necesidades cambiantes del negocio.</td>
  </tr>
</table>

> [!NOTE]
> Una VPC con un bloque CIDR de 172.16.0.0/16 (valor predeterminado, se puede anular)
> Nombres de host DNS habilitados
> Etiquetado con "Nombre" = "VPC-WEB-SERVER-BOOK"
> (valor predeterminado, se puede anular)
> Nombres de host DNS habilitados
> Etiquetado con "Nombre" = "VPC-WEB-SERVER-BOOK"

```
Parameters:
  VpcCIDR:
    Type: String
    Default: 172.16.0.0/16
```

```
VPC:
    Type: AWS::EC2::VPC
    Properties:
      CidrBlock:
        Ref: VpcCIDR
      EnableDnsHostnames: true
      Tags:
        - Key: Name
          Value: VPC-WEB-SERVER-BOOK
```

> [!NOTE]
> Subredes:
> 6 subredes en total:
> 2 subredes públicas (A y B) con bloques CIDR de 172.16.1.0/24 y 172.16.2.0/24 (valores predeterminados, se pueden anular)
> 4 subredes privadas (A, B, AA y BB) con bloques CIDR de 172.16.3.0/24, 172.16.4.0/24, 172.16.5.0/24 y 172.16.6.0/24 (valores predeterminados, se pueden anular)
> Cada subred se etiqueta con una etiqueta "Nombre" que indica su propósito (por ejemplo, "PublicSubnetA", "PrivateSubnetB", etc.)

```
PublicSubnetAIP:
    Type: String
    Default: 172.16.1.0/24

  PublicSubnetBIP:
    Type: String
    Default: 172.16.2.0/24

  PrivateSubnetAIP:
    Type: String
    Default: 172.16.3.0/24

  PrivateSubnetBIP:
    Type: String
    Default: 172.16.4.0/24

  PrivateSubnetAAIP:
    Type: String
    Default: 172.16.5.0/24

  PrivateSubnetBBIP:
    Type: String
    Default: 172.16.6.0/24
```

```
PublicSubnetA:
    Type: AWS::EC2::Subnet
    Properties:
      VpcId:
        Ref: VPC
      AvailabilityZone: us-east-1a
      CidrBlock:
        Ref: PublicSubnetAIP
      Tags:
        - Key: Name
          Value: PublicSubnetA

  PublicSubnetB:
    Type: AWS::EC2::Subnet
    Properties:
      VpcId:
        Ref: VPC
      AvailabilityZone: us-east-1b
      CidrBlock:
        Ref: PublicSubnetBIP
      Tags:
        - Key: Name
          Value: PublicSubnetB

  PrivateSubnetA:
    Type: AWS::EC2::Subnet
    Properties:
      VpcId:
      AvailabilityZone: us-east-1a
        Ref: VPC
      CidrBlock:
        Ref: PrivateSubnetAIP
      Tags:
        - Key: Name
          Value: PrivateSubnetA

  PrivateSubnetB:
    Type: AWS::EC2::Subnet
    Properties:
      VpcId:
        Ref: VPC
      AvailabilityZone: us-east-1b
      CidrBlock:
        Ref: PrivateSubnetBIP
      Tags:
        - Key: Name
          Value: PrivateSubnetB

  PrivateSubnetAA:
    Type: AWS::EC2::Subnet
    Properties:
      VpcId:
        Ref: VPC
      AvailabilityZone: us-east-1a
      CidrBlock:
        Ref: PrivateSubnetAAIP
      Tags:
        - Key: Name
          Value: PrivateSubnetAA

  PrivateSubnetBB:
    Type: AWS::EC2::Subnet
    Properties:
      VpcId:
        Ref: VPC
      AvailabilityZone: us-east-1b
      CidrBlock:
        Ref: PrivateSubnetBBIP
      Tags:
        - Key: Name
          Value: PrivateSubnetBB
```

> [!NOTE]
> Internet Gateway:
> Una puerta de enlace de Internet (IG) con una etiqueta "Nombre" = "IG_WSC"
> Adjunto a la VPC

```
InternetGateway:
    Type: AWS::EC2::InternetGateway
    Properties:
      Tags:
        - Key: Name
          Value: IG_WSC

  InternetGatewayAttachment:
    Type: AWS::EC2::VPCGatewayAttachment
    Properties:
      InternetGatewayId:
        Ref: InternetGateway
      VpcId:
        Ref: VPC
```

> [!IMPORTANT]
> Route Table:
> Una tabla de rutas pública con una etiqueta "Nombre" = "Public_Routes"
> Dos tablas de rutas privadas (una para cada NatGateway) con las etiquetas "Name" = "Route-NW-A" y "Route-NW-B"

```
 PublicRouteTable:
    Type: AWS::EC2::RouteTable
    Properties:
      VpcId:
        Ref: VPC
      Tags:
        - Key: Name
          Value: Public_Routes

  PublicRouteA:
    Type: AWS::EC2::Route
    DependsOn: InternetGatewayAttachment
    Properties:
      RouteTableId:
        Ref: PublicRouteTable
      DestinationCidrBlock: 0.0.0.0/0
      GatewayId:
        Ref: InternetGateway

  PublicSubnet1RouteTableAssociation:
    Type: AWS::EC2::SubnetRouteTableAssociation
    Properties:
      RouteTableId:
        Ref: PublicRouteTable
      SubnetId:
        Ref: PublicSubnetA

  PublicSubnet2RouteTableAssociation:
    Type: AWS::EC2::SubnetRouteTableAssociation
    Properties:
      RouteTableId:
        Ref: PublicRouteTable
      SubnetId:
        Ref: PublicSubnetB

```

> [!NOTE]
> Nat Gateway
> Dos puertas de enlace NAT (A y B) con direcciones IP elásticas
> Cada puerta de enlace NAT está asociada a una subred pública (A y B) y a una tabla de rutas privada (A y B)

```
NatGatewayA:
    Type: AWS::EC2::NatGateway
    Properties:
      AllocationId: !GetAtt AipELASTIC.AllocationId
      SubnetId:
        Ref: PublicSubnetA
      Tags:
        - Key: Name
          Value: NatGatewayA-subnetPublicA

  NatGatewayB:
    Type: AWS::EC2::NatGateway
    Properties:
      AllocationId: !GetAtt BipELASTIC.AllocationId
      SubnetId:
        Ref: PublicSubnetB
      Tags:
        - Key: Name
          Value: NatGatewayA-subnetPublicB
```

> [!NOTE]
> IP elásticas:
> Dos direcciones IP elásticas (A y B) con etiquetas "Nombre" = "EIP-nwA" y "EIP-nwB"
> Cada dirección IP elástica está asociada a una puerta de enlace NAT (A y B)

```
AipELASTIC:
    Type: AWS::EC2::EIP
    Properties:
      Domain:
        Ref: VPC
      Tags:
        - Key: Name
          Value: EIP-nwA

  BipELASTIC:
    Type: AWS::EC2::EIP
    Properties:
      Domain:
        Ref: VPC
      Tags:
        - Key: Name
          Value: EIP-nwB

```

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=25&pause=1000&color=FFFFFF&center=true&vCenter=true&random=false&width=435&lines=Template+Application" alt="Typing SVG" /></a>

<h3 align="center">Excelencia Operativa</h3>
<table>
    <tr>
        <th>Requisito</th>
        <th>Descripción</th>
    </tr>
    <tr>
        <td>LaunchTemplate</td>
        <td>Se crea una plantilla de lanzamiento con un ID de imagen, un tipo de instancia y un grupo de seguridad
            específicos, lo que demuestra una configuración de infraestructura bien planificada y ejecutada.</td>
    </tr>
    <tr>
        <td>Auto Scaling Group</td>
        <td>Se crea un grupo de escalado automático con la capacidad deseada, el tamaño máximo y mínimo, y una plantilla
            de lanzamiento, lo que garantiza un escalado y una gestión eficientes de los recursos.</td>
    </tr>
    <tr>
        <td>Scaling Policy</td>
        <td>Se crea una política de escalado para realizar un seguimiento de la utilización media de la CPU del grupo de
            escalado automático, lo que demuestra un enfoque proactivo para la gestión de recursos.</td>
    </tr>
</table>

<h3 align="center">Seguridad</h3>
<table>
    <tr>
        <th>Requisito</th>
        <th>Descripción</th>
    </tr>
    <tr>
        <td>Security Group</td>
        <td>Se crean cuatro grupos de seguridad con reglas específicas para controlar el tráfico entrante y saliente, lo
            que demuestra una configuración de infraestructura segura.</td>
    </tr>
    <tr>
        <td>LaunchTemplate</td>
        <td>Asociada a un grupo de seguridad específico, lo que garantiza que las instancias lanzadas desde la plantilla
            tengan la configuración de seguridad correcta.</td>
    </tr>
    <tr>
        <td>Auto Scaling Group</td>
        <td>Asociado a un grupo de seguridad específico, lo que garantiza que las instancias lanzadas por el grupo
            tengan la configuración de seguridad correcta.</td>
    </tr>
</table>

<h3 align="center">Fiabilidad</h3>
<table>
    <tr>
        <th>Requisito</th>
        <th>Descripción</th>
    </tr>
    <tr>
        <td>AutoScalingGroup</td>
        <td>Se crea con la capacidad deseada, el tamaño máximo y mínimo, y una plantilla de lanzamiento, lo que
            garantiza que la aplicación pueda escalar para satisfacer las demandas cambiantes.</td>
    </tr>
    <tr>
        <td>Target Group</td>
        <td>Se crea un grupo de destino con una comprobación de estado, lo que garantiza que el equilibrador de carga
            solo enrute a las instancias en buen estado.</td>
    </tr>
    <tr>
        <td>Application Load Balancer (ALB)</td>
        <td>Se crea un ALB con una subred pública y un grupo de seguridad, lo que garantiza que el tráfico se distribuya
            entre varias instancias y zonas de disponibilidad.</td>
    </tr>
</table>

<h3 align="center">Optimización del rendimiento</h3>
<table>
    <tr>
        <th>Requisito</th>
        <th>Descripción</th>
    </tr>
    <tr>
        <td>LaunchTemplate</td>
        <td>Se configura con un tipo de instancia y un ID de imagen específicos, lo que garantiza que las instancias
            estén optimizadas para el rendimiento.</td>
    </tr>
    <tr>
        <td>AutoScalingGroup</td>
        <td>Se configura con la capacidad deseada, el tamaño máximo y mínimo, y una plantilla de lanzamiento, lo que
            garantiza que los recursos estén optimizados para el rendimiento.</td>
    </tr>
    <tr>
        <td>TargetGroup</td>
        <td>Se configura con una comprobación de estado, lo que garantiza que el balanceador de carga solo enrute a las
            instancias en buen estado, lo que optimiza el rendimiento.</td>
    </tr>
</table>

<h3 align="center" >Optimización de costos</h3>
    <table>
        <tr>
            <th>Requisito</th>
            <th>Descripción</th>
        </tr>
        <tr>
            <td>LaunchTemplate</td>
            <td>Se configura con un tipo de instancia específico, lo que garantiza que los recursos estén optimizados para
                el costo.</td>
        </tr>
        <tr>
            <td>AutoScalingGroup</td>
            <td>Se configura con la capacidad deseada, el tamaño máximo y mínimo, y una plantilla de lanzamiento, lo que
                garantiza que los recursos estén optimizados para el costo.</td>
        </tr>
        <tr>
            <td>Policy</td>
            <td>Se configura para realizar un seguimiento de la utilización media de la CPU del grupo de escalado
                automático, lo que garantiza que los recursos estén optimizados para el costo.</td>
        </tr>
    </table>


> [!NOTE]
> Security Group:
> 4 grupos de seguridad:
> SGbookPublic: permite el tráfico SSH y HTTP desde cualquier lugar (0.0.0.0/0)
> SGbookPrivate: permite el tráfico SSH y HTTP desde SGbookPublic y SGalb
> SGalb: permite el tráfico HTTP desde cualquier lugar (0.0.0.0/0)
> SGdb: permite el tráfico MySQL desde SGbookPrivate

```
Resources:
#Create the SG for instance

  SGbookPublic:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: Allow connection through SSH
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: 22
          ToPort: 22
          CidrIp: 0.0.0.0/0
        - IpProtocol: tcp
          FromPort: 5000
          ToPort: 5000
          CidrIp: 0.0.0.0/0
      Tags:
        - Key: Name
          Value: sg-book-ws
      VpcId:
        Fn::ImportValue:
            !Sub "aws-stack-VPCID"

  #Create the SG for instance in subnet private
  SGbookPrivate:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: Allow connection through SSH and HTTP for instance un subnet private
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: 22
          ToPort: 22
          SourceSecurityGroupId: !GetAtt SGbookPublic.GroupId
        - IpProtocol: tcp
          FromPort: 5000
          ToPort: 5000
          SourceSecurityGroupId: !GetAtt SGalb.GroupId
      Tags:
        - Key: Name
          Value: sg-book-private
      VpcId:
        Fn::ImportValue:
            !Sub "aws-stack-VPCID"

  #Create the SG for ALB
  SGalb:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: Allow connection through HTTP
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: 80
          ToPort: 80
          CidrIp: 0.0.0.0/0
      Tags:
        - Key: Name
          Value: sg-alb
      VpcId:
        Fn::ImportValue:
            !Sub "aws-stack-VPCID"


  #Create the SG for DB
  SGdb:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: Allow connection through SSH and MYSQL for DB in subnet private
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: 3306
          ToPort: 3306
          SourceSecurityGroupId: !GetAtt SGbookPrivate.GroupId
      Tags:
        - Key: Name
          Value: sg-db
      VpcId:
        Fn::ImportValue:
            !Sub "aws-stack-VPCID"

```

> [!NOTE]
> Intancias:

```
bookWSpublic:
    Type: AWS::EC2::Instance
    Properties:
      AvailabilityZone: us-east-1a
      ImageId: ami-0bb84b8ffd87024d8
      InstanceType: t2.micro
      IamInstanceProfile: LabInstanceProfile
      KeyName: vockey
      NetworkInterfaces:
        - AssociatePublicIpAddress: true
          DeviceIndex: 0
          SubnetId:
            Fn::ImportValue:
                !Sub "aws-stack-PublicSubnetA"
          GroupSet:
            - Ref: SGbookPublic
      Tags:
        - Key: Name
          Value: book-ws-public
      UserData:
        Fn::Base64: !Sub |
          #!/bin/bash
          sudo dnf install -y python3.9-pip
          pip install virtualenv
          sudo dnf install -y mariadb105-server
          sudo service mariadb start
          sudo chkconfig mariadb on
          pip install flask
          pip install mysql-connector-python
          pip install boto3
          wget https://jav-bucket-web.s3.amazonaws.com/python-db-ssm.zip
          wget https://jav-bucket-web.s3.amazonaws.com/databases.zip
          sudo unzip python-db-ssm.zip
          sudo unzip databases.zip
          sudo mv python-db-ssm databases /home/ec2-user
          wget https://jav-bucket-web.s3.amazonaws.com/bookapp.service
          sudo mv bookapp.service /etc/systemd/system
          sudo systemctl daemon-reload
          sudo systemctl start bookapp
          sudo systemctl enable bookapp
```

> [!NOTE]
> LaunchTemplate:

```
 LaunchTemplateBook:
    Type: AWS::EC2::LaunchTemplate
    Properties:
      LaunchTemplateData:
        IamInstanceProfile:
          Name: LabInstanceProfile
        ImageId: ami-0bb84b8ffd87024d8
        KeyName: vockey
        InstanceType: t2.micro
        SecurityGroupIds:
          - Ref: SGbookPrivate
        UserData:
          Fn::Base64: !Sub |
            #!/bin/bash
            sudo dnf install -y python3.9-pip
            pip install virtualenv
            sudo dnf install -y mariadb105-server
            sudo service mariadb start
            sudo chkconfig mariadb on
            pip install flask
            pip install mysql-connector-python
            pip install boto3
            wget https://jav-bucket-web.s3.amazonaws.com/python-db-ssm.zip
            wget https://jav-bucket-web.s3.amazonaws.com/databases.zip
            sudo unzip python-db-ssm.zip
            sudo unzip databases.zip
            sudo mv python-db-ssm databases /home/ec2-user
            wget https://jav-bucket-web.s3.amazonaws.com/bookapp.service
            sudo mv bookapp.service /etc/systemd/system
            sudo systemctl daemon-reload
            sudo systemctl start bookapp
            sudo systemctl enable bookapp
      LaunchTemplateName: lt-book

```

> [!NOTE]
> Application Load Balancer (ALB):

```
ALBbook:
    Type: AWS::ElasticLoadBalancingV2::LoadBalancer
    Properties:
      Name: alb-cafe
      Scheme: internet-facing
      SecurityGroups:
        - Ref: SGalb
      Subnets:
        - Fn::ImportValue: !Sub "aws-stack-PublicSubnetA"
        - Fn::ImportValue: !Sub "aws-stack-PublicSubnetB"
      Type: application
```

> [!NOTE]
> Target Group:

```
TGelb:
    Type: AWS::ElasticLoadBalancingV2::TargetGroup
    Properties:
      HealthCheckEnabled: true
      HealthCheckPath: /health
      Name: tg-wsbook
      Port: 5000
      Protocol: HTTP
      TargetType: instance
      VpcId:
        Fn::ImportValue:
            !Sub "aws-stack-VPCID"
```

> [!NOTE]
> Listener

```
ListenerALB:
    Type: AWS::ElasticLoadBalancingV2::Listener
    Properties:
      LoadBalancerArn:
        Ref: ALBbook
      Port: 80
      Protocol: HTTP
      DefaultActions:
        - Type: forward
          TargetGroupArn:
            Ref: TGelb
```

> [!IMPORTANT]
> Auto Scaling group

```
ASGbook:
    Type: AWS::AutoScaling::AutoScalingGroup
    Properties:
      AutoScalingGroupName: asg-book
      DesiredCapacity: 2
      MaxSize: 4
      MinSize: 2
      LaunchTemplate:
        LaunchTemplateId:
          Ref: LaunchTemplateBook
        Version: !GetAtt LaunchTemplateBook.LatestVersionNumber
      TargetGroupARNs:
        - Ref: TGelb
      VPCZoneIdentifier:
        - Fn::ImportValue: !Sub "aws-stack-PrivateSubnetA"
        - Fn::ImportValue: !Sub "aws-stack-PrivateSubnetB"
```

> [!NOTE]
> Scaling Policy

```
ScalingPolicyASG:
    Type: AWS::AutoScaling::ScalingPolicy
    Properties:
      AutoScalingGroupName:
        Ref: ASGbook
      PolicyType: TargetTrackingScaling
      TargetTrackingConfiguration:
        PredefinedMetricSpecification:
          PredefinedMetricType: ASGAverageCPUUtilization
        TargetValue: 25
```


<h2>
    <a href="https://aws.amazon.com/codepipeline/"> AWS CodePipeLine </a>
</h2>
<img  height="350" width="1000"src="img/codepipeline" alt="">

<p>
    1. Se crea el repositorio en codecommit (tener en cuenta el doble guión).
    1.1 Para ver los repositorios creados.
    1.2 Para obtener información del repositorio
    2. Se clona el repositorio, para obtener la carpeta a trabajar.
    3. Creación de los archivos network.yml & aplication.yml
    3.1 Validacion del Template
    3.2 Realizamos el push al repositorio (add. , git commit, git push).
    4. Configuramos el pipeline, en aws es codePipeline. Esto con el fin de que si se da un
    push, la infraestructura se desplegará automáticamente. Revisar GuiaPipeline.pdf

</p>

```
1. aws codecommit create-repository --repository-name infraestructura-aws
--repository-description "crear infraestructura en aws"
1.1 aws codecommit list-repositories
1.2 aws codecommit get-repository --repository-name infraestructura-aws
2. git clone "link del repositorio"
3.1 aws cloudformation validate-template --template-body file://network.yml
3.2 git push codecommit::us-east-1://infraestructura-aws
python3 app.py
```

<p>
    Ahora podras observar los recursos desplegados de forma correcta en AWS Cloudformation.
</p>

<h2 href = "https://docs.aws.amazon.com/cloudwatch/">
    <a href="https://docs.aws.amazon.com/cloudwatch/"> Control CloudWatch </a> 
</h2>

<h4>
    Amazon CloudWatch es una herramienta de supervisión que permite monitorear el rendimiento de las aplicaciones, responder a cambios en el desempeño, optimizar el uso de recursos y proporcionar información detallada sobre el estado operativo. Al recopilar datos de todos los recursos de AWS, CloudWatch ofrece una visión completa del rendimiento del sistema, permitiendo a los usuarios configurar alertas, responder automáticamente a cambios y obtener una visión unificada del estado operativo. Revisar GuiaCloudWatch.pdf
</h4>
