# [CloudConnect SDK](https://www.easefilter.com/Forums_Files/CloudStorageConnect.htm)
## The challenges to connect the public cloud storage
Enterprises are increasingly adopting cloud storage options because they need more capacity, elastic capacity and a better way to manage storage costs over time. The growing amount of enterprise data is proving too difficult for IT departments to manage using their data center alone. Migrating and managing your data storage in the cloud can offer significant value to the business. A cloud storage migration is when a company moves some or all of its local data into the cloud, usually to run on the cloud-based infrastructure provided by a cloud service provider such as AWS and Azure.The main challenge of the cloud storage migration here is how to carry out your migration with minimal disruption to normal operation, at the lowest cost, and over the shortest period of time. If your data becomes inaccessible to users during a migration, you risk impacting your business operations.The biggest challenge of the cloud storage migration for most small to medium size companies is the application redevelopment to adopt the cloud storage, most companies can't afford the expense. CloudTier Cloud Connect provides a complete solution to transparently connect to Amazon S3 storage and Azure storage. CloudTier uses the cloud storage as second tier, it can automatically to move data between local and the cloud, so your application doesn't need to do any change, it can access the cloud storage just like the local one transparently.

## Cloud storage tiering technology
The Cloud storage tiering was implemented with tiered storage file system filter driver. A file system filter driver intercepts requests targeted at a file system or another file system filter driver. By intercepting the request before it reaches its intended target, the filter driver can extend or replace functionality provided by the original target of the request. File system filtering services are available through the filter manager in Windows. The CloudTier tiered storage filter driver can intercept the file I/O to the local storage and redirect it to the remote cloud storage by implementing the file system filtering functionalities which was provided by the Filter Manager framework.

