
# Análisis de infraestructura TI

## 1. Introducción

El presente documento tiene como propósito analizar y proponer una infraestructura de Tecnologías de la Información (TI) para la Corporación Autónoma Regional del Quindío (CRQ), entidad pública con sede en Armenia, Quindío, encargada de ejercer la autoridad ambiental en el departamento.

La propuesta busca diseñar una infraestructura que permita centralizar la administración de diferentes servicios tecnológicos, facilitando la disponibilidad de los recursos, el intercambio de información y la gestión de los servicios utilizados por la organización.

Para ello, se plantea la implementación de una solución basada en Dokploy como plataforma de gestión y despliegue de aplicaciones, complementada con servicios tradicionales de Linux sobre Ubuntu Server. La arquitectura contempla servicios web, sincronización horaria, almacenamiento compartido, autenticación centralizada, administración de impresión y gestión de bases de datos.

El proyecto busca aplicar los conocimientos de administración de infraestructura de TI mediante la configuración, integración y documentación de los servicios propuestos.

## 2. Descripción de la empresa

La Corporación Autónoma Regional del Quindío (CRQ) es una entidad pública del orden regional, ubicada en Armenia, Quindío, encargada de administrar los recursos naturales renovables y promover la protección del medio ambiente dentro de su jurisdicción.

Entre sus funciones se encuentran la ejecución de políticas, planes y programas ambientales, la conservación de los recursos naturales y el seguimiento al cumplimiento de la normativa ambiental.

La CRQ cuenta con antecedentes documentados de un Sistema Integrado de Gestión (SIG), orientado al mejoramiento de sus procesos institucionales y a la calidad de los servicios prestados. Su Manual de Calidad de 2017 contempla referentes como ISO 9001 e ISO 14001, entre otras normas.

En este contexto, la infraestructura tecnológica representa un componente de apoyo para el desarrollo de las actividades administrativas y misionales de la organización, facilitando el almacenamiento, intercambio, disponibilidad y administración de la información.

## 3. Análisis de necesidades

Considerando las funciones institucionales de la CRQ y el alcance establecido para el presente proyecto, se propone diseñar una infraestructura tecnológica que permita centralizar la administración de servicios y facilitar el acceso a los recursos compartidos de la organización.

A partir de este contexto, se identifican las siguientes necesidades que serán atendidas mediante la solución propuesta:

- **Disponibilidad de servicios web:** disponer de un servicio que permita publicar y consultar contenido institucional mediante conexiones seguras HTTPS.
- **Sincronización horaria:** mantener una referencia de tiempo común entre los servidores y equipos de la infraestructura.
- **Almacenamiento compartido:** proporcionar espacios centralizados para almacenar y consultar archivos desde equipos Linux.
- **Administración de usuarios:** implementar un mecanismo de autenticación centralizada que facilite la gestión de cuentas de usuario.
- **Gestión de impresión:** centralizar la administración de impresoras y colas de impresión para los usuarios autorizados.
- **Compartición de archivos:** facilitar el intercambio de información entre equipos Windows y otros dispositivos compatibles.
- **Gestión de bases de datos:** disponer de un servicio de base de datos para almacenar y consultar información utilizada por las aplicaciones.
- **Administración de aplicaciones:** utilizar Dokploy para gestionar el despliegue y la administración de aplicaciones y servicios web.

Estas necesidades constituyen la base para definir los servicios tecnológicos, los requisitos técnicos y la arquitectura de infraestructura que se desarrollarán en el proyecto.

## 4. Servicios de infraestructura propuestos

### 4.1. Servicio Web

La infraestructura propuesta contempla la implementación de un servidor web mediante Nginx, gestionado a través de Dokploy, con el propósito de alojar y publicar un sitio web relacionado con la Corporación Autónoma Regional del Quindío (CRQ).

Este servicio permitirá disponer de un espacio web para presentar información institucional, facilitando el acceso al contenido desde los equipos de la red y otros usuarios autorizados. Además, se configurará el acceso mediante HTTPS, utilizando un certificado SSL/TLS para proteger la comunicación entre los clientes y el servidor.

La implementación de este servicio busca garantizar la disponibilidad del sitio web, facilitar su administración y proporcionar un entorno de publicación seguro y organizado.

