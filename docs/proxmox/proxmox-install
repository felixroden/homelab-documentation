# Proxmox Installation Guide

Proxmox Virtual Environment (Proxmox VE) is an open-source server virtualization environment that allows you to manage virtual machines, containers, and storage with a user-friendly web-based interface. This guide will walk you through the process of installing Proxmox VE.

## Prerequisites

Before starting the installation, ensure you have the following:

- A compatible 64-bit processor with Intel VT/AMD-V support.
- A minimum of 2 GB RAM (4 GB or more recommended).
- A hard disk with at least 20 GB of available space.
- A bootable USB drive or CD/DVD with the Proxmox VE ISO.
- A reliable internet connection for updates and package installations.

## Step-by-Step Installation

### Step 1: Download Proxmox VE ISO

1. Visit the Proxmox Download page and download the latest Proxmox VE ISO image.

### Step 2: Create a Bootable USB Drive

1. Use a tool like Rufus (Windows) or Etcher (Linux/Mac) to create a bootable USB drive with the downloaded Proxmox VE ISO.
    - **Rufus**: [Download Rufus](https://rufus.ie/)
    - **Etcher**: Download Etcher

### Step 3: Boot from the USB Drive

1. Insert the bootable USB drive into your server.
2. Restart the server and enter the BIOS/UEFI setup (usually by pressing a key like F2, F10, F12, ESC, or DEL during startup).
3. Set the USB drive as the primary boot device.
4. Save the changes and exit the BIOS/UEFI setup.

### Step 4: Install Proxmox VE

1. The server will boot from the USB drive and display the Proxmox VE installation menu.
2. Select "Install Proxmox VE" and press Enter.
3. Read and accept the End User License Agreement (EULA).
4. Select the target hard disk where you want to install Proxmox VE and click "Next".
5. Configure your country, time zone, and keyboard layout, then click "Next".
6. Set a strong root password and enter your email address for administrative notifications, then click "Next".
7. Configure the network settings for your Proxmox VE server:
    - Enter the hostname (e.g., `proxmox.local`).
    - Configure the IP address, netmask, gateway, and DNS server.
8. Review the installation summary and click "Install" to begin the installation process.
9. Wait for the installation to complete. This may take several minutes.
10. Once the installation is complete, remove the USB drive and reboot the server.

### Step 5: Access the Proxmox Web Interface

1. After rebooting, the Proxmox VE server will display the IP address to access the web interface.
2. Open a web browser on a computer connected to the same network and enter the URL:
    
``` bash
    https://<Proxmox_IP_Address>:8006
```
    
3. You will see a security warning about the self-signed SSL certificate. Proceed to the web interface by clicking "Advanced" and then "Proceed to <Proxmox_IP_Address> (unsafe)".

### Step 6: Log In to Proxmox VE

1. Log in using the username `root` and the password you set during installation.
2. Upon successful login, you will be greeted by the Proxmox VE dashboard.

## Post-Installation Configuration

After installation, it is recommended to perform some post-installation configurations:

### Update Proxmox VE

1. Open a terminal or SSH into your Proxmox VE server.
2. Update the package list and upgrade the installed packages:
    
``` bash
    apt update && apt full-upgrade
```
    
3. Reboot the server if necessary:

    
``` bash
    reboot
```
    

### Add Subscription Key (Optional)

If you have purchased a Proxmox VE subscription, add your subscription key:

1. Log in to the Proxmox web interface.
2. Go to `Datacenter` > `Subscription`.
3. Enter your subscription key and click "Activate".

### Add No-Subscription Repository (Optional)

If you do not have a subscription, you can enable the no-subscription repository to receive updates:

1. Edit the repository configuration file:
    
``` bash
    nano /etc/apt/sources.list
```
    
2. Add the following line:
    
``` bash
    deb http://download.proxmox.com/debian/pve bullseye pve-no-subscription
```
    
3. Save the file and exit the editor.
4. Update the package list:
    
``` bash
    apt update
```
    

### Configure Storage

1. In the Proxmox web interface, go to `Datacenter` > `Storage`.
2. Add and configure storage options such as local directories, NFS, iSCSI, or Ceph.

### Create Virtual Machines or Containers

1. Use the Proxmox web interface to create and manage virtual machines or containers.
2. Refer to the Proxmox VE Documentation for detailed instructions and advanced configurations.