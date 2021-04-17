### Terminology
- Tenant - An instance of Azure AD and represents a single organization.
- Azure AD Directory - Each tenant has a dedicated Directory. This is used to perform identity and access management functions for resources. 
- Subscriptions - It is used to pay for services. There can be multiple subscriptions in a Directory.
- Core Domain - The initial domain name <tenant>.onmicrosoft.com is the core domain. it is possible to define custom domain names too.
- Azure resourced are divided into four levels:
  - Management groups
    - Management groups are used to manage multiple subscriptions. 
    - All subscriptions inherit the conditions applied to the management group. 
    - All subscriptions within a single management group belong to the same Azure tenant.
    - A management group can be placed in a lower hierarchy of another management group.
    - There is a single top-level management group - Root management group - for each directory in Azure.
  - Subscriptions
    - An Azure subscription is a logical unit of Azure services that links to an Azure account. 
    - An Azure subscription is a billing and/or access control boundary in an Azure AD Directory. 
    - An Azure AD Directory may have multiple subscriptions but each subscription can only trust a single directory.
    - An Azure role applied at the subscription level applies to all the resources within the subscription.
  - Resource groups
    - A resource group acts as a container for resources. 
    - In Azure, all the resources must be inside a resource group and can belong only to a group. 
    - If a resource group is deleted, all the resources inside it are also deleted. 
    - A resource group has its own Identity and Access Management settings for providing role based access. An Azure role applied to the resource group applied to all the resources in the group.
  - Resources
    - A resource is a deployable item in Azure like VMs, App Services, Storage Accounts etc. 
- Managed identity
  - Azure provides the ability to assign Managed Identities to resources like app service, function apps, virtual machines etc. 
  - Managed Identity uses Azure AD tokens to access other resources (like key vaults, storage accounts) that support Azure AD authentication. 
  - It is a service principal of special type that can be used with Azure resources. 
  - Managed Identity can be system-assigned (tied to a resource and cannot be shared with other resources) or user-assigned (independent life cycle and can be share across resources).
-Azure Resource manager
  - It is the client neutral deployment and management service for Azure that is used for lifecycle management (creating, updating and deleting) and access control of of resources.
  - ARM templates can be used for consistent and dependency-defined redeployment of resources.
- Note: A global administration can always elevate their privileges to the Root management group