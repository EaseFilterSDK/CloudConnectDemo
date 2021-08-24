# CloudConnect Demo Application
## The challenges to connect the public cloud storage
Enterprises are increasingly adopting cloud storage options because they need more capacity, elastic capacity and a better way to manage storage costs over time. The growing amount of enterprise data is proving too difficult for IT departments to manage using their data center alone. Migrating and managing your data storage in the cloud can offer significant value to the business. A cloud storage migration is when a company moves some or all of its local data into the cloud, usually to run on the cloud-based infrastructure provided by a cloud service provider such as AWS and Azure.The main challenge of the cloud storage migration here is how to carry out your migration with minimal disruption to normal operation, at the lowest cost, and over the shortest period of time. If your data becomes inaccessible to users during a migration, you risk impacting your business operations.The biggest challenge of the cloud storage migration for most small to medium size companies is the application redevelopment to adopt the cloud storage, most companies can't afford the expense. CloudTier Cloud Connect provides a complete solution to transparently connect to Amazon S3 storage and Azure storage. CloudTier uses the cloud storage as second tier, it can automatically to move data between local and the cloud, so your application doesn't need to do any change, it can access the cloud storage just like the local one transparently.

Tiered Storage File System Filter Driver Technology
The Cloud storage tiering was implemented with tiered storage file system filter driver. A file system filter driver intercepts requests targeted at a file system or another file system filter driver. By intercepting the request before it reaches its intended target, the filter driver can extend or replace functionality provided by the original target of the request. File system filtering services are available through the filter manager in Windows. The CloudTier tiered storage filter driver can intercept the file I/O to the local storage and redirect it to the remote cloud storage by implementing the file system filtering functionalities which was provided by the Filter Manager framework.

![loudTier Storage Tiering Architecture](https://www.easefilter.com/images/CloudTiering.png)

# Cloud Archiving Solution for Unstructured Data

Cloud archiving is the process of moving data to secondary storage in the cloud, the potential benefits of cloud archiving include lower costs and easier access, no interruption and change to your existing applications and infrastructure. Automatically archive, manage and secure all your organization’s files to the cloud, transparently access your archived

![loudTier Storage Tiering Solution](https://www.easefilter.com/images/CloudTier.png)

## CloudTier example is a simple C# Windows forms application, to demo how to use the transparent storage tiering SDK. 
The example can generate some stub files. To handle the read request of the stub file, we need to register the callback function for the file system filter driver. When the stub file was accessed, the callback function will be invoked, the callback function will retrieve the data from the remote server and send back to the filter driver.

## How to run the CloudTier demo?

1.	Create the stub files first, go to tools->create stub test files.
	By creating the stub file, you can move out your data to low-cost remote storage, 
        
2.	The test source folder stores the file data to simulate the remote host server. 
	You can store your source file data anywhere, i.e. Amazon s3, Azure storage or your own private cloud storage.

3.	The test stub file folder stores the test stub files.
	The stub file doesn't take the storage space, it only keeps the meta data you created.

4.	After the stub files were created, start the filter service. The stub files can be read as a regular file, when you open the stub file, 
	all data will read from the source file by the demo application.

5.	For demo purpose, the new stub file’s reparse point tag always pointing to the source file, you can change it to your remote sever, or in the cloud.

[Read more about CloudTier SDK example](https://www.easefilter.com/Forums_Files/CloudTier.htm)

