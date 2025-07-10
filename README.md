# Lab 1: Create a Virtual Machine in Azure from Azure Portal.

In this lab, we will create a Windows Virtual Machine in Azure via Azure portal. Later, we will create the same Virtual Machine using Terraform.

Step 1: In Azure portal, search for Virtual Machines and click on create Virtual Machine.

Step 2: Add the details to create Virtual Machine including:

          Resource Group
          VM Name
          Region
          Image
          Credentials and other details
 
Step 3: Enable RDP under "inbound port rules" to enable RDP access to VM. By default, it allows RDP from all IP addresses. This is not secure. Once VM is created, secure NSG rule to use only “my IP address” to allow RDP from your public IP address only.

Step 4: Go to disks tab and use standard SSD for testing purposes. For Production, it is recommended to use Premium SSD for best performance.
 
On Azure portal, it shows an estimated monthly cost to run this VM, which is very handy.
 
Step 5: It will take couple of minutes to create the virtual machine. Once VM is created, go to network settings to secure Network Security Group for RDP.
Change source to "My IP Address" so it will only allow the public IP address of our local machine to RDP on Azure VM. Note that the warning sign next to RDP rule will also disappear.
 
Step 6: Connect via RDP. Click on Connect to connect to VM via RDP. Download RDP File. RDP to VM and connect using the credentials created when commissioning VM. 
We are logged in to Azure VM. Along with VM, it create other resources including OS disks, public IP address and other resources.
 
Step 7: Configure Auto Shutdown. Under operations in the navigation bar of VM, we can configure auto shutdown on Dev/Test VMs to save costs. Add an email address to receive automated emails.
Make sure to delete all resources so you don’t get charged.

Step 8: Once the testing is completed, select all resources and click on delete so you are not being charged for the resources.
