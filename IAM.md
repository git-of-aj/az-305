Governance ensures those rules and policies are enforced.

It helps in Industry standards, such as information security management.
- Corporate or organizational standards

Hierarchy : helps define governance exactly where it's néeded : 
![](https://docs.microsoft.com/en-us/learn/wwl-azure/design-governance/media/governance-strategies.png)

### Management Group : 
- Design management groups with governance in mind. For example, apply Azure policies at the management group level for all workloads that require the same security, compliance, connectivity, and feature settings.

1. Based on your org structure 
![](https://docs.microsoft.com/en-us/learn/wwl-azure/design-governance/media/management-groups.png)
2. Geo location : so you can easily address that country's rules and Regulations
3. Workload type : production / testing 

### subscription 
[Types](https://azure.microsoft.com/en-us/support/legal/offer-details/)

*You can use subscriptions to:*

Organize specialized workloads that need to scale outside the existing [subscription limits](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/azure-subscription-service-limits)

Provide different billing environments such as development, test, and production.

Achieve compliance by applying policies to a subscription.

Manage and track costs for your organizational structure.ypes

![](https://docs.microsoft.com/en-us/learn/wwl-azure/design-governance/media/subscriptions-example.png)

### Resource Group : 
Place resources of similar usage, type, or location in logical groups.

Organize resources by life cycle so all the resources can be created or deleted at the same time.

Apply role permissions to a group of resources or give a group access to administer a group of resources.

Use resource locks to protect individual resources from deletion or change.

[Resource-Group-Design-ideas+Properties](https://docs.microsoft.com/en-us/learn/modules/design-governance/5-design-for-resource-groups)

## Tags : 
ask yourself what you want to accomplish. Will the tags be used for reporting or billing? Perhaps you will use the tags to enable more effective searching? Maybe the tags will be used in automated scripts. Be sure to clearly define your goals.
[TAG EXAMPLES WITH DESCRIPTION](https://docs.microsoft.com/en-us/learn/modules/design-governance/6-design-for-resource-tags)

Pro tip ☑ : Consider using Azure policy to apply tags and enforce tagging rules and conventions. Resource tagging is only effective if it’s used consistently across an organization. You can use Azure policy to require that certain tags be added to new resources as they're provisioned.