### 4.2. Servicio NTP

El servicio NTP (Network Time Protocol) permitirá sincronizar los relojes de los servidores y equipos clientes de la infraestructura tecnológica, utilizando un servidor central como referencia horaria.

Para la propuesta de infraestructura de la CRQ, se plantea configurar un servicio NTP en el servidor Linux, encargado de obtener la hora de fuentes de tiempo externas y distribuirla a los equipos de la red local.

La implementación de este servicio permitirá mantener una referencia horaria uniforme entre los dispositivos, facilitando la organización de los registros del sistema, la revisión de eventos y la administración de los servicios tecnológicos.

Su implementación contribuirá a mantener la coherencia temporal de las operaciones realizadas en los diferentes componentes de la infraestructura.

### 4.3. Servicio NFS

El servicio NFS (Network File System) permitirá compartir directorios y archivos entre el servidor Linux y los equipos clientes que utilicen este sistema operativo, facilitando el acceso centralizado a los recursos almacenados en la infraestructura.

Para la propuesta de infraestructura de la CRQ, se plantea configurar un servidor NFS que proporcione un espacio de almacenamiento compartido para los usuarios y equipos autorizados de la red local.

La implementación de este servicio facilitará el intercambio de archivos, evitará la duplicación innecesaria de información y permitirá que diferentes equipos accedan a los directorios compartidos sin necesidad de mantener copias independientes de los documentos.

De esta manera, NFS contribuirá a organizar el almacenamiento de información y facilitar su disponibilidad entre los equipos Linux de la infraestructura.

### 4.4. Servicio NIS

El servicio NIS (Network Information Service) permitirá centralizar la información de usuarios, grupos y otros datos de configuración utilizados por los equipos Linux de la infraestructura.

Para la propuesta de infraestructura de la CRQ, se plantea configurar un servidor NIS que proporcione información de usuarios a los equipos clientes autorizados, evitando la necesidad de administrar de manera independiente estas cuentas en cada dispositivo.

La implementación de este servicio facilitará la administración de usuarios dentro de la red local, permitiendo mantener una gestión más organizada de las cuentas y simplificando el acceso a los recursos compartidos.

De esta manera, NIS contribuirá a centralizar la información de identificación de usuarios y a facilitar la administración de los equipos Linux que formen parte de la infraestructura propuesta.

### 4.5. Servicio CUPS

El servicio CUPS (Common UNIX Printing System) permitirá centralizar la administración de las impresoras y los trabajos de impresión dentro de la infraestructura tecnológica.

Para la propuesta de infraestructura de la CRQ, se plantea configurar un servidor de impresión sobre Linux que permita gestionar las impresoras disponibles en la red, administrar las colas de impresión y facilitar el acceso de los usuarios autorizados a estos recursos.

La implementación de este servicio contribuirá a organizar las tareas de impresión, simplificar la administración de los dispositivos y facilitar el control de los trabajos enviados desde los equipos clientes.

De esta manera, CUPS permitirá disponer de un servicio de impresión centralizado y administrado desde el servidor Linux.

### 4.6. Servicio Samba

El servicio Samba permitirá compartir archivos y directorios entre el servidor Linux y los equipos clientes que utilicen sistemas operativos Windows, facilitando el intercambio de información dentro de la red local.

Para la propuesta de infraestructura de la CRQ, se plantea configurar un servidor Samba que proporcione carpetas compartidas a los usuarios autorizados, estableciendo permisos de acceso y escritura de acuerdo con las necesidades de la organización.

La implementación de este servicio facilitará el intercambio de documentos entre diferentes sistemas operativos, centralizará el almacenamiento de archivos compartidos y permitirá organizar el acceso a la información desde los equipos clientes.

De esta manera, Samba contribuirá a mejorar la interoperabilidad entre los dispositivos de la infraestructura y facilitará la gestión de los recursos compartidos.

### 4.7. Base de datos

La infraestructura propuesta contempla la implementación de un servicio de base de datos relacional mediante MySQL o PostgreSQL, gestionado a través de Dokploy, con el propósito de almacenar y administrar la información utilizada por las aplicaciones desplegadas.

