# Smart data course to get the aws data engineer certification

Certifications: https://aws.amazon.com/certification/

Paths: https://d1.awsstatic.com/es_ES/training-and-certification/docs/AWS_certification_paths.pdf

Cloud Practitioner guide: https://d1.awsstatic.com/training-and-certification/docs-cloud-practitioner/AWS-Certified-Cloud-Practitioner_Exam-Guide.pdf

Data Engineer guide: https://d1.awsstatic.com/training-and-certification/docs-data-engineer-associate/AWS-Certified-Data-Engineer-Associate_Exam-Guide.pdf

## Overview about Cloud Computing

Entrega bajo demanda de potencia de cómputo, bases de datos, almacenamiento, aplicaciones y otros recursos de TI, a través de Internet con un sistema de precios de pago por uso.

Infraestructura como hardware -> Infraestructura como software

Six advantages of cloud computing:
* Change CapEx for OpEx
* Beneficio de las ecomonías de escala
* Dejar de adivinar la capacidad
* Incrementar la velocidad y la agilidad
* Dejar de gastar en mantener centros de datos
* Ser global en minutos

Modelos
* On-Premises
* IaaS: EC2, Elastic Compute Cloud
* PaaS: Elastic Beanstalk, implementa y escala aplicaciones web.
* SaaS: AWS does not offer this type of services

Type of clouds:
* Private
* Hybrid
* Public

## Definición de ingeniería de datos

* Diseño, desarrollo, implementación y mantenimiento de sistemas y procesos que toman datos sin procesar y producen alta calidad e información.
* Intersección entre seguridad, gestión de datos, DataOps, arquitectura de datos, orquestación e ingeniería de software.
* Gestiona el ciclo de vida de datos:
    * Ingestion -> Transformation -> Serving
    * Undercurrents: Security, Data management, DataOps, Data architecture, Orchestation, Software engineering

## Big data information

* Volumen
* Velocidad
* Variedad

Tipos de datos: 
* Estructurados: CSV, Tables
* No estructurados: Videos, Audios, Images, Emails, Documents
* Semi estructurados: XML, JSON, Logs, is a mix of structured data and non-structured data

## Data warehouses vs Data lakes

Data warehouse:
* Provienen de diversas fuentes
* Se almacenan ya estructurados
* Diseñado para consultas y análisis complejos
* Los datos se limpian, transforman y cargan (ETL)
* Esquema de estrella o copo de nieve
* Optimizado para operaciones de lectura intensiva

Ejemplos:
* Amazon Redshift

Data Lake:
* No se procesan, vienen en su formato nativo
* Incluye datos estructurados, semiestructurados y no estructurados
* No hay esquema definido
* No hay preprocesamiento
* Extract - Load - Transform
* Admite procesamiento por lotes, en tiempo real y de flujo
* Se puede consultar con fines de transformarción o exploración

Ejemplos:
* Amazon Simple Storage Service (S3)
* S3 -> AWS Glue -> Amazon Athena

Data Lakehouse:
* Admite datos estructurados y no estructurados
* Permite el esquema de escritura y el esquema de lectura
* Por lo general se construyen sobre arquitecturas distribuidas o en la nube
* Llevan transacciones ACID a Big Data
ACID: Atomicity, Consistency, Isoltaion and Durability

Ejemplos:
* AWS Lake Formation (con S3 y Redshift Spectrum)

Data Mesh:
* Gobernanza y organización 
* Productos de datos para casos de uso
* Habla de gestión de datos
* Gestión de datos basadas en dominio

Ejemplos:
* AWS Lake Formation
* AWS Data Exchange
* AWS Glue

## Overview about Big Data AWS

Solution components:
* Datos sin procesar ->
* Ingestar / recopilar ->
* Alamacenamiento ->
* Procesar / analizar ->
* Consumir / Visualizar ->
* Respuestas e información

AWS Big Data Services:
* Ingesta
    - Amazon Kinesis: Ingesta de datos en tiempo real, como streaming.
    - AWS DMS (Database Migration Service): Llevar datos a la nube, migrar información.
    - AWS Snowball: Cargar datos off-line, de manera física.
    - Amazon SQS: Simple Queue Service
    - AWS Direct Connect: Conexión directa entre los servidores privados y la nube
    - AWS IoT Core: 
* Almacenamiento
    - Amazon DynamoDB: NoSQL
    - Amazon S3 - Glacier: Almacenamiento de datos, en general.
    - Amazon RDS:
    - Amazon Elastic Cache: Base de datos en memoria.
* Procesamiento
    - AWS Lambda: Reaccionar a evento.
    - Amazon EMR (Amazon Elastic MapReduce): Procesamiento de aplicaciones Hadoop with spark
    - Amazon ML
    - AWS Glue: ETL serverless
    - AWS Data Pipeline: 
    - Amazon SageMaker
* Análisis y Visualización
    - Amazon OpenSearch: Base de datos de indexamiento
    - Amazon Athena: Consultar datos desde S3 sin cargar los datos
    - Amazon Redshift: Almacen de datos
    - Amazon Quicksight: Dashboard
* Seguridad
    - AWS IAM
    - AWS KMS
    - AWS CloudHSM: Llaves a nivel de hardware
    - Amazon CLoudWatch
    - AWS CloudTrail: Monitorear llamado a APIs.

## Benefits of AWS

* Cómputo: Paga por el tiempo de cómputo
* Almacenamiento: Paga por lo que almacenas
* Transferencia de datos: La entrada de datos es gratuita

Infraestructura global de aws:
- Regiones
- Zonas de disponibilidad
- Puntos de presencia (Edge Location)
- Zonas locales

Acceso:
- Consola + MFA
- CLI
- SDK

## Administración de facturación

- Etiquetas
- Cost Explorer
- Cost explorer informes
- Amazon Budgets and alerts

## Create Budgets

* Create Tags in each service, key-value pairs.

To create budget:
* Billing and Cost Management
* |> Create budget section
* |> Templates (Monthly cost budget)
* |> Create budget