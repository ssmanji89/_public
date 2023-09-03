@startmindmap
!define ICONURL https://raw.githubusercontent.com/rabelenda/cicon-plantuml-sprites/v1.0.0/cicon/
!define AWSICONURL https://raw.githubusercontent.com/awslabs/aws-icons-for-plantuml/v19.08.08/dist/
!define ICONSIZE 32

skinparam defaultTextAlignment center
skinparam ArrowColor #777777
skinparam ArrowFontColor #777777
skinparam NodeBorderWidth 1
skinparam NodeBorderColor #777777
skinparam NodeBackgroundColor #FFFFFF
skinparam NodeMargin 5
skinparam NodePadding 5

!define ETL [<<CICON.Microservice>>\nETL Pipeline]
!define GATEWAY [<<CICON.AWS>>\nAPI Gateway]
!define DATABASE [<<CICON.AWS>>\nDatabases]
!define AUTOMATION [<<CICON.Business>>\nBusiness Process Automation Services]
!define MANAGER [<<CICON.Business>>\nIntegrations Manager]

* Integrations Manager
** Business Process Automation Services
*** RPA Tools
*** Workflow Management
*** Intelligent Automation
** API Gateway
*** API Design
*** Security & Authorization
*** Traffic Management
** Databases
*** Data Storage
*** Data Management
*** Data Warehousing
** ETL Pipeline
*** Data Extraction
*** Data Transformation
*** Data Loading
@endmindmap
