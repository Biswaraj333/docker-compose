# Azure Virtual Machine Creation Guide

## Overview
This guide will help you create a Virtual Machine (VM) in Microsoft Azure. It includes all the steps to set up a basic VM, configure networking, and connect to it via remote desktop or SSH.

---

## Prerequisites
- **Azure Subscription**: You need an active Azure account. If you don't have one, you can create a free account [here](https://azure.microsoft.com/en-us/free/).
- **Azure Portal Access**: You need to be able to access the [Azure Portal](https://portal.azure.com/).
- **Basic Knowledge**: Familiarity with virtual machines and networking concepts.

---

## Steps to Create a VM in Azure

### 1. **Log in to the Azure Portal**
   - Open the [Azure Portal](https://portal.azure.com/).
   - Sign in with your Azure account credentials.

### 2. **Navigate to Virtual Machines**
   - In the left-hand menu, click on **"Virtual machines"**.
   - If it's not listed, use the search bar at the top to search for "Virtual Machines".

### 3. **Create a New Virtual Machine**
   - On the Virtual Machines page, click **"Create"** and then select **"Azure virtual machine"**.
   - You will be directed to the "Create a Virtual Machine" wizard.

### 4. **Configure the Basic Settings**
   - **Subscription**: Choose the subscription you want to use.
   - **Resource Group**: Select an existing resource group or create a new one.
   - **VM Name**: Enter a name for your VM (e.g., `MyAzureVM`).
   - **Region**: Choose the Azure region where you want your VM to be located (e.g., `East US`).
   - **Availability Options**: Leave as default unless you need a specific setup.
   - **Image**: Choose the OS you want to install on your VM (e.g., Windows Server, Ubuntu).
   - **Size**: Select the appropriate size based on your workload (e.g., Standard B1s for a small VM).
   - **Authentication Type**: 
     - **Password**: Provide a username and password for the VM.
     - **SSH Public Key** (for Linux VMs): Provide an SSH key.
   - **Public IP**: Choose "Create new" to have a new public IP for remote access.

### 5. **Configure Disks**
   - **OS Disk Type**: Choose the disk type (e.g., SSD, HDD).
   - **Data Disks**: Optionally, you can attach data disks for additional storage if needed.

### 6. **Networking Configuration**
   - **Virtual Network**: Select an existing virtual network or create a new one.
   - **Subnet**: Choose a subnet from the selected virtual network or create a new one.
   - **Network Security Group**: Create a new security group or use an existing one to manage access to your VM.
   - **Public IP**: Ensure that a public IP is assigned if you want to connect to the VM over the internet.

### 7. **Management Options**
   - Configure monitoring options like boot diagnostics, and backup if necessary.
   - Enable **Auto-shutdown** to avoid running the VM unnecessarily.

### 8. **Review + Create**
   - Once all configurations are complete, review the settings.
   - If everything looks good, click **"Create"**.

   Azure will begin provisioning your virtual machine. This might take a few minutes.

### 9. **Access the VM**
   - Once the VM has been created, go to the **Virtual Machines** section in the Azure Portal.
   - Select the VM you just created.
   - To access the VM:
     - **For Windows VMs**: Use **Remote Desktop Protocol (RDP)**.
       - Download the RDP file from the "Connect" tab and use your credentials to log in.
     - **For Linux VMs**: Use **SSH**.
       - Open your terminal and use the command: 
         ```
         ssh username@<your-vm-public-ip>
         ```

---

## Additional Configuration (Optional)

- **Set Up a Static IP**: 
  If you need a fixed IP address for your VM, navigate to the **Public IP Address** section and configure a static IP.

- **Install Software**:
  After accessing your VM, you can install any necessary software, such as a web server, database, or development tools, based on your use case.

- **Scaling**:
  You can change the size of your VM after creation by selecting the "Size" option under the VM's settings.

- **Backup and Restore**:
  Configure backup services in the "Backup" tab to ensure your VM data is regularly backed up.

---

## Conclusion
Congratulations! You have successfully created and configured a Virtual Machine on Azure. From here, you can install applications, configure your environment, and scale as needed.

---

## Troubleshooting
- **RDP/SSH Connection Issues**: Ensure the VM’s firewall rules and network security group (NSG) allow RDP or SSH traffic (port 3389 for RDP, port 22 for SSH).
- **VM Not Starting**: Check the "Boot Diagnostics" and "Logs" to diagnose the issue.

For further assistance, refer to the [Azure documentation](https://docs.microsoft.com/en-us/azure/virtual-machines/).

---
 
