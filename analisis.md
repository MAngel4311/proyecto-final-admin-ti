
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

### 4.2. Servicio NTP

### 4.3. Servicio NFS

### 4.4. Servicio NIS

### 4.5. Servicio CUPS

### 4.6. Servicio Samba

### 4.7. Base de datos

## 5. Tabla de requisitos técnicos

## 6. Arquitectura propuesta

## 7. Justificación de la solución
