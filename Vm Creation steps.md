# Steps to Create a Virtual Machine in Azure

Creating a Virtual Machine (VM) in Azure involves a few essential steps that can be performed through the **Azure Portal** or via the **Azure CLI**. This guide will walk you through the process using the **Azure Portal**.

## Step 1: Sign In to Azure Portal
- **Explanation**: To get started, you must sign in to the Azure Portal with your Microsoft or organizational account.
  - **Action**: Go to [Azure Portal](https://portal.azure.com) and enter your login credentials.

## Step 2: Navigate to "Create a Resource"
- **Explanation**: The Azure Portal has a wide range of services, and you need to create a new resource, specifically a Virtual Machine.
  - **Action**: In the left-hand menu of the Azure Portal, click on **"Create a resource"**. This will open the "Create a new resource" page.

## Step 3: Search for "Virtual Machine"
- **Explanation**: Azure provides numerous resource types. To find the Virtual Machine option, you need to search for it in the marketplace.
  - **Action**: In the **"Search the Marketplace"** box, type "Virtual Machine" and select the **"Virtual Machine"** option from the list.

## Step 4: Click "Create"
- **Explanation**: After selecting the Virtual Machine option, you can start the creation process by clicking the **"Create"** button.
  - **Action**: Click the **"Create"** button on the Virtual Machine overview page to begin configuring your new VM.

## Step 5: Configure Basic Settings
- **Explanation**: This section allows you to define the primary attributes of your VM, such as the subscription, resource group, region, and name.
  - **Action**:
    - **Subscription**: Choose the Azure subscription you want to use for the VM.
    - **Resource Group**: Select an existing resource group or create a new one to organize your VM and other resources.
    - **VM Name**: Provide a unique name for your virtual machine.
    - **Region**: Select the Azure region where you want to deploy your VM. Choose a region that is closest to your users or data.
    - **Availability Options**: Choose availability sets or zones for high availability if required.
    - **Image**: Choose the operating system image for your VM, such as **Windows Server** or **Ubuntu**.
    - **Size**: Select the VM size based on your workload requirements (e.g., CPU, memory, and disk resources). You can view different VM sizes under the "Select size" option.

## Step 6: Configure Administrator Account
- **Explanation**: Set up the admin credentials to access your VM.
  - **Action**: 
    - **Username**: Set a username for the VM's administrator account.
    - **Password**: Choose a strong password for the administrator account. Alternatively, you can set up SSH public key authentication for Linux VMs.

## Step 7: Configure Inbound Port Rules (Optional)
- **Explanation**: This section allows you to configure inbound port rules to enable remote access to your VM.
  - **Action**:
    - If you want to connect via **SSH** (Linux VMs), select **SSH** (port 22).
    - If you want to connect via **RDP** (Windows VMs), select **RDP** (port 3389).
    - You can also disable public inbound ports if you plan to connect through a VPN or private connection.

## Step 8: Configure Disks
- **Explanation**: This section lets you configure the VM’s disks, including the OS disk and any additional data disks.
  - **Action**:
    - **OS Disk**: Choose the type of disk for your operating system (Standard HDD, Standard SSD, or Premium SSD).
    - **Data Disks**: You can also add additional data disks if needed for extra storage.
    - **Encryption**: You can enable encryption for the disks to enhance security.

## Step 9: Configure Networking
- **Explanation**: Networking settings are essential to allow communication to and from your VM.
  - **Action**:
    - **Virtual Network (VNet)**: Select an existing VNet or create a new one. The VNet defines the network environment for your VM.
    - **Subnet**: Select an existing subnet or create a new one within the chosen VNet.
    - **Public IP**: Choose whether you want your VM to have a public IP address for external access. You can select **None** if you want it to be private.
    - **Network Security Group (NSG)**: The NSG defines the firewall rules for your VM. You can either use an existing NSG or create a new one.
    - **Load Balancer**: Optionally, you can associate the VM with a load balancer for distributing traffic across multiple VMs.

## Step 10: Configure Management (Optional)
- **Explanation**: Azure offers several management features that you can enable, such as monitoring, backup, and auto-shutdown.
  - **Action**:
    - **Boot Diagnostics**: Enable boot diagnostics to capture screenshots of the VM’s console during boot-up, useful for troubleshooting.
    - **OS Monitoring**: Optionally enable monitoring for metrics like CPU, memory usage, and disk I/O.
    - **Auto-shutdown**: You can set an automatic shutdown time to save costs.

## Step 11: Configure Advanced Settings (Optional)
- **Explanation**: This section allows you to fine-tune additional configurations, such as custom scripts, extensions, or custom images.
  - **Action**:
    - You can leave the advanced settings as default unless you have specific requirements for your VM.

## Step 12: Review + Create
- **Explanation**: Before deploying the VM, you should review all the settings to ensure everything is correct.
  - **Action**: Once you've reviewed your settings, click **"Create"**. Azure will validate your configuration, and once validation is successful, it will start provisioning your VM.

## Step 13: Wait for Deployment to Complete
- **Explanation**: The deployment of your VM will take a few minutes, depending on the size and configuration of the virtual machine.
  - **Action**: You can monitor the progress of the deployment in the Azure Portal. Once completed, you'll see a notification that your VM is successfully created.

## Step 14: Connect to Your VM
- **Explanation**: Once your VM is up and running, you can connect to it either via **RDP** (for Windows VMs) or **SSH** (for Linux VMs).
  - **Action**:
    - For **Windows VMs**: Click on the VM in the Azure Portal, then click **Connect** and select **RDP**. Enter the required credentials and download the RDP file to connect.
    - For **Linux VMs**: Use an SSH client like **PuTTY** or your terminal to connect using the public IP and SSH key or password you set earlier.

---

With these steps, you've successfully created and connected to a virtual machine in Azure!
