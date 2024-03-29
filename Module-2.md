# What are Batch Jibs 
Sure! Here are some real industry examples of batch jobs:

1. Financial Processing: Banks and financial institutions often use batch jobs to process large volumes of transactions, such as credit card transactions, account updates, and statement generation overnight or at specific intervals.

2. E-commerce Order Processing: Online retailers use batch jobs to manage inventory updates, process orders, and generate reports on sales and revenue periodically.

3. Data Warehousing: Companies use batch jobs to extract, transform, and load (ETL) data from various sources into a data warehouse for analysis and reporting purposes.

4. Billing and Invoicing: Utility companies and service providers employ batch jobs to generate invoices, calculate charges, and apply discounts for their customers based on usage data.

5. Email Campaigns: Marketing teams often use batch jobs to send out scheduled email campaigns to target audiences, managing the distribution of marketing materials.

6. Social Media Analytics: Companies use batch processing to analyze and extract insights from vast amounts of social media data collected over time.

7. Healthcare Data Processing: Hospitals and healthcare organizations use batch jobs to process patient data, update electronic health records, and generate reports for administrative purposes.

8. Manufacturing: Manufacturers use batch jobs for quality control, analyzing production data, and tracking inventory levels at regular intervals.

# azure batch:  use to run large-scale parallel and high-performance computing (HPC) batch jobs efficiently in Azure
Azure Batch creates and manages a pool of compute nodes (virtual machines), installs the applications you want to run, and schedules jobs to run on the nodes. There's no cluster or job scheduler software to install, manage, or scale. Instead, you use Batch APIs and tools, command-line scripts, or the Azure portal to configure, manage, and monitor your jobs.
> It can Run parallel workloads = intrinsically parallel (also known as "embarrassingly parallel") ==>
>  run independently, with each instance completing part of the work.
> access some common data, but they don't communicate with other instances of the application. exmaple - https://learn.microsoft.com/en-us/azure/batch/batch-technical-overview#run-parallel-workloads

## concepts
1. Job: Preparing a three-course dinner for your guests.|| A job is a collection of tasks. It manages how computation is performed by its tasks on the compute nodes in a pool (means group of computers)
2. Tasks: Cooking the individual dishes like salad, main course, and dessert. || task represents a unit of computation => task runs one or more programs or scripts on a compute node to perform the work you need done. => Runs on a machine (NODE)
3. Workflow: The recipe book guiding you through the cooking process.
4. node: kitechen accesorries: A node is an Azure virtual machine (VM) or cloud service VM that is dedicated to processing a portion of your application's workload.
5. Pools: Your kitchen appliances, utensils, and helpers that work together to prepare the meal. || A pool is the collection of nodes that your application runs on

## use cases
Azure Batch is a cloud-based job scheduling service provided by Microsoft Azure, designed to run large-scale parallel and high-performance computing (HPC) workloads efficiently. It can be used in various industries to solve compute-intensive tasks, process large datasets, and optimize resource utilization. Here are some real industry use cases of Azure Batch:

1. Scientific Research: In fields like genomics, climate modeling, and drug discovery, researchers deal with large datasets and complex simulations that require significant computational power. Azure Batch can be used to distribute these tasks across multiple nodes and process them in parallel, significantly reducing the time required for analysis and experimentation.

2. Media and Entertainment: Video rendering and special effects rendering for movies, animations, and video games often require intense computation. Azure Batch can be utilized to render frames simultaneously across multiple virtual machines, enabling faster rendering times and efficient resource usage.

3. Financial Services: Financial institutions often need to perform large-scale financial modeling, risk analysis, and simulations. Azure Batch can handle complex calculations for portfolio optimization, Monte Carlo simulations, and other computational finance tasks, improving decision-making and reducing processing time.

4. Manufacturing and Engineering: In industries like automotive, aerospace, and consumer electronics, engineering simulations are essential for product design and testing. Azure Batch can be leveraged to run simulations, finite element analysis (FEA), computational fluid dynamics (CFD), and other engineering simulations at scale, enabling faster iterations and accelerating the product development process.

5. Image and Video Processing: Applications in computer vision, image recognition, and video analysis require significant computational resources to process large datasets. Azure Batch can be used to distribute image processing tasks across multiple nodes, accelerating the processing of images and videos.

6. Bioinformatics: Genomic data analysis involves handling vast amounts of data to identify patterns and potential correlations. Azure Batch can be employed to perform DNA sequencing alignment, variant calling, and other bioinformatics workflows, speeding up research in healthcare and life sciences.

7. Internet of Things (IoT) Analytics: IoT devices generate a massive amount of data that needs to be processed and analyzed in real-time. Azure Batch can be utilized to process and analyze this data efficiently, enabling actionable insights and decision-making in various IoT applications.

8. Deep Learning and Machine Learning: Training large-scale deep learning models requires substantial computational resources. Azure Batch can help distribute the training workload across multiple GPUs and virtual machines, accelerating the training process for complex machine learning models.

