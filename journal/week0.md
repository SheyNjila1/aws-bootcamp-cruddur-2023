# Week 0 — Billing and Architecture

## Cruddlur Logical Diagram
![image](https://user-images.githubusercontent.com/96470430/221334647-0abf3005-4ea2-409b-8d58-b1f6c0a88bc3.png)

### Link: https://lucid.app/lucidchart/2ff09365-398e-4d57-9c66-cf4454e08ca7/edit?viewport_loc=-468%2C-38%2C2972%2C1588%2C0_0&invitationId=inv_01a0bf83-9d31-4940-ac62-3b229938c41f

## Cruddlur Diagram (Outline)
![image](https://user-images.githubusercontent.com/96470430/221334748-a13873b9-5c77-4e0b-93a1-df5f9264595f.png)
### Link: https://lucid.app/lucidchart/6c772b9e-8845-4a2f-a4e9-26bdd1013971/edit?viewport_loc=-482%2C-118%2C2972%2C1588%2C0_0&invitationId=inv_6f562e82-ad1f-4dc1-908f-3f195c01858b

## Jenkins CI/CD Pipeline for Infra provisioning with Terraform
![image](https://user-images.githubusercontent.com/96470430/221335748-514b6d21-4619-471f-b3f1-12ead5c73ae1.png)
### Link: https://lucid.app/lucidchart/6a01cf3c-b638-4130-bfa7-660bee4bf1ed/edit?viewport_loc=-424%2C2268%2C2972%2C1588%2C0_0&invitationId=inv_e276cf5d-0a3c-4d0b-8073-ed81f9f70232

## Jenkins CI/CD Application deployment in a kubernetes cluster
![image](https://user-images.githubusercontent.com/96470430/221336101-39c5b6c6-6e1d-4974-8528-855167c72406.png)
### Link: https://lucid.app/lucidchart/6a01cf3c-b638-4130-bfa7-660bee4bf1ed/edit?viewport_loc=-424%2C2268%2C2972%2C1588%2C0_0&invitationId=inv_e276cf5d-0a3c-4d0b-8073-ed81f9f70232


## Project: Use EventBridge to hookup Health Dashboard to SNS and send notification when there is a service health issue.
### Architectural Diagram
![image](https://user-images.githubusercontent.com/96470430/221334848-6dd7e767-2f9f-43b0-9d42-7f29440716d8.png)

### Link to tutorial: https://docs.aws.amazon.com/health/latest/ug/cloudwatch-events-health.html 
### Steps
#### create an EventBridge rule for AWS Health
#### Open the Amazon EventBridge console at https://console.aws.amazon.com/events/.

#### To change the AWS Region, use the Region selector in the upper-right corner of the page. Choose the Region in which you want to track AWS Health events.

#### In the navigation pane, choose Rules.

#### Choose Create rule.

#### On the Define rule detail page, enter a name and description for your rule.
![1-EventBridge-rule-for-AWS-Healt](https://user-images.githubusercontent.com/96470430/221335239-4963d2ef-3339-4408-8db0-1c9a63502ddc.PNG)

#### Keep the default values for Event bus and Rule type, and then choose Next.

#### On the Build event pattern page, for Event source, choose AWS events and EventBridge partner events.
![2-Build-Event-Pattern](https://user-images.githubusercontent.com/96470430/221335248-6d73b704-9baa-4bff-a1e3-981c3530d1da.PNG)

#### Under Event pattern, for Event source, choose AWS services.

#### Under Event pattern, for AWS service, choose Health.
![3-Creation-Method](https://user-images.githubusercontent.com/96470430/221335274-f3930844-0d74-47c5-8a0f-6ab85f2098bd.PNG)

#### For Event type, choose one of the following options.

#####  Specific Health Abuse Events – Create a rule for AWS Health events that have the word Abuse in the event type name.

#### Specific Health events – Create a rule for events for a specific AWS service, such as Amazon EC2.
![5-ReviewandCreate](https://user-images.githubusercontent.com/96470430/221335287-eeb20013-37fd-4321-8f5a-5d1f67c6484a.PNG)

#### You can choose Any service or Specific service(s). If you chose a specific service, choose one of the following options:

#### Choose Any event type category to create a rule that applies to all event type categories.
![8-HealthDashBoard](https://user-images.githubusercontent.com/96470430/221335289-cb154fa1-588f-4ab5-b6f8-d4bcf35e067a.PNG)

#### Choose Specific event type category(s) and then choose a value from the list, such as issue, accountNotification, or scheduledChange.

![666666-succesfullycreated](https://user-images.githubusercontent.com/96470430/221335292-9c5502d7-cea2-461a-9046-5a061f11b2b8.PNG)

![666666-succesfullycreated](https://user-images.githubusercontent.com/96470430/221335353-3e957264-8fe9-4cc3-9406-1ed1ffa9959b.PNG)

![8-HealthDashBoard](https://user-images.githubusercontent.com/96470430/221335358-9f5ad351-08b1-427c-8442-12f6a047e034.PNG)


# Amazon Elastic Compute Cloud (EC2) is a web service that provides resizable compute capacity in the cloud. EC2 allows users to configure and launch virtual machines, known as instances, in Amazon's data centers.

Here are some of the main technical and service limits of EC2:

##### 1. Instance Limits: Each AWS account has a limit on the number of EC2 instances that can be launched. The instance limits vary by instance type, region, and account type. The limits can be increased by contacting AWS Support.

##### 2. Volume Limits: There are limits on the number and size of Elastic Block Store (EBS) volumes that can be attached to an EC2 instance. The limits depend on the instance type and can also be increased by contacting AWS Support.

##### 3. Network Limits: EC2 instances are limited by the amount of network bandwidth available. The network bandwidth is determined by the instance type and the network performance mode selected. The network limits can impact the performance of applications running on the instance.

##### 4. Availability Zone Limits: Each AWS region is divided into multiple Availability Zones. EC2 instances can be launched in any Availability Zone within a region. However, there are limits on the number of instances that can be launched in each Availability Zone. These limits can impact the availability and scalability of applications running on EC2.

##### 5. Security Limits: AWS imposes limits on the number of security groups and rules that can be associated with an EC2 instance. These limits can impact the security posture of applications running on EC2


# Amazon S3 (Simple Storage Service) is a cloud-based object storage service provided by Amazon Web Services (AWS).  
#### While S3 is a highly flexible and customizable service, it does have some technical and service limits that can impact its technical path for technical flexibility.

### Technical Limits:

##### 1. Object Size: The maximum size of a single object that can be stored in S3 is 5 terabytes. If an object is larger than 5 terabytes, it will need to be split into multiple objects.

##### 2. Bucket Size: The maximum size of an S3 bucket is unlimited. However, AWS recommends keeping the number of objects per bucket below 100,000 for optimal performance. If a bucket exceeds this limit, it can affect performance when listing objects or using lifecycle policies.

##### 3. API Requests: S3 imposes limits on the number of API requests that can be made per second. This limit varies based on the type of request and the region. In general, the limit is around 3,500 requests per second per prefix.

##### 4. Transfer Speed: The maximum transfer speed of S3 varies depending on the size and number of objects being transferred, as well as the location of the source and destination. The transfer speed is also impacted by the network bandwidth and latency.

### Service Limits:

##### 1. Storage Classes: S3 offers different storage classes, including Standard, Infrequent Access, and Glacier. Each storage class has its own set of service limits, such as the minimum storage duration and the minimum size of objects that can be stored.

##### 2. Data Retrieval: S3 imposes limits on the frequency and speed at which data can be retrieved from certain storage classes, such as Glacier. Retrieving data from Glacier may also incur additional costs.

##### 3. Bucket Lifecycle Policies: S3 allows users to define lifecycle policies that automatically transition objects between different storage classes or delete them based on specific criteria. However, S3 limits the number of lifecycle policies that can be created per bucket.

##### 4. Bucket and Object Names: S3 imposes restrictions on the naming of buckets and objects. For example, bucket names must be globally unique, and object keys cannot contain certain characters.

#### Impact on Technical Flexibility:

##### The technical and service limits of S3 can impact its technical flexibility in several ways. For example, if an application requires the storage of large objects, it may need to split them into multiple smaller objects, which can increase complexity and impact performance. Similarly, if an application needs to perform a large number of API requests, it may need to implement rate limiting to avoid exceeding the request limits imposed by S3.

###### To ensure technical flexibility, it is important to design applications that can adapt to the technical and service limits of S3. This can involve designing data structures and transfer mechanisms that are optimized for S3, as well as utilizing S3 features, such as lifecycle policies, to manage the lifecycle of objects. Additionally, applications should be designed to handle errors and exceptions that may occur when working with S3, such as throttling or service interruptions.
