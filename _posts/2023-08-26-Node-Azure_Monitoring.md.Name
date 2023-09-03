@startuml
!define MONITORING [<<icon-monitoring>> Monitoring]
!define IDENTITY [<<icon-identity>> Identity]
!define NETWORKING [<<icon-networking>> Networking]
!define SECURITY [<<icon-security>> Security]
!define DATABASE [<<icon-database>> Database]
!define APPLICATION [<<icon-application>> Applications]
!define STORAGE [<<icon-storage>> Storage]

!define VM [<<icon-vm>> Virtual Machine]
!define WEBAPP [<<icon-webapp>> Web App]
!define DB [<<icon-sqldatabase>> SQL Database]
!define QUEUE [<<icon-storagequeue>> Storage Queue]
!define AZUREFUNCTION [<<icon-function>> Azure Function]
!define EVENTGRID [<<icon-eventgrid>> Event Grid]
!define APIMANAGEMENT [<<icon-apimanagement>> API Management]
!define LOGANALYTICS [<<icon-loganalytics>> Log Analytics]
!define MONITOR [<<icon-monitor>> Monitor]
!define KEYVAULT [<<icon-keyvault>> Key Vault]

!define SENDER [<<icon-sender>> Sender]
!define RECEIVER [<<icon-receiver>> Receiver]

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
    node "Azure Security Center" as SECURITY_CENTER_NODE {
        VM as SECURITY_CENTER_VM
        WEBAPP as SECURITY_CENTER_WEBAPP
        DB as SECURITY_CENTER_DB
        QUEUE as SECURITY_CENTER_QUEUE
        AZUREFUNCTION as SECURITY_CENTER_FUNCTION
        EVENTGRID as SECURITY_CENTER_EVENTGRID
        APIMANAGEMENT as SECURITY_CENTER_APIMANAGEMENT
        MONITOR as SECURITY_CENTER_MONITOR
        LOGANALYTICS as SECURITY_CENTER_LOGANALYTICS
        KEYVAULT as SECURITY_CENTER_KEYVAULT

        SECURITY_CENTER_VM -- SECURITY_CENTER_DB : bi-directional
        SECURITY_CENTER_WEBAPP -- SECURITY_CENTER_QUEUE : bi-directional
        SECURITY_CENTER_WEBAPP -- SECURITY_CENTER_FUNCTION : bi-directional
        SECURITY_CENTER_EVENTGRID -- SECURITY_CENTER_FUNCTION : bi-directional
        SECURITY_CENTER_EVENTGRID -- SECURITY_CENTER_APIMANAGEMENT : bi-directional
        SECURITY_CENTER_MONITOR -- SECURITY_CENTER_VM : bi-directional
        SECURITY_CENTER_MONITOR -- SECURITY_CENTER_WEBAPP : bi-directional
        SECURITY_CENTER_MONITOR -- SECURITY_CENTER_LOGANALYTICS : bi-directional
        SECURITY_CENTER_KEYVAULT -- SECURITY_CENTER_VM : bi-directional
        SECURITY_CENTER_KEYVAULT -- SECURITY_CENTER_WEBAPP : bi-directional
        SECURITY_CENTER_KEYVAULT -- SECURITY_CENTER_DB : bi-directional
    }
    
    node "Azure Sentinel" as SENTINEL_NODE {
        VM as SENTINEL_VM
        WEBAPP as SENTINEL_WEBAPP
        DB as SENTINEL_DB
        QUEUE as SENTINEL_QUEUE
        AZUREFUNCTION as SENTINEL_FUNCTION
        EVENTGRID as SENTINEL_EVENTGRID
        APIMANAGEMENT as SENTINEL_APIMANAGEMENT
        MONITOR as SENTINEL_MONITOR
        LOGANALYTICS as SENTINEL_LOGANALYTICS
        SECURITY as SENTINEL_SECURITY
        KEYVAULT as SENTINEL_KEYVAULT

        SENTINEL_VM -- SENTINEL_DB : bi-directional
        SENTINEL_WEBAPP -- SENTINEL_QUEUE : bi-directional
        SENTINEL_WEBAPP -- SENTINEL_FUNCTION : bi-directional
        SENTINEL_EVENTGRID -- SENTINEL_FUNCTION : bi-directional
        SENTINEL_EVENTGRID -- SENTINEL_APIMANAGEMENT : bi-directional
        SENTINEL_MONITOR -- SENTINEL_VM : bi-directional
        SENTINEL_MONITOR -- SENTINEL_WEBAPP : bi-directional
        SENTINEL_MONITOR -- SENTINEL_LOGANALYTICS : bi-directional
        SENTINEL_SECURITY -- SENTINEL_VM : bi-directional
        SENTINEL_SECURITY -- SENTINEL_WEBAPP : bi-directional
        SENTINEL_SECURITY -- SENTINEL_DB : bi-directional
        SENTINEL_KEYVAULT -- SENTINEL_VM : bi-directional
        SENTINEL_KEYVAULT -- SENTINEL_WEBAPP : bi-directional
        SENTINEL_KEYVAULT -- SENTINEL_DB : bi-directional
    }
}

node "Identity" as IDENTITY_NODE {
    node "Azure Active Directory" as AAD {
        WEBAPP as AAD_WEBAPP
        AZUREFUNCTION as AAD_FUNCTION
        MONITOR_WEBAPP as AAD_MONITOR_WEBAPP
        MONITOR_FUNCTION as AAD_MONITOR_FUNCTION
        AAD_WEBAPP -- AAD_FUNCTION : bi-directional
        AAD_MONITOR_WEBAPP -- AAD_MONITOR_FUNCTION : bi-directional
    }
node "Azure Key Vault" as KEYVAULT_NODE {
    VM as KEYVAULT_VM
    WEBAPP as KEYVAULT_WEBAPP
    MONITOR as KEYVAULT_MONITOR
    LOGANALYTICS as KEYVAULT_LOGANALYTICS
    SECURITY_CENTER as KEYVAULT_SECURITY_CENTER
    SENTINEL as KEYVAULT_SENTINEL

    KEYVAULT_VM -- KEYVAULT_WEBAPP : bi-directional
    KEYVAULT_MONITOR -- KEYVAULT_VM : bi-directional
    KEYVAULT_MONITOR -- KEYVAULT_WEBAPP : bi-directional
    KEYVAULT_MONITOR -- KEYVAULT_LOGANALYTICS : bi-directional
    KEYVAULT_SECURITY_CENTER -- KEYVAULT_VM : bi-directional
    KEYVAULT_SECURITY_CENTER -- KEYVAULT_WEBAPP : bi-directional
    KEYVAULT_SECURITY_CENTER -- KEYVAULT_LOGANALYTICS : bi-directional
    KEYVAULT_SECURITY_CENTER -- KEYVAULT_SENTINEL : bi-directional
}
}

IDENTITY_NODE -- VNET : bi-directional
VNET -- TRAFFIC_MANAGER : bi-directional
TRAFFIC_MANAGER -- MONITORING_NODE : bi-directional
TRAFFIC_MANAGER -- SECURITY_CENTER_NODE : bi-directional
TRAFFIC_MANAGER -- SENTINEL_NODE : bi-directional
KEYVAULT_NODE -- MONITORING_NODE : bi-directional
KEYVAULT_NODE -- SECURITY_CENTER_NODE : bi-directional
KEYVAULT_NODE -- SENTINEL_NODE : bi-directional

@enduml