@startuml
!define ICONURL https://raw.githubusercontent.com/rabelenda/cicon-plantuml-sprites/v1.0.0/cicon/
!define AZUREICONURL https://raw.githubusercontent.com/rabelenda/cicon-plantuml-sprites/v1.0.0/cicon-azure/

!define MONITORING [<<CICON.Microsoft>>\nMonitoring]
!define IDENTITY [<<CICON.Microsoft>>\nIdentity]
!define NETWORKING [<<CICON.Microsoft>>\nNetworking]
!define SECURITY [<<CICON.Microsoft>>\nSecurity]
!define DATABASE [<<CICON.Microsoft>>\nDatabase]
!define APPLICATION [<<CICON.Microsoft>>\nApplications]
!define STORAGE [<<CICON.Microsoft>>\nStorage]

!define VM [<<CICON.Azure VM>>\nVirtual Machine]
!define WEBAPP [<<CICON.Azure Web App>>\nWeb App]
!define DB [<<CICON.Azure SQL Database>>\nSQL Database]
!define QUEUE [<<CICON.Azure Storage Queue>>\nStorage Queue]
!define AZUREFUNCTION [<<CICON.Azure Function>>\nAzure Function]
!define EVENTGRID [<<CICON.Azure Event Grid>>\nEvent Grid]
!define APIMANAGEMENT [<<CICON.Azure API Management>>\nAPI Management]
!define LOGANALYTICS [<<CICON.Azure Log Analytics>>\nLog Analytics]
!define MONITOR [<<CICON.Azure Monitor>>\nMonitor]
!define KEYVAULT [<<CICON.Azure Key Vault>>\nKey Vault]

!define SENDER [<<CICON.Azure Icon Set/Security & Identity/Group-Group of Users>>\nSender]
!define RECEIVER [<<CICON.Azure Icon Set/Security & Identity/User-User>>\nReceiver]

title Monitoring Node Deployment Diagram

package "Azure Customer" {
    node "Monitoring" as MONITORING_NODE {
        node "Azure Monitor" as MONITOR_NODE {
            VM as MONITOR_VM
            WEBAPP as MONITOR_WEBAPP
            DB as MONITOR_DB
            QUEUE as MONITOR_QUEUE
            AZUREFUNCTION as MONITOR_FUNCTION
            EVENTGRID as MONITOR_EVENTGRID
            APIMANAGEMENT as MONITOR_APIMANAGEMENT
            LOGANALYTICS as MONITOR_LOGANALYTICS
            KEYVAULT as MONITOR_KEYVAULT

            MONITOR_VM -- MONITOR_DB : bi-directional
            MONITOR_VM -- MONITOR_QUEUE : bi-directional
            MONITOR_WEBAPP -- MONITOR_QUEUE : bi-directional
            MONITOR_WEBAPP -- MONITOR_FUNCTION : bi-directional
            MONITOR_EVENTGRID -- MONITOR_FUNCTION : bi-directional
            MONITOR_EVENTGRID -- MONITOR_APIMANAGEMENT : bi-directional
            MONITOR_LOGANALYTICS -- MONITOR_VM : bi-directional
            MONITOR_LOGANALYTICS -- MONITOR_WEBAPP : bi-directional
            MONITOR_KEYVAULT -- MONITOR_VM : bi-directional
            MONITOR_KEYVAULT -- MONITOR_WEBAPP : bi-directional
            MONITOR_KEYVAULT -- MONITOR_DB : bi-directional
        }
        
        node "Azure Log Analytics" as LOG_ANALYTICS_NODE {
            VM as LOG_ANALYTICS_VM
            WEBAPP as LOG_ANALYTICS_WEBAPP
            DB as LOG_ANALYTICS_DB
            QUEUE as LOG_ANALYTICS_QUEUE
            AZUREFUNCTION as LOG_ANALYTICS_FUNCTION
            EVENTGRID as LOG_ANALYTICS_EVENTGRID
            APIMANAGEMENT as LOG_ANALYTICS_APIMANAGEMENT
            MONITOR as LOG_ANALYTICS_MONITOR
            KEYVAULT as LOG_ANALYTICS_KEYVAULT
        LOG_ANALYTICS_VM -- LOG_ANALYTICS_DB : bi-directional
        LOG_ANALYTICS_WEBAPP -- LOG_ANALYTICS_QUEUE : bi-directional
        LOG_ANALYTICS_WEBAPP -- LOG_ANALYTICS_FUNCTION : bi-directional
        LOG_ANALYTICS_EVENTGRID -- LOG_ANALYTICS_FUNCTION : bi-directional
        LOG_ANALYTICS_EVENTGRID -- LOG_ANALYTICS_APIMANAGEMENT : bi-directional
        LOG_ANALYTICS_MONITOR -- LOG_ANALYTICS_VM : bi-directional
        LOG_ANALYTICS_MONITOR -- LOG_ANALYTICS_WEBAPP : bi-directional
        LOG_ANALYTICS_KEYVAULT -- LOG_ANALYTICS_VM : bi-directional
        LOG_ANALYTICS_KEYVAULT -- LOG_ANALYTICS_WEBAPP : bi-directional
        LOG_ANALYTICS_KEYVAULT -- LOG_ANALYTICS_DB : bi-directional
    }

    node "Azure Event Grid" as EVENT_GRID_NODE {
        MONITOR as EVENT_GRID_MONITOR
        LOG_ANALYTICS as EVENT_GRID_LOG_ANALYTICS

        EVENT_GRID_MONITOR -- EVENT_GRID_LOG_ANALYTICS : bi-directional
    }
}

CUSTOMER -down-> MONITORING_NODE
MONITORING_NODE -down-> MONITOR_NODE
MONITORING_NODE -down-> LOG_ANALYTICS_NODE
MONITORING_NODE -down-> EVENT_GRID_NODE
}

@enduml