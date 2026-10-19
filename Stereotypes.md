# Stéréotypes standard

Ce document recense les stéréotypes des profils standard, par référentiel puis par famille.
Les trois référentiels correspondent aux trois notions de la [typologie des components](.claude/rules/modelia/Definitions.md#typologie-des-components). Un composant système héberge des contextes applicatifs, qui hébergent des composants applicatifs : dans un modèle, l'élément hébergé est un component interne de son hôte.

Un stéréotype se désigne dans un modèle par `<ProfileName>.<TypeName>`, par exemple `org.mathouic.modelia.architecture.profile.data.applicationcontext.V01_00_000.SqlServerInstance`. Le modèle déclare le profil dans son `metainfo.yaml`, avec le chemin du référentiel :

```yaml
profiles:
  - profilePath: <chemin>/standard-architecture-profil/architectureProfile.applicativeContext
    profileName: org.mathouic.modelia.architecture.profile.data.applicationcontext.V01_00_000
```

> Document généré à partir des fichiers de stéréotypes : il est mis à jour à chaque ajout ou modification d'un stéréotype.

## Sommaire

- [Composants applicatifs](#composants-applicatifs) — `architectureProfile.applicativeComponent/`
- [Contextes applicatifs](#contextes-applicatifs) — `architectureProfile.applicativeContext/`
- [Composants systèmes](#composants-systèmes) — `architectureProfile.system/`

## Composants applicatifs

Référentiel `architectureProfile.applicativeComponent/`. Les éléments logiciels qui rendent un service applicatif et s'exécutent dans un contexte applicatif.

### Exécution (`runtime`)

Profil `org.mathouic.modelia.architecture.profile.runtime.applicative.V01_00_000`

| Icône | Stéréotype | Cible | Méta-informations | Description |
|:---:|---|---|---|---|
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.runtime.applicative.V01_00_000/icons/WebApi_100.png" width="40"> | `WebApi` | component | `version` : string | API web |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.runtime.applicative.V01_00_000/icons/WebApplication_100.png" width="40"> | `WebApplication` | component | `version` : string | Application web |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.runtime.applicative.V01_00_000/icons/Worker_100.png" width="40"> | `Worker` | component | `version` : string | Traitement d'arrière-plan ou batch |

### Données (`data`)

Profil `org.mathouic.modelia.architecture.profile.data.applicative.V01_00_000`

| Icône | Stéréotype | Cible | Méta-informations | Description |
|:---:|---|---|---|---|
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.data.applicative.V01_00_000/icons/BlobContainer_100.png" width="40"> | `BlobContainer` | component | — | Conteneur de blobs |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.data.applicative.V01_00_000/icons/Database_100.png" width="40"> | `Database` | component | `compatibilityLevel` : string<br>`collation` : string | Base de données |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.data.applicative.V01_00_000/icons/FileShare_100.png" width="40"> | `FileShare` | component | — | Partage de fichiers |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.data.applicative.V01_00_000/icons/Schema_100.png" width="40"> | `Schema` | component | — | Schéma d'une base de données |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.data.applicative.V01_00_000/icons/SsisPackage_100.png" width="40"> | `SsisPackage` | component | — | Package SSIS |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.data.applicative.V01_00_000/icons/SsrsReport_100.png" width="40"> | `SsrsReport` | component | — | Rapport SSRS |

### Identité (`identity`)

Profil `org.mathouic.modelia.architecture.profile.identity.applicative.V01_00_000`

| Icône | Stéréotype | Cible | Méta-informations | Description |
|:---:|---|---|---|---|
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.identity.applicative.V01_00_000/icons/AppRegistration_100.png" width="40"> | `AppRegistration` | component | `applicationId` : string | Inscription d'application Entra ID |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.identity.applicative.V01_00_000/icons/EnterpriseApplication_100.png" width="40"> | `EnterpriseApplication` | component | `applicationId` : string | Application d'entreprise Entra ID |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.identity.applicative.V01_00_000/icons/OidcClient_100.png" width="40"> | `OidcClient` | component | `clientId` : string<br>`protocol` : string | Client OpenID Connect ou SAML d'un royaume |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.identity.applicative.V01_00_000/icons/Realm_100.png" width="40"> | `Realm` | component | — | Royaume Keycloak |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.identity.applicative.V01_00_000/icons/RelyingParty_100.png" width="40"> | `RelyingParty` | component | `identifier` : string | Partie de confiance ADFS |

### Azure PaaS (`azure`)

Profil `org.mathouic.modelia.architecture.profile.azure.applicative.V01_00_000`

| Icône | Stéréotype | Cible | Méta-informations | Description |
|:---:|---|---|---|---|
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.azure.applicative.V01_00_000/icons/Certificate_100.png" width="40"> | `Certificate` | component | `expirationDate` : date | Certificat d'un Key Vault |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.azure.applicative.V01_00_000/icons/Function_100.png" width="40"> | `Function` | component | `trigger` : string | Fonction d'une Function App |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.azure.applicative.V01_00_000/icons/ManagedApi_100.png" width="40"> | `ManagedApi` | component | `path` : string<br>`version` : string | API publiée dans API Management |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.azure.applicative.V01_00_000/icons/Secret_100.png" width="40"> | `Secret` | component | — | Secret d'un Key Vault |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.azure.applicative.V01_00_000/icons/Workflow_100.png" width="40"> | `Workflow` | component | — | Workflow d'une Logic App |

### Messagerie (`messaging`)

Profil `org.mathouic.modelia.architecture.profile.messaging.applicative.V01_00_000`

| Icône | Stéréotype | Cible | Méta-informations | Description |
|:---:|---|---|---|---|
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.messaging.applicative.V01_00_000/icons/Exchange_100.png" width="40"> | `Exchange` | component | `exchangeType` : string | Exchange RabbitMQ |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.messaging.applicative.V01_00_000/icons/Queue_100.png" width="40"> | `Queue` | component | — | File de messages |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.messaging.applicative.V01_00_000/icons/Subscription_100.png" width="40"> | `Subscription` | component | — | Abonnement à un topic |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.messaging.applicative.V01_00_000/icons/Topic_100.png" width="40"> | `Topic` | component | — | Topic de publication |

### Observabilité (`observability`)

Profil `org.mathouic.modelia.architecture.profile.observability.applicative.V01_00_000`

| Icône | Stéréotype | Cible | Méta-informations | Description |
|:---:|---|---|---|---|
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.observability.applicative.V01_00_000/icons/Dashboard_100.png" width="40"> | `Dashboard` | component | — | Tableau de bord |

### Poste client (`client`)

Profil `org.mathouic.modelia.architecture.profile.client.applicative.V01_00_000`

| Icône | Stéréotype | Cible | Méta-informations | Description |
|:---:|---|---|---|---|
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.client.applicative.V01_00_000/icons/MobileApp_100.png" width="40"> | `MobileApp` | component | `version` : string | Application mobile |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.client.applicative.V01_00_000/icons/OfficeAddin_100.png" width="40"> | `OfficeAddin` | component | `version` : string | Complément Office |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.client.applicative.V01_00_000/icons/SinglePageApplication_100.png" width="40"> | `SinglePageApplication` | component | `version` : string | Application monopage (SPA) |
| <img src="architectureProfile.applicativeComponent/org.mathouic.modelia.architecture.profile.client.applicative.V01_00_000/icons/TeamsApp_100.png" width="40"> | `TeamsApp` | component | `version` : string | Application Teams |

### Transverse

Profil `org.mathouic.modelia.architecture.profile.applicative.V01_00_000`

Aucun stéréotype pour l'instant.

## Contextes applicatifs

Référentiel `architectureProfile.applicativeContext/`. Les serveurs logiciels sur lesquels s'exécutent les composants applicatifs.

### Exécution (`runtime`)

Profil `org.mathouic.modelia.architecture.profile.runtime.applicationcontext.V01_00_000`

| Icône | Stéréotype | Cible | Méta-informations | Description |
|:---:|---|---|---|---|
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.runtime.applicationcontext.V01_00_000/icons/DotNet_100.png" width="40"> | `DotNet` | component | `version` : string | Runtime .NET (Core / 5+) |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.runtime.applicationcontext.V01_00_000/icons/DotNetFramework_100.png" width="40"> | `DotNetFramework` | component | `version` : string | Runtime .NET Framework 4.x |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.runtime.applicationcontext.V01_00_000/icons/IIS_100.png" width="40"> | `IIS` | component | `version` : string | Serveur web IIS |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.runtime.applicationcontext.V01_00_000/icons/IISSite_100.png" width="40"> | `IISSite` | component | `bindings` : string*<br>`appPool` : string | Site IIS, avec ses liaisons et son pool d'applications |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.runtime.applicationcontext.V01_00_000/icons/Kestrel_100.png" width="40"> | `Kestrel` | component | `version` : string | Serveur web Kestrel d'ASP.NET Core |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.runtime.applicationcontext.V01_00_000/icons/NodeJs_100.png" width="40"> | `NodeJs` | component | `version` : string | Runtime Node.js |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.runtime.applicationcontext.V01_00_000/icons/WindowsService_100.png" width="40"> | `WindowsService` | component | `serviceName` : string<br>`account` : string | Service Windows |

### Données (`data`)

Profil `org.mathouic.modelia.architecture.profile.data.applicationcontext.V01_00_000`

| Icône | Stéréotype | Cible | Méta-informations | Description |
|:---:|---|---|---|---|
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.data.applicationcontext.V01_00_000/icons/AzureCacheForRedis_100.png" width="40"> | `AzureCacheForRedis` | component | `serviceTier` : string | Azure Cache for Redis |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.data.applicationcontext.V01_00_000/icons/AzurePostgreSqlServer_100.png" width="40"> | `AzurePostgreSqlServer` | component | `version` : string<br>`serviceTier` : string | Azure Database for PostgreSQL |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.data.applicationcontext.V01_00_000/icons/AzureSqlManagedInstance_100.png" width="40"> | `AzureSqlManagedInstance` | component | `serviceTier` : string | Azure SQL Managed Instance |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.data.applicationcontext.V01_00_000/icons/AzureSqlServer_100.png" width="40"> | `AzureSqlServer` | component | — | Serveur logique Azure SQL Database |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.data.applicationcontext.V01_00_000/icons/AzureStorageAccount_100.png" width="40"> | `AzureStorageAccount` | component | `kind` : string<br>`replication` : string | Compte de stockage Azure |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.data.applicationcontext.V01_00_000/icons/PostgreSqlServer_100.png" width="40"> | `PostgreSqlServer` | component | `version` : string | Serveur PostgreSQL |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.data.applicationcontext.V01_00_000/icons/Redis_100.png" width="40"> | `Redis` | component | `version` : string | Serveur Redis |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.data.applicationcontext.V01_00_000/icons/SSIS_100.png" width="40"> | `SSIS` | component | `version` : string | SQL Server Integration Services |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.data.applicationcontext.V01_00_000/icons/SSRS_100.png" width="40"> | `SSRS` | component | `version` : string | SQL Server Reporting Services |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.data.applicationcontext.V01_00_000/icons/SqlServerInstance_100.png" width="40"> | `SqlServerInstance` | component | `version` : string<br>`edition` : string<br>`instanceName` : string | Instance MS SQL Server |

### Identité (`identity`)

Profil `org.mathouic.modelia.architecture.profile.identity.applicationcontext.V01_00_000`

| Icône | Stéréotype | Cible | Méta-informations | Description |
|:---:|---|---|---|---|
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.identity.applicationcontext.V01_00_000/icons/ActiveDirectoryDomain_100.png" width="40"> | `ActiveDirectoryDomain` | component | `domainName` : string | Domaine Active Directory |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.identity.applicationcontext.V01_00_000/icons/Adfs_100.png" width="40"> | `Adfs` | component | `version` : string | Active Directory Federation Services |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.identity.applicationcontext.V01_00_000/icons/EntraIdTenant_100.png" width="40"> | `EntraIdTenant` | component | `tenantId` : string | Tenant Microsoft Entra ID |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.identity.applicationcontext.V01_00_000/icons/KeycloakServer_100.png" width="40"> | `KeycloakServer` | component | `version` : string | Serveur Keycloak |

### Azure PaaS (`azure`)

Profil `org.mathouic.modelia.architecture.profile.azure.applicationcontext.V01_00_000`

| Icône | Stéréotype | Cible | Méta-informations | Description |
|:---:|---|---|---|---|
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.azure.applicationcontext.V01_00_000/icons/ApiManagement_100.png" width="40"> | `ApiManagement` | component | `serviceTier` : string | Azure API Management |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.azure.applicationcontext.V01_00_000/icons/AppConfiguration_100.png" width="40"> | `AppConfiguration` | component | — | Azure App Configuration |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.azure.applicationcontext.V01_00_000/icons/AppService_100.png" width="40"> | `AppService` | component | `runtimeStack` : string | Azure App Service |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.azure.applicationcontext.V01_00_000/icons/FunctionApp_100.png" width="40"> | `FunctionApp` | component | `runtimeStack` : string | Azure Function App |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.azure.applicationcontext.V01_00_000/icons/KeyVault_100.png" width="40"> | `KeyVault` | component | — | Azure Key Vault |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.azure.applicationcontext.V01_00_000/icons/LogicApp_100.png" width="40"> | `LogicApp` | component | `plan` : string | Azure Logic App |

### Messagerie (`messaging`)

Profil `org.mathouic.modelia.architecture.profile.messaging.applicationcontext.V01_00_000`

| Icône | Stéréotype | Cible | Méta-informations | Description |
|:---:|---|---|---|---|
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.messaging.applicationcontext.V01_00_000/icons/AzureEventGrid_100.png" width="40"> | `AzureEventGrid` | component | — | Azure Event Grid |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.messaging.applicationcontext.V01_00_000/icons/AzureServiceBus_100.png" width="40"> | `AzureServiceBus` | component | `serviceTier` : string | Namespace Azure Service Bus |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.messaging.applicationcontext.V01_00_000/icons/Kafka_100.png" width="40"> | `Kafka` | component | `version` : string | Cluster Kafka |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.messaging.applicationcontext.V01_00_000/icons/RabbitMq_100.png" width="40"> | `RabbitMq` | component | `version` : string | Serveur RabbitMQ |

### Observabilité (`observability`)

Profil `org.mathouic.modelia.architecture.profile.observability.applicationcontext.V01_00_000`

| Icône | Stéréotype | Cible | Méta-informations | Description |
|:---:|---|---|---|---|
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.observability.applicationcontext.V01_00_000/icons/ApplicationInsights_100.png" width="40"> | `ApplicationInsights` | component | — | Azure Application Insights |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.observability.applicationcontext.V01_00_000/icons/Elasticsearch_100.png" width="40"> | `Elasticsearch` | component | `version` : string | Cluster Elasticsearch |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.observability.applicationcontext.V01_00_000/icons/Grafana_100.png" width="40"> | `Grafana` | component | `version` : string | Serveur Grafana |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.observability.applicationcontext.V01_00_000/icons/LogAnalyticsWorkspace_100.png" width="40"> | `LogAnalyticsWorkspace` | component | `retentionDays` : number | Espace de travail Log Analytics |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.observability.applicationcontext.V01_00_000/icons/Seq_100.png" width="40"> | `Seq` | component | `version` : string | Serveur de logs Seq |

### Poste client (`client`)

Profil `org.mathouic.modelia.architecture.profile.client.applicationcontext.V01_00_000`

| Icône | Stéréotype | Cible | Méta-informations | Description |
|:---:|---|---|---|---|
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.client.applicationcontext.V01_00_000/icons/MobileOS_100.png" width="40"> | `MobileOS` | component | `platform` : string | Système d'exploitation mobile |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.client.applicationcontext.V01_00_000/icons/OfficeHost_100.png" width="40"> | `OfficeHost` | component | `applications` : string* | Application Office hôte (Outlook, Excel…) |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.client.applicationcontext.V01_00_000/icons/Teams_100.png" width="40"> | `Teams` | component | — | Microsoft Teams |
| <img src="architectureProfile.applicativeContext/org.mathouic.modelia.architecture.profile.client.applicationcontext.V01_00_000/icons/WebBrowser_100.png" width="40"> | `WebBrowser` | component | `supportedBrowsers` : string* | Navigateur web |

## Composants systèmes

Référentiel `architectureProfile.system/`. Les éléments d'infrastructure sur lesquels s'exécutent les contextes applicatifs, ou qui assurent leur communication.

Profil `org.mathouic.modelia.architecture.profile.system.V01_00_000`. Ce profil n'est pas découpé en familles ; ses stéréotypes sont regroupés ici par thème.

### Hébergement

| Icône | Stéréotype | Cible | Méta-informations | Description |
|:---:|---|---|---|---|
| <img src="architectureProfile.system/org.mathouic.modelia.architecture.profile.system.V01_00_000/icons/VirtualMachine_100.png" width="40"> | `VirtualMachine` | component | `os` : string<br>`osVersion` : string<br>`size` : string | Machine virtuelle |
| <img src="architectureProfile.system/org.mathouic.modelia.architecture.profile.system.V01_00_000/icons/PhysicalServer_100.png" width="40"> | `PhysicalServer` | component | `os` : string<br>`osVersion` : string | Serveur physique |
| <img src="architectureProfile.system/org.mathouic.modelia.architecture.profile.system.V01_00_000/icons/Container_100.png" width="40"> | `Container` | component | `image` : string | Conteneur |
| <img src="architectureProfile.system/org.mathouic.modelia.architecture.profile.system.V01_00_000/icons/KubernetesCluster_100.png" width="40"> | `KubernetesCluster` | component | `version` : string | Cluster Kubernetes |
| <img src="architectureProfile.system/org.mathouic.modelia.architecture.profile.system.V01_00_000/icons/AzureKubernetesService_100.png" width="40"> | `AzureKubernetesService` | component | `version` : string | Azure Kubernetes Service (AKS) |
| <img src="architectureProfile.system/org.mathouic.modelia.architecture.profile.system.V01_00_000/icons/AzureContainerAppsEnvironment_100.png" width="40"> | `AzureContainerAppsEnvironment` | component | — | Environnement Azure Container Apps |
| <img src="architectureProfile.system/org.mathouic.modelia.architecture.profile.system.V01_00_000/icons/AppServicePlan_100.png" width="40"> | `AppServicePlan` | component | `sku` : string | Plan App Service |

### Réseau

| Icône | Stéréotype | Cible | Méta-informations | Description |
|:---:|---|---|---|---|
| <img src="architectureProfile.system/org.mathouic.modelia.architecture.profile.system.V01_00_000/icons/VirtualNetwork_100.png" width="40"> | `VirtualNetwork` | component | `addressSpace` : string* | Réseau virtuel |
| <img src="architectureProfile.system/org.mathouic.modelia.architecture.profile.system.V01_00_000/icons/Subnet_100.png" width="40"> | `Subnet` | component | `addressPrefix` : string | Sous-réseau |
| <img src="architectureProfile.system/org.mathouic.modelia.architecture.profile.system.V01_00_000/icons/LoadBalancer_100.png" width="40"> | `LoadBalancer` | component | — | Répartiteur de charge |
| <img src="architectureProfile.system/org.mathouic.modelia.architecture.profile.system.V01_00_000/icons/ApplicationGateway_100.png" width="40"> | `ApplicationGateway` | component | `waf` : string | Azure Application Gateway (WAF) |
| <img src="architectureProfile.system/org.mathouic.modelia.architecture.profile.system.V01_00_000/icons/AzureFrontDoor_100.png" width="40"> | `AzureFrontDoor` | component | — | Azure Front Door |
| <img src="architectureProfile.system/org.mathouic.modelia.architecture.profile.system.V01_00_000/icons/Firewall_100.png" width="40"> | `Firewall` | component | — | Pare-feu |
| <img src="architectureProfile.system/org.mathouic.modelia.architecture.profile.system.V01_00_000/icons/ReverseProxy_100.png" width="40"> | `ReverseProxy` | component | `product` : string | Reverse proxy |
| <img src="architectureProfile.system/org.mathouic.modelia.architecture.profile.system.V01_00_000/icons/DnsZone_100.png" width="40"> | `DnsZone` | component | `zoneName` : string | Zone DNS |

### Organisation Azure

| Icône | Stéréotype | Cible | Méta-informations | Description |
|:---:|---|---|---|---|
| <img src="architectureProfile.system/org.mathouic.modelia.architecture.profile.system.V01_00_000/icons/AzureSubscription_100.png" width="40"> | `AzureSubscription` | folder | `subscriptionId` : string | Abonnement Azure |
| <img src="architectureProfile.system/org.mathouic.modelia.architecture.profile.system.V01_00_000/icons/AzureResourceGroup_100.png" width="40"> | `AzureResourceGroup` | folder | `region` : string | Groupe de ressources Azure |