Para la propuesta de infraestructura de la CRQ, se plantea disponer de una base de datos que permita organizar la información institucional utilizada por la aplicación web, facilitando las operaciones de consulta, registro, actualización y administración de los datos.

La base de datos se integrará con el backend de la aplicación, encargado de procesar las solicitudes y establecer la comunicación con el sistema de almacenamiento. Asimismo, se restringirá el acceso directo a la base de datos, permitiendo únicamente las conexiones autorizadas desde los componentes correspondientes.

La implementación de este servicio contribuirá a centralizar la información, facilitar su administración y proporcionar un mecanismo estructurado para el almacenamiento de los datos utilizados por la aplicación.
                                
## 5. Tabla de requisitos técnicos

La siguiente tabla presenta los requisitos técnicos de comunicación de los servicios propuestos para la infraestructura de la CRQ. Se especifican los puertos y protocolos utilizados por cada servicio, así como las direcciones IP correspondientes a los servidores donde serán implementados.

Las direcciones IP se definirán durante la configuración de la infraestructura, teniendo en cuenta la asignación de red y la distribución de los servicios entre las máquinas virtuales.


| N.º | Servicio | Dirección IP | Puerto | Protocolo | Tipo de servicio |
|---|---|---|---|---|---|
| 1 | Web (Nginx) | Por definir | 80 / 443 | TCP | HTTP / HTTPS |
| 2 | NTP | Por definir | 123 | UDP | Sincronización horaria |
| 3 | NFS (v4) | Por definir | 2049 | TCP | Compartición de archivos Linux |
| 4 | NIS | Por definir | 111 / 834* | RPC / TCP / UDP | Información centralizada de usuarios |
| 5 | CUPS | Por definir | 631 | TCP | Impresión mediante IPP |
| 6 | Samba | Por definir | 445 | TCP | Compartición de archivos SMB |
| 7 | MySQL | Por definir | 3306 | TCP | Base de datos |
| 8 | PostgreSQL | Por definir | 5432 | TCP | Base de datos |


## 6. Arquitectura propuesta

La arquitectura propuesta para la infraestructura tecnológica de la CRQ se organiza en tres componentes principales: la red local, la plataforma de aplicaciones y el servidor Linux encargado de proporcionar los servicios tradicionales de infraestructura.

**Red local de la CRQ:** comprende los equipos clientes que accederán a las aplicaciones y servicios disponibles en la infraestructura. Incluye equipos Linux, Windows y Mac, así como impresoras de red que utilizarán el servicio de impresión centralizado.

**Plataforma de aplicaciones:** está compuesta por Dokploy y Traefik, encargados de gestionar el despliegue y el enrutamiento de las aplicaciones. Dentro de esta plataforma se contemplan un servidor web Nginx para publicar el sitio institucional, un backend API para procesar las solicitudes, un panel administrativo y una base de datos MySQL o PostgreSQL para almacenar la información utilizada por la aplicación.

**Servidor Linux - Servicios de infraestructura:** proporciona los servicios tradicionales necesarios para la administración de los recursos de la red. Incluye NTP para la sincronización horaria, NFS para compartir archivos con clientes Linux, NIS para centralizar información de usuarios y grupos, CUPS para administrar los trabajos de impresión y Samba para compartir archivos con equipos Windows y Mac.

La comunicación entre estos componentes permitirá que los usuarios accedan a las aplicaciones y recursos compartidos de acuerdo con los servicios y permisos configurados. De esta manera, la arquitectura busca centralizar la administración de los servicios tecnológicos y facilitar su disponibilidad dentro de la red local.

La distribución física de los componentes, las direcciones IP y los parámetros de comunicación se establecerán durante la implementación de la infraestructura.


## 7. Justificación de la solución

La infraestructura propuesta permitirá centralizar la administración de los servicios tecnológicos de la CRQ mediante Dokploy y herramientas de Linux. La integración de estos componentes facilitará el despliegue de aplicaciones, el almacenamiento y acceso compartido a la información, la administración de usuarios, la sincronización horaria y la gestión de impresión.

La selección de estas tecnologías responde a los requerimientos del proyecto y permite desarrollar una solución organizada, modular y compatible con Ubuntu Server, incorporando mecanismos de seguridad como HTTPS y control de acceso a los recursos.