![loudTier Storage Tiering Architecture](https://www.easefilter.com/images/CloudTiering.png)

## Hierarchical storage management
CloudTier Cloud Storage Connect is a data storage technique which automatically moves data between high-cost local disk and low-cost remote cloud storage. CloudTier Cloud Storage Connect can help simplify the migration process by providing the transparent file access from the remote storage. Using the cloud as a storage tier, data can first be moved to a ‘warm’ archive tier of higher-performance disk, where it can still be accessed quickly to meet RPO and RTO SLA’s. As you retain archives for longer, older data can then be moved to a ‘cold’ archive tier with better economics. (This is similar to the tiered storage cost/performance model offered by Amazon S3 with its “warm” Standard tier, “cold” Infrequent Access tier and “frozen” Glacier tier.)

## Integrate your exiting on-premises applications with remote cloud storage transparently                     
Our CloudTier Cloud Storage Connect service can connect an on-premise software appliance with cloud-based storage to integrate your existing on-premises applications with the remote cloud storage infrastructure in a seamless, secure, and transparent fashion.There are no interruption to migrate your on-premise files to the remote cloud storage, don't need to change your existing applications and infrastructure.

1.	Set up file cloud migration policies based on the file type, file size, file attributes.
2.	Create stub file based on the policies after the file was migrated to the cloud storage, it can free up the space from on-premise storage.
3.	Transparent the cloud storage access by reading the stub file for your local application.
4.	Transparent moving data back from remote cloud storage to the local, re-hydrate the stub file for the recent access file based on the policies.

## Cloud archiving solution for unstructured data

Cloud archiving is the process of moving data to secondary storage in the cloud, the potential benefits of cloud archiving include lower costs and easier access, no interruption and change to your existing applications and infrastructure. Automatically archive, manage and secure all your organization’s files to the cloud, transparently access your archived

![loudTier Storage Tiering Solution](https://www.easefilter.com/images/CloudTier.png)

## CloudConnect example is a simple C# Windows forms application, to demo how to connect the cloud storage as the second tier. 
The example can generate some stub files. To handle the read request of the stub file, we need to register the callback function for the file system filter driver. When the stub file was accessed, the callback function will be invoked, the callback function will retrieve the data from the remote server and send back to the filter driver.

## How to run the CloudConnect demo?

1.	Create the stub files first, go to tools->create stub test files.
	By creating the stub file, you can move out your data to low-cost remote storage, 
        
2.	The test source folder stores the file data to simulate the remote host server. 
	You can store your source file data anywhere, i.e. Amazon s3, Azure storage or your own private cloud storage.

3.	The test stub file folder stores the test stub files.
	The stub file doesn't take the storage space, it only keeps the meta data you created.

4.	After the stub files were created, start the filter service. The stub files can be read as a regular file, when you open the stub file, 
	all data will read from the source file by the demo application.

5.	For demo purpose, the new stub file’s reparse point tag always pointing to the source file, you can change it to your remote sever, or in the cloud.

## Connect Amazon S3 storage as second tier storage

1.	Make sure you have a S3 key pair. You will need both the access key ID and the secret access key in order to continue. You can get them from the S3 console website.
2.	Select Amazon_S3 cloud provider name. Click "Add Site" button to create a new site for the amazon s3 connection.
3.	Put your site name and then enter your access key id and secret access key in the text boxes, choose the region in your setting.
4.	Check the enable upload multiple parts box if you want to use parallel upload tasks for a file.
5.	Check the enable parallel download box if you want to use parallel download tasks for a file.
6.	Set the number of the parallel tasks for upload or download.
7.	After filled in all the data, click apply to save the settings.
8.	Click test connection to check if your setting is correct.

![Amazon S3 settings](https://www.easefilter.com/images/AmazonS3Settings.PNG)

## Connect Microsoft Azure storage as second tier storage

1.	Get your connection string  from the Microsoft Azure Dashboard Portal site, by clicking on the link to the Dashboard website.
2.	Select AzureStorage cloud provider name. Click "Add Site" button to create a new site for the Azure storage connection.
3.	Put your site name and then enter your connection string in the text box.
4.	Check the enable upload multiple blobs box if you want to use parallel upload tasks for a file.
5.	Check the enable parallel download box if you want to use parallel download tasks for a file.
6.	Set the number of the parallel tasks for upload or download.
7.	After filled in all the data, click apply to save the settings.
8.	Click test connection to check if your setting is correct.

![Azure settings](https://www.easefilter.com/images/AzureSettings.PNG)

## EaseFilter File System Filter Driver SDK Reference
| Product Name | Description |
| --- | --- |
| [Cloud File System SDK](https://www.easefilter.com/cloud/cloud-file-system-sdk.htm) | EaseFilter Cloud File System SDK Introduction. |
| [CloudTier Storage Tiering SDK](https://www.easefilter.com/cloud/storage-tiering-sdk.htm) | EaseFilter Storage Tiering Filter Driver SDK Introduction. |
| [File Monitor SDK](https://www.easefilter.com/kb/file-monitor-filter-driver-sdk.htm) | EaseFilter File Monitor Filter Driver SDK Introduction. |
| [File Control SDK](https://www.easefilter.com/kb/file-control-file-security-sdk.htm) | EaseFilter File Control Filter Driver SDK Introduction. |
| [File Encryption SDK](https://www.easefilter.com/kb/transparent-file-encryption-filter-driver-sdk.htm) | EaseFilter Transparent File Encryption Filter Driver SDK Introduction. |
| [Registry Filter SDK](https://www.easefilter.com/kb/registry-filter-drive-sdk.htm) | EaseFilter Registry Filter Driver SDK Introduction. |
| [Process Filter SDK](https://www.easefilter.com/kb/process-filter-driver-sdk.htm) | EaseFilter Process Filter Driver SDK Introduction. |
| [EaseFilter SDK Programming](https://www.easefilter.com/kb/programming.htm) | EaseFilter Filter Driver SDK Programming. |

## EaseFilter SDK Sample Projects
| Sample Project | Description |
| --- | --- |
| [CloudTier Storage Tiering Demo](https://www.easefilter.com/cloud/cloudtier-storage-tiering-demo.htm) | A HSM File System Filter Driver Demo. |
| [CloudTier S3 Tiering Demo](https://www.easefilter.com/cloud/cloudtier-s3-intelligent-tiering-demo.htm) | CloudTier S3 Intelligent Tiering Demo. |
| [Cloud File DR S3 Demo](https://www.easefilter.com/cloud/cloud-file-dr-demo.htm) | Cloud File DR S3 Demo. |
| [Amazon S3 File Explorer Demo](https://www.easefilter.com/cloud/s3-browser-demo.htm) | Amazon S3 File Explorer Demo. |
| [Auto File DRM Encryption](https://www.easefilter.com/kb/auto-file-drm-encryption-tool.htm) | Auto file encryption with DRM data embedded. |
| [Transparent File Encrypt](https://www.easefilter.com/kb/AutoFileEncryption.htm) | Transparent on access file encryption. |
| [Secure File Sharing with DRM](https://www.easefilter.com/kb/DRM_Secure_File_Sharing.htm) | Secure encrypted file sharing with digital rights management. |
| [File Monitor Example](https://www.easefilter.com/kb/file-monitor-demo.htm) | Monitor file system I/O in real time, tracking file changes. |
| [File Protector Example](https://www.easefilter.com/kb/file-protector-demo.htm) | Prevent sensitive files from being accessed by unauthorized users or processes. |
| [FolderLocker Example](https://www.easefilter.com/kb/FolderLocker.htm) | Lock file automatically in a FolderLocker. |
| [Process Monitor](https://www.easefilter.com/kb/Process-Monitor.htm) | Monitor the process creation and termination, block unauthorized process running. |
| [Registry Monitor](https://www.easefilter.com/kb/RegMon.htm) | Monitor the Registry activities, block the modification of the Registry keys. |
| [Secure Sandbox Example](https://www.easefilter.com/kb/Secure-Sandbox.htm) |A secure sandbox example, block the processes accessing the files out of the box. |
| [FileSystemWatcher Example](https://www.easefilter.com/kb/FileSystemWatcher.htm) | File system watcher, logging the file I/O events. |
| [ZeroTrust Example](https://www.easefilter.com/kb/zero-trust-file-access-control-demo.htm) | Zero trust file access control with encryption feature. |

## Filter Driver Reference

* [Understand MiniFilter Driver](https://www.easefilter.com/kb/understand-minifilter.htm)
* [Understand File I/O](https://www.easefilter.com/kb/File_IO.htm)
* [Understand I/O Request Packets(IRPs)](https://www.easefilter.com/kb/understand-irps.htm)
* [Filter Driver Developer Guide](https://www.easefilter.com/kb/DeveloperGuide.htm)
* [MiniFilter Filter Driver Framework](https://www.easefilter.com/kb/minifilter-framework.htm)
* [Isolation Filter Driver](https://www.easefilter.com/kb/Isolation_Filter_Driver.htm)

## Support
If you have questions or need help, please contact support@easefilter.com 

[Home](https://www.easefilter.com/) | [Solution](https://www.easefilter.com/solutions.htm) | [Download](https://www.easefilter.com/download.htm) | [Demos](https://www.easefilter.com/online-fileio-test.aspx) | [Blog](https://blog.easefilter.com/) | [Programming](https://www.easefilter.com/kb/programming.htm)


