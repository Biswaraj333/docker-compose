# Azure Virtual Machine Creation Guide
 
## Prerequisites

Before you begin, ensure you have the following:

- **Azure Subscription**: Ensure you have an active Azure subscription (e.g., Microsoft Azure Sponsorship).

- **Access to the Azure Portal**: You must be logged into the [Azure Portal](https://portal.azure.com/).

- **SSH Public Key**: You should have an existing SSH public key stored in Azure (for authentication).
 
---
 
## Steps to Create a Virtual Machine in Azure
 
### 1. **Create the Virtual Machine**

   - **Navigate to the Azure Portal** and log in with your Azure credentials.

   - In the search bar, type and select **"Virtual Machines"**.

   - Click on **"Create"** and then select **"Azure Virtual Machine"**.
 
### 2. **Basic Configuration**

   - **Subscription**: Select **Microsoft Azure Sponsorship**.

   - **Resource Group**: Select or create a new resource group, for example, `RG_AIBOX_DEV`.

   - **Instance Details**:

     - **VM Name**: `demo3-ai` (example)

     - **Region**: Central India

     - **Availability Option**: 

       - Choose **Virtual Machine scale set / Availability Zone / No infra**.

       - **Zone Option**: Select **Self selected** and choose **at least 2 zones**.

     - **Security Type**: Trusted launch VM

     - **Image**: Select **Ubuntu Server 22**

     - **VM Architecture**: x64

     - **Azure Spot Discount**: Skip this option (Not for Production).

     - **Size**: Select **Standard B8as** with **8 CPUs** and **32 GiB RAM** (requires at least 8 vCPUs and 32 GiB of RAM).

   - **Administrator Account**:

     - **Authentication Type**: Select **SSH public key**.

     - **Username**: `qylis` (default).

     - **SSH Public Key Source**: Use an existing key stored in Azure.

     - **Stored Keys**: Select **AIBOX-DATABASE-STORAGE.pem**.

   - **Spot**: Skip this option.
 
   - **Inbound Port Rules**:

     - **Public Inbound Ports**: Select **Allow selected ports**.

     - **Select Inbound Ports**: Choose **HTTP**, **HTTPS**, and **SSH**.
 
### 3. **Disks Configuration**

   - **Encryption at Host**: Set to **False** (change in future as needed).

   - **OS Disk**:

     - **Size**: Default 30 GiB.

     - **Type**: **Premium SSD (locally redundant)**.

     - **Key Management**: Set to **Platform managed key**.
 
### 4. **Networking Configuration**

   - **Network Interface**:

     - **Virtual Network**: Choose to **create new** or **use an existing one** (based on your requirement).

     - **Subnet**: Create or use an existing subnet.

     - **Public IP**: Automatically picked.

     - **Network Security Group (NSG)**: Set to **Basic**.

   - **Public Inbound Ports**: Select the same inbound ports as selected in the Basic Configuration (HTTP, HTTPS, SSH).
 
   - **Load Balancing**: Select **None** (unless needed).
 
### 5. **Management Configuration**

   - The **Management**, **Monitoring**, and **Advanced** options are automatically selected. These can be reviewed and adjusted based on your needs.
 
### 6. **Tags**:

   - Tags are automatically selected, but you can modify or add additional tags as needed.
 
### 7. **Review & Create**

   - **Review**: Go over the configuration details one last time.

   - If everything looks correct, click **Create** to begin provisioning your VM.
 
---
 
## Conclusion

You have successfully configured and created a Virtual Machine in Azure with the specified settings. From here, you can access your VM, install necessary software, and scale the resources as required.
 
---
 
## Troubleshooting

- **RDP/SSH Connection Issues**: Ensure the network security group (NSG) and firewall settings allow RDP or SSH traffic on the correct ports (22 for SSH, 3389 for RDP).

- **VM Not Starting**: If the VM doesn't start or shows an error, check the boot diagnostics and logs in the Azure portal for troubleshooting.
 
For more detailed information, refer to the [Azure Virtual Machines Documentation](https://docs.microsoft.com/en-us/azure/virtual-machines/).

Page not found
 
