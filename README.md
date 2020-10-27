Azure Demo : Provision VM's in thirteen data centers worldwide in 10 minutes!
=============================================================================

            

**!This script uses the older Azure ASM engine to provision resources. ASM is superseded by Azure Resource Manager (ARM)!**


![Image](https://github.com/azureautomation/azure-demo--provision-vm's-in-thirteen-data-centers-worldwide-in-10-minutes!/raw/master/azuredemo_provisionvmsglobally.gif)


Blog: 
http://www.ruudborst.nl


Presentation: [https://www.youtube.com/watch?v=mRkJmgg9IJ0](https://www.youtube.com/watch?v=mRkJmgg9IJ0)


This script helps you to automatically deploy an Azure VM, Azure Service and related Storage Account in each available Microsoft Azure data center. It also facilitates in the provisioning and management of these VM's through the script advanced functions
 which are made available in the 'Global' scope and thus can be used in the console. This includes the VM and storage account provisioning,remote PowerShell session setup, PowerShell remote command execution, rdp connection and public endpoint functions.
This way it's fairly easy to provision the VM's in every Azure region available, use the resources (network/compute/storage) at that location and execute any remote ps commands to that VM. The 'Execute-RemoteCommand' facilitates in the session setup and
 lets you execute a command against one or more VM's and orders all results accordingly.


All script parameters are optional and will be determined automatically when left blank. In addition to the configurable script parameters, the script's main routine will prompt for the administrator credentials, the Windows image file (deployment)
 and in which region/datacenter the VM's should be deployed. For demo purposes this script requires you to supply all the information instead of supplying the information to the script's parameters. When all information is validated PowerShell's parallel
 workflow execution will be used to deploy the VM's and related storage accounts.


Note: PowerShell workflow in version 3 is limited with a hardcoded maximum of five simultaneous threads, there are some workarounds and solutions (runspaces/jobs) to expand the number of threads but it's wiser to be on the safe side and avoid running
 into any kind of restriction or thread limitation in Azure. 


Important: Please be aware of the Azure VM Core and Cloud Service limit in Azure (default 20), open up a support ticket with Microsoft to raise the limit.    See: http://azure.microsoft.com/en-us/documentation/articles/azure-subscription-service-limits/#subscription-limits

 

        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.
