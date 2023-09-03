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
!define KPI [<<CICON.Microsoft>>\nKey Performance Indicators]

node "Azure Customer" {
    frame "Systems Administration on Microsoft Azure" {
        frame "Administration" as ADMINISTRATION_NODE {
            frame "Subscription Management" as SUBSCRIPTION_NODE {
                frame "Cost Management" as COST_MANAGEMENT_NODE
                frame "Budget Control" as BUDGET_CONTROL_NODE
                frame "Spending Forecast" as SPENDING_FORECAST_NODE
            }
            frame "Resource Management" as RESOURCE_NODE {
                frame "Infrastructure Optimization" as INFRA_OPTIMIZATION_NODE
                frame "Deployment Automation" as DEPLOYMENT_AUTOMATION_NODE
                frame "Resource Configuration Management" as RESOURCE_CONFIG_NODE
            }
            frame "Role-Based Access Control" as RBAC_NODE {
                frame "Security and Compliance" as SECURITY_COMPLIANCE_NODE
                frame "Access Control and Audit" as ACCESS_CONTROL_AUDIT_NODE
            }
            frame "Policy Management" as POLICY_NODE {
                frame "Regulatory Compliance" as REGULATORY_COMPLIANCE_NODE
                frame "Resource Governance" as RESOURCE_GOVERNANCE_NODE
            }
        }
        
        frame "Development" as DEVELOPMENT_NODE {
            frame "Azure DevOps" as AZURE_DEVOPS_NODE {
                frame "Code Quality and Security" as CODE_QUALITY_SECURITY_NODE
                frame "Continuous Integration and Deployment" as CI_CD_NODE
                frame "Agile Project Management" as AGILE_PM_NODE
            }
            frame "Azure API Management" as API_MANAGEMENT_NODE {
                frame "API Analytics and Monitoring" as API_ANALYTICS_MONITORING_NODE
                frame "API Security and Access Control" as API_SECURITY_ACCESS_CONTROL_NODE
                frame "API Versioning and Lifecycle Management" as API_VERSION_LIFECYCLE_NODE
            }
            frame "Azure Functions" as FUNCTIONS_NODE {
                frame "Scalability and Performance" as SCALABILITY_PERFORMANCE_NODE
                frame "Serverless Architecture" as SERVERLESS_ARCH_NODE
                frame "Integration with other Services" as SERVICE_INTEGRATION_NODE
            }
        }
        
        frame "Monitoring" as MONITORING_NODE {
            frame "Azure Monitor" as MONITOR_NODE {
                frame "Metrics and Logs" as METRICS_LOGS_NODE
                frame "Alerting and Notification" as ALERTING_NOTIFICATION_NODE
                frame "Dashboarding and Reporting" as DASHBOARD_REPORTING_NODE
            }
            frame "Azure Log Analytics" as LOG_ANALYTICS_NODE {
                frame "Log Collection and Management" as LOG_COLLECTION_MANAGEMENT_NODE
                frame "Custom Log Analysis and Visualization" as CUSTOM_LOG_ANALYSIS_NODE
                frame "Threat Detection and Response" as THREAT_DETECTION_RESPONSE_NODE
            }
            frame "Azure Service Health" as SERVICE_HEALTH_NODE {
                frame "Service IncidentManagement" as SERVICE_INCIDENT_NODE
                frame "Service Level Agreements" as SERVICE_LEVEL_AGREEMENTS_NODE
                frame "Service Performance and Availability" as SERVICE_PERFORMANCE_AVAILABILITY_NODE
            }
            frame "Azure Advisor" as ADVISOR_NODE {
                frame "Security Recommendations" as SECURITY_RECOMMENDATIONS_NODE
                frame "Performance Optimization" as PERFORMANCE_OPTIMIZATION_NODE
                frame "Cost Optimization" as COST_OPTIMIZATION_NODE
            }
        }
        
        frame "Identity" as IDENTITY_NODE {
            frame "Azure Active Directory" as AAD_NODE {
                frame "Identity and Access Management" as IDENTITY_ACCESS_MGMT_NODE
                frame "Single Sign-On and Multi-Factor Authentication" as SSO_MFA_NODE
                frame "Group and Role Management" as GROUP_ROLE_MGMT_NODE
            }
            frame "Azure AD Domain Services" as ADDS_NODE {
                frame "Domain Controller Management" as DOMAIN_CONTROLLER_NODE
                frame "LDAP and Kerberos Integration" as LDAP_KERBEROS_NODE
                frame "Security and Compliance" as SECURITY_COMPLIANCE_NODE
            }
        }
        
        frame "Networking" as NETWORKING_NODE {
            frame "Azure Virtual Network" as VIRTUAL_NETWORK_NODE {
                frame "VNet Design and Implementation" as VNET_DESIGN_IMPLEMENTATION_NODE
                frame "IP Address Management" as IP_ADDRESS_MGMT_NODE
                frame "VNet Peering and Gateway Integration" as VNET_PEERING_GATEWAY_NODE
            }
            frame "Azure Load Balancer" as LOAD_BALANCER_NODE {
                frame "Traffic Distribution and Optimization" as TRAFFIC_DISTRIBUTION_OPTIMIZATION_NODE
                frame "Availability and Redundancy" as AVAILABILITY_REDUNDANCY_NODE
                frame "Health Probes and Diagnostic Logs" as HEALTH_PROBES_DIAG_LOGS_NODE
            }
            frame "Azure Traffic Manager" as TRAFFIC_MANAGER_NODE {
                frame "Global Traffic Management" as GLOBAL_TRAFFIC_MGMT_NODE
                frame "Load Balancing and Failover" as LOAD_BALANCING_FAILOVER_NODE
                frame "DNS and Endpoint Monitoring" as DNS_ENDPOINT_MONITORING_NODE
            }
            frame "Azure VPN Gateway" as VPN_GATEWAY_NODE {
                frame "Secure Site-to-Site and Remote Access VPN" as SECURE_SITE_TO_SITE_REMOTE_ACCESS_VPN_NODE
                frame "High Availability and Disaster Recovery" as HA_DR_NODE
                frame "Traffic Routing and Filtering" as TRAFFIC_ROUTING_FILTERING_NODE
            }
        }
        
        frame "Security" as SECURITY_NODE {
            frame "Azure Security Center" as SECURITY_CENTER_NODE {
                frame "Security Assessment and Recommendations" as SECURITY_ASSESSMENT_RECOMMENDATIONS_NODE
                frame "Threat Detection and Response" as THREAT_DETECTION_RESPONSE_NODE
                frame "Compliance and Policy Management" as COMPLIANCE_POLICY_MGMT_NODE
            }
            frame "Azure Firewall" as FIREWALL_NODE {
                frame "Network Security and Access Control" as NETWORK_SECURITY_ACCESS_CONTROL_NODE
                frame "Application and Threat Intelligence" as APP_THREAT_INTELLIGENCE_NODE
                frame "Centralized Policy Management" as CENTRALIZED_POLICY_MGMT_NODE
            }
            frame "Azure DDoS Protection" as DDOS_PROTECTION_NODE {
                frame "DDoS Attack Detection and Mitigation" as DDOS_ATTACK_MITIGATION_NODE
                frame "Custom Protection Policies" as CUSTOM_PROTECTION_POLICIES_NODE
                frame "Monitoring and Reporting" as MONITORING_REPORTING_NODE
            }
            frame "Azure Key Vault" as KEY_VAULT_NODE {
                frame "Key and Secret Management" as KEY_SECRET_MGMT_NODE
                frame "Certificate Management" as CERTIFICATE_MGMT_NODE
                frame "Role-Based Access Control" as RBAC_NODE1
                frame "Auditing and Monitoring" as AUDITING_MONITORING_NODE
                }
            }
            frame "Storage" as STORAGE_NODE {
                frame "Azure Blob Storage" as BLOB_STORAGE_NODE {
                    frame "Object Storage" as OBJECT_STORAGE_NODE
                    frame "Blob Tiering and Lifecycle Management" as BLOB_TIERING_LIFECYCLE_NODE
                    frame "Data Security and Encryption" as DATA_SECURITY_ENCRYPTION_NODE
                }
                frame "Azure Files" as FILES_NODE {
                    frame "SMB File Sharing" as SMB_FILE_SHARING_NODE
                    frame "Cloud-based File Storage" as CLOUD_BASED_FILE_STORAGE_NODE
                    frame "File Sync and Backup" as FILE_SYNC_BACKUP_NODE
                }
                frame "Azure Queue Storage" as QUEUE_STORAGE_NODE {
                    frame "Message Queues and Asynchronous Processing" as MESSAGE_QUEUES_ASYNC_PROCESSING_NODE
                    frame "Queue-Based Load Leveling" as QUEUE_BASED_LOAD_LEVELING_NODE
                    frame "At-Least-Once Message Delivery" as AT_LEAST_ONCE_MESSAGE_DELIVERY_NODE
                }
                frame "Azure Table Storage" as TABLE_STORAGE_NODE {
                    frame "NoSQL Key-Value Data Store" as NOSQL_KEY_VALUE_DATA_STORE_NODE
                    frame "Scalable and Low-Cost Data Storage" as SCALABLE_LOW_COST_DATA_STORAGE_NODE
                    frame "Flexible Data Schema" as FLEXIBLE_DATA_SCHEMA_NODE
                }
            }
            
            frame "Database" as DATABASE_NODE {
                frame "Azure SQL Database" as SQL_DATABASE_NODE {
                    frame "Relational Database Management" as RELATIONAL_DB_MGMT_NODE
                    frame "High Availability and Disaster Recovery" as HA_DR_NODE
                    frame "Security and Compliance" as SECURITY_COMPLIANCE_NODE
                }
                frame "Azure Cosmos DB" as COSMOS_DB_NODE {
                    frame "Globally Distributed Database" as GLOBALLY_DISTRIBUTED_DB_NODE
                    frame "Multi-Model Database" as MULTI_MODEL_DB_NODE
                    frame "Scalability and Performance" as SCALABILITY_PERFORMANCE_NODE
                }
                frame "Azure Database for MySQL" as MYSQL_DB_NODE {
                    frame "Open-Source Relational Database Management" as OPEN_SOURCE_RELATIONAL_DB_MGMT_NODE
                    frame "High Availability and Security" as HA_SECURITY_NODE11
                    frame "Automated Management and Monitoring" as AUTOMATED_MGMT_MONITORING_NODE
                }
                frame "Azure Database for PostgreSQL" as POSTGRESQL_DB_NODE {
                    frame "Open-Source Relational Database Management" as OPEN_SOURCE_RELATIONAL_DB_MGMT_NODE
                    frame "High Availability and Security" as HA_SECURITY_NODE11
                    frame "Automated Management and Monitoring" as AUTOMATED_MGMT_MONITORING_NODE
                }
            }
            
            frame "Key Performance Indicators" as KPI_NODE {
                frame "Availability" as AVAILABILITY_NODE
                frame "Performance" as PERFORMANCE_NODE
                frame "Scalability" as SCALABILITY_NODE
                frame "Security" as SECURITY_NODE1
                frame "Cost" as COST_NODE
            }
        }
    }

    CUSTOMER -down-> ADMINISTRATION_NODE
    CUSTOMER -down-> DEVELOPMENT_NODE
    CUSTOMER -down-> MONITORING_NODE
    CUSTOMER -down-> IDENTITY_NODE
    CUSTOMER -down-> NETWORKING_NODE
    CUSTOMER -down-> SECURITY_NODE
    CUSTOMER -down-> STORAGE_NODE
    CUSTOMER -down-> DATABASE_NODE
    CUSTOMER -down-> KPI_NODE
    
@enduml        