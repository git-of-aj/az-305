## types of Azure SQL: https://learn.microsoft.com/en-us/azure/azure-sql/azure-sql-iaas-vs-paas-what-is-overview?view=azuresql-db#azure-sql-database
![image](https://github.com/Ananyojha/az-305/assets/76782360/bf9a82cd-968b-4f9a-9a13-8e41acf000a7)
1. AZURE SQL DATABASE: A fully managed SQL Server database engine, based on the latest stable Enterprise Edition of SQL Server. SQL Database has two deployment options built on standardized hardware and software that is owned, hosted, and maintained by Microsoft. 2 OPTIONS FOR HOSTING --a. Instance b. ELASTIC POOL:An elastic pool, which is a collection of databases with a shared set of resources


## DTU vs Vcore Purchase Model => [MS DOCS](https://learn.microsoft.com/en-us/azure/azure-sql/database/service-tiers-sql-database-vcore?view=azuresql-db#compare-vcore-and-dtu-purchasing-models)
> choose the vCore-based model when you need fine-grained control over resources and performance for applications with varying workloads or high-demand periods. On the other hand, opt for the DTU-based model for more straightforward resource management and predictable workloads where you don't need to worry about specific resource configurations. The choice ultimately depends on your specific application requirements and the level of control you need over the underlying hardware resources.
In Microsoft Azure SQL Database, you have two options for purchasing and configuring database resources: vCore-based and DTU-based purchasing models. Both models have their advantages and are suited for different use cases. Let's compare the two and provide a real industry use case for each:

1. vCore-Based Model:
   - In the vCore-based model, you select the number of virtual cores (vCores) and the amount of memory directly. This offers more granular control over resource allocation and allows you to scale compute and memory independently.
   - This model is suitable for scenarios where you have specific performance requirements, need to optimize resource utilization, or have variable workloads with unpredictable demand patterns.
   - It provides better visibility and control over the underlying hardware, making it ideal for resource-intensive and mission-critical applications.

   Real Industry Use Case: E-commerce Platform
   An e-commerce platform experiences varying levels of traffic throughout the year, with significant spikes during seasonal sales events. During regular periods, the platform needs moderate performance, but during peak events, it requires substantial computing power to handle increased user traffic, transactions, and data processing. Using the vCore-based model, the platform can provision the exact number of vCores and memory needed during peak times and scale them back down during off-peak periods, optimizing cost efficiency and performance.

2. DTU-Based Model:
   - In the DTU-based model (Database Transaction Units), you choose a predefined performance level based on a combination of CPU, memory, and I/O resources. DTUs are abstracted performance units that simplify resource allocation and management.
   - This model is suitable for scenarios where you don't need to worry about resource-specific configurations and just want a simplified way to allocate resources for your database.
   - It is generally easier to set up and is recommended for applications with consistent and predictable workloads where granular control is not a priority.

   Real Industry Use Case: Blogging Website
   A blogging website with a stable and steady audience experiences consistent traffic throughout the day. The website's resource requirements are not highly variable, and the workload is relatively predictable. The DTU-based model allows the website owner to choose a DTU level that matches the average workload, ensuring adequate performance without the need to fine-tune resource configurations. This simplicity and ease of management are suitable for this scenario.

## Scaling Options
1. SQL elastic database pools:
- The databases in an elastic pool are on a single server and share a set number of resources at a set price.
- [MS DOCS](https://learn.microsoft.com/en-us/azure/azure-sql/database/elastic-pool-overview?view=azuresql)

## AZURE SQL vs Azure SQL Managed Instance
**Key Differences:**

1. **Service Model:**
   - *Azure SQL Database:* Multi-tenant database service designed for cloud-native applications.
   - *Azure SQL Managed Instance:* Offers a dedicated, isolated instance with compatibility for on-premises SQL Server.

2. **Isolation and Compatibility:**
   - *Azure SQL Database:* Provides a shared environment with automatic scaling and tuning, suitable for modern cloud applications.
   - *Azure SQL Managed Instance:* Offers a dedicated instance, ensuring higher isolation and compatibility with on-premises SQL Server features.

3. **Feature Set:**
   - *Azure SQL Database:* Optimized for cloud-native scenarios with features like automatic tuning and serverless options.
   - *Azure SQL Managed Instance:* Supports additional SQL Server features, such as SQL Server Agent, cross-database queries, and CLR assemblies.

**Use Cases:**

1. *Azure SQL Database:*
   - Ideal for cloud-native applications with varying workloads.
   - Well-suited for scenarios where automatic scaling and tuning are crucial.
   - Cost-effective for applications with dynamic resource requirements.

2. *Azure SQL Managed Instance:*
   - Best for applications with dependencies on specific SQL Server features not available in Azure SQL Database.
   - Suitable for scenarios requiring a higher degree of isolation, resembling on-premises SQL Server.
   - When there's a need for a dedicated instance with predictable performance characteristics.

In summary, choose Azure SQL Database for cloud-native applications with dynamic workloads, and opt for Azure SQL Managed Instance when compatibility with specific SQL Server features and a dedicated instance are critical to your application's requirements.

------------------------

## ADF 
Azure Data Factory is a managed cloud service that's built for these complex hybrid extract-transform-load (ETL), extract-load-transform (ELT), and data integration projects
- [DOCS](https://learn.microsoft.com/en-us/azure/data-factory/introduction)
