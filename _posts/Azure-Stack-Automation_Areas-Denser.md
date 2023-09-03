@startuml
!define ICONURL https://raw.githubusercontent.com/rabelenda/cicon-plantuml-sprites/v1.0.0/cicon/
!define ADMINISTRATION [<<CICON.Microsoft>>\nAdministration]
!define DEVELOPMENT [<<CICON.Microsoft>>\nDevelopment]
!define MONITORING [<<CICON.Microsoft>>\nMonitoring]
!define IDENTITY [<<CICON.Microsoft>>\nIdentity]
!define NETWORKING [<<CICON.Microsoft>>\nNetworking]
!define SECURITY [<<CICON.Microsoft>>\nSecurity]
!define STORAGE [<<CICON.Microsoft>>\nStorage]
!define DATABASE [<<CICON.Microsoft>>\nDatabase]
!define CUSTOMER [<<CICON.Microsoft>>\nAzure Customer]

node "Azure Customer" {
    frame "Systems Administration on Microsoft Azure" {
        frame "Administration" as ADMINISTRATION_NODE {
            frame "Subscription Management" as SUBSCRIPTION_NODE
            frame "Resource Management" as RESOURCE_NODE
            frame "Role-Based Access Control" as RBAC_NODE
            frame "Policy Management" as POLICY_NODE
        }
        
        frame "Development" as DEVELOPMENT_NODE {
            frame "Azure DevOps" as AZURE_DEVOPS_NODE
            frame "Azure API Management" as API_MANAGEMENT_NODE
            frame "Azure Functions" as FUNCTIONS_NODE
        }
        
        frame "Monitoring" as MONITORING_NODE {
            frame "Azure Monitor" as MONITOR_NODE
            frame "Azure Log Analytics" as LOG_ANALYTICS_NODE
            frame "Azure Service Health" as SERVICE_HEALTH_NODE
            frame "Azure Advisor" as ADVISOR_NODE
        }
        
        frame "Identity" as IDENTITY_NODE {
            frame "Azure Active Directory" as AAD_NODE
            frame "Azure AD Domain Services" as ADDS_NODE
        }
        
        frame "Networking" as NETWORKING_NODE {
            frame "Azure Virtual Network" as VIRTUAL_NETWORK_NODE
            frame "Azure Load Balancer" as LOAD_BALANCER_NODE
            frame "Azure Traffic Manager" as TRAFFIC_MANAGER_NODE
            frame "Azure VPN Gateway" as VPN_GATEWAY_NODE
        }
        
        frame "Security" as SECURITY_NODE {
            frame "Azure Security Center" as SECURITY_CENTER_NODE
            frame "Azure Firewall" as FIREWALL_NODE
            frame "Azure DDoS Protection" as DDOS_PROTECTION_NODE
            frame "Azure Key Vault" as KEY_VAULT_NODE
        }
        
        frame "Storage" as STORAGE_NODE {
            frame "Azure Blob Storage" as BLOB_STORAGE_NODE
            frame "Azure File Storage" as FILE_STORAGE_NODE
            frame "Azure Queue Storage" as QUEUE_STORAGE_NODE
            frame "Azure Table Storage" as TABLE_STORAGE_NODE
        }
        
        frame "Database" as DATABASE_NODE {
            frame "Azure SQL Database" as SQL_NODE
            frame "Azure Cosmos DB" as COSMOS_NODE
            frame "Azure Database for MySQL" as MYSQL_NODE
            frame "Azure Database for PostgreSQL" as POSTGRESQL_NODE
        }
    }
}

CUSTOMER --> ADMINISTRATION_NODE
CUSTOMER --> DEVELOPMENT_NODE
CUSTOMER --> MONITORING_NODE
CUSTOMER --> IDENTITY_NODE
CUSTOMER --> NETWORKING_NODE
CUSTOMER --> SECURITY_NODE
CUSTOMER --> STORAGE_NODE
CUSTOMER --> DATABASE_NODE
@enduml