9. Weather Forecasting: Meteorological agencies need to run extensive weather simulations to produce accurate forecasts. Azure Batch can be used to parallelize these simulations, improving forecast accuracy and reducing the time it takes to generate predictions.

These are just a few examples of how Azure Batch can be used across different industries to handle large-scale, compute-intensive workloads efficiently. Its ability to scale seamlessly and manage complex computing tasks makes it a valuable tool for a wide range of applications.

These examples illustrate how batch jobs are commonly used across various industries to efficiently process large volumes of data and automate routine tasks.
=======================================================
**SLA** : higher your SLA, the less frequently the service can go down and the quicker the service must recover.
**Problem with HA**
But as you strive for more nines, the cost and complexity grow 
> 99.99% SLA = MAX 5 min total Downtime in a month

achieve four nines (99.99%), you can't rely on manual intervention to recover from failures. The application must be self-diagnosing and self-healing.
=========================================

## ACI: Serverless container
> Azure Container Instances is a solution for any scenario that can operate in isolated containers, without orchestration **(means without K8s)**. Run event-driven applications, quickly deploy from your container development pipelines, and run data processing and build jobs.
- You can't scale it => If you need to run more instances, use our API to automate and create more requests for container group creation to the service.
**use cases**:
1. Web Applications and Microservices: ACI is excellent for hosting web applications and microservices that require isolation and quick scaling. It allows developers to package their applications in containers and deploy them without the need for managing complex container orchestration systems like Kubernetes. ACI can handle sudden spikes in traffic and scale up or down automatically.

2. Backend APIs and Services: Many applications require backend APIs and services to process requests and provide data. ACI can host these backend components in isolated containers, ensuring a clean separation of concerns and making it easier to manage and scale them independently.

3. Batch Processing and Data Jobs: ACI can be used for running data processing tasks, batch jobs, and ETL (Extract, Transform, Load) operations. For instance, you can use ACI to process large amounts of data, run periodic data jobs, or transform data from one format to another.

4. CI/CD Pipelines: ACI can be integrated into continuous integration and continuous deployment (CI/CD) pipelines. Developers can build and test their containers in CI/CD pipelines and then deploy them to ACI without dealing with the complexity of a full container orchestration platform.

5. Dev/Test Environments: ACI can be used for creating temporary development and testing environments. Developers can quickly spin up container instances with the required dependencies and configurations, test their applications, and tear them down once testing is complete, saving costs and resources.

6. Event-Driven Applications: ACI is well-suited for event-driven applications that need to respond to specific events or triggers. For example, processing messages from a message queue, responding to webhooks, or handling file uploads.

7. Machine Learning and AI Inference: ACI can be used to deploy machine learning models and AI inference workloads. Data scientists and AI engineers can package their trained models into containers and deploy them on ACI to make predictions and serve real-time inference requests.

8. IoT (Internet of Things) Applications: ACI can be used to process and analyze data generated by IoT devices. It allows developers to deploy lightweight and scalable container instances to handle data streams from IoT devices efficiently.
   
> running independent and isolated containers is suitable for development, testing, and one-off tasks, while using an orchestrator like Kubernetes is essential for managing complex production environments that require scalability, high availability, service discovery, and orchestration of multiple services. The choice between isolated containers and an orchestrator depends on the specific requirements of the application and the scale of the deployment.

# AKS - managed k8s
When you create an AKS cluster, a control plane is automatically created and configured. This control plane is provided at no cost as a managed Azure resource abstracted from the user. You only pay for and manage the nodes attached to the AKS cluster.
[CORE CONCEPTS = K8S + AKS ](https://learn.microsoft.com/en-us/azure/aks/concepts-clusters-workloads)

# Azure Fucntios
1. When to use??
 https://learn.microsoft.com/en-us/azure/azure-functions/functions-overview?pivots=programming-language-csharp#scenarios
2. Hosting - range from fully serverless, where you only pay for execution time (Consumption plan), to always warm instances kept ready for fastest response times (Premium plan || have excess App Service hosting resources, you can host your functions in an existing App Service plan || Though having dedicated is GOOD
3. **Durable FUnction** == Stateful Functions => https://learn.microsoft.com/en-us/azure/azure-functions/durable/durable-functions-overview?tabs=in-process%2Cv3-model%2Cv1-model&pivots=csharp
4. Comparison Power Automate vs logic apps - https://learn.microsoft.com/en-us/azure/azure-functions/functions-compare-logic-apps-ms-flow-webjobs?toc=%2Fazure%2Fazure-functions%2Fdurable%2Ftoc.json#compare-microsoft-power-automate-and-azure-logic-apps

## Azuer Logic Apps: can create and run automated workflows with little to no code. By using the visual designer
- systems across cloud, on premises, and hybrid environments and provides low-code-no-code tools for you to develop highly scalable integration solutions for your enterprise and business-to-business (B2B) scenarios. LIKE CONNECT TO ON-PREM USING ON-PREM CONNECTOR
Key terms : https://learn.microsoft.com/en-us/azure/logic-apps/logic-apps-overview#key-terms

