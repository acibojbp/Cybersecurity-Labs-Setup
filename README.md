# Getting Started with Cybersecurity Labs

Welcome to the Cybersecurity Labs Setup! As someone deeply passionate about cybersecurity, I've embarked on numerous journeys to set up and configure various operating systems tailored for cybersecurity practices. Through my personal experiences, I've curated this guide to help you navigate the installation process for several key operating systems commonly used in the field.

In this guide, I'll walk you through step-by-step instructions for installing the following operating systems on VirtualBox, just as I did:

- [Choose a Virtualization Platform](#choose-a-virtualization-platform)
- [Windows 10](#install-windows-10-virtual-machine)
- [Windows Server 2022](#install-windows-server-2022-virtual-machine)
- [Kali Linux](#install-kali-linux-virtual-machine)
- [Ubuntu Desktop](#install-ubuntu-linux-virtual-machine)
- [Ubuntu Server](#install-ubuntu-server-virtual-machine)

By following these instructions, you'll be able to create virtual machines tailored to your cybersecurity needs and start experimenting with different tools and techniques within a secure and isolated environment.
## Choose a Virtualization Platform

Select a virtualization platform to set up virtual machines for conducting experiments. VirtualBox is a popular choice due to its free and open-source nature, but there are other options available as well.
#### Other Options:

- VMware Workstation
- Hyper-V
- Parallels Desktop
- QEMU
- Proxmox Virtual Environment

For this task, I've opted for VirtualBox. To begin, we need to have VirtualBox installed. You can download it from [Oracle VM Virtual Box](https://www.virtualbox.org/). 

As of writing, the latest version is 7.0.14. Make sure to select the appropriate platform package for your operating system. In my case, I'm using Windows 11, so I'll be downloading the Windows hosts package. After installing VirtualBox, we can move on to installing the various virtual machines required for upcoming labs.

## Install Windows 10 Virtual Machine

Proceed with installing a virtual machine running Windows 10 for your cybersecurity lab. You can obtain a Windows 10 ISO file from the [official Microsoft website](https://www.microsoft.com/en-us/software-download/windows10) or other trusted sources.

Since I am running a Windows Machine, I cannot download an ISO directly but we can choose **Create Windows 10 installation media**. Once the installation media setup is complete, you'll have the Windows 10 ISO file ready for use.

To install Windows 10 in VirtualBox. 

1. Open VirtualBox and click on "New" to create a new virtual machine.
2. Follow the wizard to set up the virtual machine:
    - Specify a name; for this purpose, we will name it as Windows 10, but you can choose any name depending on your intended use or specific lab.
    - Leave the Folder as default, or you can change it.
    - In the ISO image section, navigate to where the downloaded ISO is saved and select it.
    - Keep the Skip Unattended Installation option unchanged to simplify the installation process.
3. If you choose to have unattended installation, in the next window, setup a username and password as well as hostname and domain name.
	 - Make sure to tick Guest Additions which consists of device drivers and system applications that optimize the guest operating system for better performance and usability.
4. Allocate the desired amount of memory (RAM) and CPU to the virtual machine based on the workload you intend to run on the virtual machine. It is recommended to allocate at least 2 GB of RAM and assigning one or two CPU cores should suffice for basic usage, but adjust as needed for more demanding tasks or multitasking scenarios.
5. Create a virtual hard disk by selecting "Create a virtual hard disk now" and choosing the default options for the disk type and storage allocation.
    - It is recommended to have at least 32 GB, but this depends on what purpose you want this machine for. You can leave it at the default of 50 GB.
6. Finish setting up the virtual machine by completing the setup wizard and clicking "Finish" to finalize the creation of the Windows 10 virtual machine.
7. Once the virtual machine is created, select it from the VirtualBox Manager and click "Start" to launch it.
8. If you didn't select **Skip Unattended Installation**, you can simply wait for the installation to complete. Otherwise, if you did select it, follow the on-screen instructions to install Windows 10 using the ISO file. You will need to partition the virtual hard disk, select the installation location, and configure initial settings such as language and region.
9. Once the installation is complete, the virtual machine will restart.

Congratulations! You have successfully installed a Windows 10 virtual machine in VirtualBox. You can now use this virtual machine for various cybersecurity tasks and experiments within a secure and isolated environment.

### Troubleshooting Resolution Issues:

If you encounter issues with the resolution in your Windows 10 virtual machine, it could be due to a problem with the installation of Guest Additions. This could also occur if you skipped unattended installation, as Guest Additions would need to be installed manually in such cases.

To resolve this:

1. Make sure that Guest Additions are installed in your virtual machine. You can do this by selecting "Devices" from the VirtualBox menu and choosing "Insert Guest Additions CD image". Then, follow the on-screen instructions to install Guest Additions.
2. If you had it ticked during setup and it didn't install correctly, you can manually upgrade Guest Additions by going to the "Devices" menu and selecting "Upgrade Guest Additions".

By ensuring that Guest Additions are correctly installed and upgraded, you should be able to resolve any resolution issues in your Windows 10 virtual machine. This ensures a seamless experience, almost identical to running it natively. Feel free to explore all the new features and enjoy your virtual machine experience!

## Install Windows Server 2022 Virtual Machine

First, download the ISO file from [Windows Server 2022 | Microsoft Evaluation Center](https://www.microsoft.com/en-US/evalcenter/evaluate-windows-server-2022).
This will be pretty much the same as installing a regular Windows machine. Only difference would be here I skip the unattended installation because sometimes it causes errors for me. 

To install Windows Server 2022 in VirtualBox. 

1. Open VirtualBox and click on "New" to create a new virtual machine.
2. Follow the wizard to set up the virtual machine:
    - Specify a name; for this purpose, we will name it as Windows 10, but you can choose any name depending on your intended use or specific lab.
    - Leave the Folder as default, or you can change it.
    - In the ISO image section, navigate to where the downloaded ISO is saved and select it.
    - Tick the Skip Unattended Installation option.
4. Adjust the memory (RAM) and CPU allocation for the virtual machine according to your workload. The minimum requirement for a successful install is 1 processor and 1 GB RAM (2 GB if you opt for Desktop Experience). However, feel free to increase these resources for more demanding tasks or multitasking scenarios.
5. Create a virtual hard disk by selecting "Create a virtual hard disk now" and choosing the default options for the disk type and storage allocation.
    - It is recommended to have at least 32 GB, but this depends on what purpose you want this machine for. You can leave it at the default of 50 GB.
6. Finish setting up the virtual machine by completing the setup wizard and clicking "Finish" to finalize the creation of the Windows 10 virtual machine.
7. Once the virtual machine is created, select it from the VirtualBox Manager and click "Start" to launch it.
8. Follow the on-screen instructions to install Windows 10 using the ISO file. You will need to partition the virtual hard disk, select the installation location, and configure initial settings such as language and region.
9. Once the installation is complete, the virtual machine will restart.

> Note: During the on-screen installation, ensure that you select "Windows Server 2022 Standard Evaluation (Desktop Experience)" as the operating system option. Failure to do so will result in a command-line interface (CLI) only, which can be challenging to navigate, especially for less experienced users.

> Upon booting up, if you're unsure how to press Ctrl + Alt + Del on VirtualBox, simply navigate to the input settings and select "Ctrl + Alt + Del".

Congratulations! You have successfully installed a Windows Server virtual machine in VirtualBox. You can now utilize this virtual machine for a variety of server-related tasks and experiments within a secure and isolated environment.
### Troubleshooting Resolution Issues:

If you encounter issues with the resolution in your Windows 10 virtual machine, it could be due to a problem with the installation of Guest Additions. This could also occur if you skipped unattended installation, as Guest Additions would need to be installed manually in such cases.

To resolve this:

1. Make sure that Guest Additions are installed in your virtual machine. You can do this by selecting "Devices" from the VirtualBox menu and choosing "Insert Guest Additions CD image". Then, follow the on-screen instructions to install Guest Additions.
2. If it didn't install correctly, you can manually upgrade Guest Additions by going to the "Devices" menu and selecting "Upgrade Guest Additions".

By ensuring that Guest Additions are correctly installed and upgraded, you should be able to resolve any resolution issues in your Windows 10 virtual machine. This ensures a seamless experience, almost identical to running it natively. Feel free to explore all the new features and enjoy your virtual machine experience!
## Install Kali Linux Virtual Machine

### Why Choose Kali Linux?

Choosing Kali Linux means accessing a robust set of pre-installed security tools, perfect for penetration testing, digital forensics, and vulnerability assessment. Supported by an active community and regular updates, Kali ensures users stay ahead in cybersecurity. Its customizable nature allows tailoring to specific needs, and ethical guidelines ensure responsible testing practices. 

We will be using Kali for some of the labs where we need to target and attack a specific machine.

To install Kali Linux, follow these steps:

1. **Download Kali Linux**: Visit the [Kali Linux website](https://www.kali.org/get-kali/#kali-platforms) and select the Virtual Machine option. As of writing, the latest version is 2024.1. Choose the 64-bit VirtualBox version. This will download a .7z file.
2. **Extract the Downloaded File**: After downloading, extract the .7z file. You'll find two files inside.
3. **Open the .vbox File**: Double-click the .vbox file. If you don't see the file extension, enable it by going to View -> Show -> File Extensions. This will open VirtualBox, and you'll see Kali Linux listed as installed.
4. **Launch Kali Linux**: Click on Kali Linux in VirtualBox to start it up.
### Post-Installation Setup

After booting up Kali, the first step is to log in using the default credentials (`username:kali`, `password:kali`). Following this, it's crucial to enhance security by changing the default password. You can change the default password by opening a terminal and executing the following command:

```
sudo passwd kali
```

You will be prompted to enter the current password (which is "kali" by default), followed by the new password.
Once the password is changed, prioritize updating Kali Linux by opening a terminal and executing the following command:

```
sudo apt update && sudo apt upgrade -y
```

This ensures that all tools and system packages are up to date, reinforcing the overall security of your Kali virtual machine.

There are a lot more best practices in further securing your Kali virtual machine after completing a fresh installation. It's essential to implement additional security measures, especially considering its intended use for conducting attacks. Researching and applying these best practices is recommended.  
### Install VirtualBox Guest Additions (Optional)

VirtualBox Guest Additions improve the performance and usability of the virtual machine. To install them:

1. In the VirtualBox menu, go to "Devices" > "Insert Guest Additions CD image".
2. Navigate to the mounted CD-ROM directory then right-click and select "Open in Terminal".
3. Run the following command to install the Guest Additions:
```
sudo sh ./VBoxLinuxAdditions.run
```
4. Restart the virtual machine after the installation is complete.

Congratulations! You've installed Kali Linux in VirtualBox. You can now leverage its powerful suite of pre-installed security tools for various cybersecurity tasks and experiments within a secure and isolated environment.

## Install Ubuntu Linux Virtual Machine

Installing Ubuntu on VirtualBox is straightforward and user-friendly, often considered as easy as, if not easier than, installing Windows. You can refer to this guide for more detailed instructions: [How to run an Ubuntu Desktop virtual machine using VirtualBox 7 | Ubuntu](https://ubuntu.com/tutorials/how-to-run-ubuntu-desktop-on-a-virtual-machine-using-virtualbox#1-overview).

### Download Ubuntu ISO:

1. Visit the official Ubuntu website and download the Ubuntu Desktop ISO file from [Download Ubuntu Desktop | Download | Ubuntu](https://ubuntu.com/download/desktop).
2. As of writing the latest version is 23.10, but we'll select Ubuntu 22.04.4 LTS (Long-Term Support) for its stability, long-term support, compatibility with third-party software and hardware, and reduced maintenance needs. Opting for an LTS release ensures a stable platform suitable for various use cases, including production environments and enterprise deployments, with long-term reliability.

To install Ubuntu in VirtualBox, follow these steps:

1. Open VirtualBox and click on "New" to create a new virtual machine.
2. Follow the wizard to set up the virtual machine:
    - Specify a name; for this purpose, we will name it as Ubuntu, but you can choose any name depending on your intended use or specific lab.
    - Leave the Folder as default, or you can change it.
    - In the ISO image section, navigate to where the downloaded Ubuntu ISO is saved and select it.
    - Keep the Skip Unattended Installation option unchanged to simplify the installation process.
3. If you choose to have an unattended installation, in the next window, set up a username and password as well as hostname and domain name.
    - Make sure to tick Guest Additions, which consists of device drivers and system applications that optimize the guest operating system for better performance and usability.
4. Allocate the desired amount of memory (RAM) and CPU to the virtual machine based on the workload you intend to run on the virtual machine. In the website, it is recommended to allocate at least 4 GB of RAM, and assigning two CPU cores, but you can adjust this as needed.
5. Create a virtual hard disk by selecting "Create a virtual hard disk now" and choosing the default options for the disk type and storage allocation.
    - It is recommended to have at least 25 GB, but this depends on what purpose you want this machine for. You can leave it at the default of 50 GB.
6. Finish setting up the virtual machine by completing the setup wizard and clicking "Finish" to finalize the creation of the Ubuntu virtual machine.
7. Once the virtual machine is created, select it from the VirtualBox Manager and click "Start" to launch it.
8. If you didn't select **Skip Unattended Installation**, you can simply wait for the installation to complete. Otherwise, if you did select it, follow the on-screen instructions to install Ubuntu using the ISO file. You will need to partition the virtual hard disk, select the installation location, and configure initial settings such as language and region.
9. Once the installation is complete, the virtual machine will restart.

Congratulations! You have successfully installed an Ubuntu virtual machine in VirtualBox. You can now use this virtual machine for various tasks within a secure and isolated environment.
### Post-Installation Setup

1. Boot up Ubuntu on your virtual machine.
2. When prompted, log in using the credentials (username and password) you specified during the installation process.
3. Once logged in, open a terminal window.
4. Update the system by running the following command:
```
sudo apt update && sudo apt upgrade -y
```
  
This ensures that the Ubuntu system is up-to-date with the latest software packages and security patches, providing improved stability, performance, and protection against vulnerabilities.
### Install VirtualBox Guest Additions (Optional)

VirtualBox Guest Additions improve the performance and usability of the virtual machine. To install them:

1. In the VirtualBox menu, go to "Devices" > "Insert Guest Additions CD image".
2. Navigate to the mounted CD-ROM directory then right-click and select "Open in Terminal".
3. Run the following command to install the Guest Additions:
```
sudo sh ./VBoxLinuxAdditions.run
```
4. Restart the virtual machine after the installation is complete.

## Install Ubuntu Server Virtual Machine

Visit the official Ubuntu website and download the Ubuntu Desktop ISO file from [Get Ubuntu Server | Download | Ubuntu](https://ubuntu.com/download/server)

To install Ubuntu Server in VirtualBox, follow these steps:

1. Open VirtualBox and click on "New" to create a new virtual machine.
2. Follow the wizard to set up the virtual machine:
    - Specify a name; for this purpose, we will name it as Ubuntu, but you can choose any name depending on your intended use or specific lab.
    - Leave the Folder as default, or you can change it.
    - In the ISO image section, navigate to where the downloaded Ubuntu ISO is saved and select it.
    - Keep the Skip Unattended Installation option unchanged to simplify the installation process.
3. If you choose to have an unattended installation, in the next window, set up a username and password as well as hostname and domain name.
    - Make sure to tick Guest Additions, which consists of device drivers and system applications that optimize the guest operating system for better performance and usability.
4. Allocate the desired amount of memory (RAM) and CPU to the virtual machine based on the workload you intend to run on the virtual machine. In the website, it is recommended to allocate at least 4 GB of RAM, and assigning two CPU cores, but you can adjust this as needed.
5. Create a virtual hard disk by selecting "Create a virtual hard disk now" and choosing the default options for the disk type and storage allocation.
    - It is recommended to have at least 25 GB, but this depends on what purpose you want this machine for. You can leave it at the default of 50 GB.
6. Finish setting up the virtual machine by completing the setup wizard and clicking "Finish" to finalize the creation of the Ubuntu virtual machine.
7. Once the virtual machine is created, select it from the VirtualBox Manager and click "Start" to launch it.
8. If you didn't select **Skip Unattended Installation**, you can simply wait for the installation to complete. Otherwise, if you did select it, follow the on-screen instructions to install Ubuntu using the ISO file. You will need to partition the virtual hard disk, select the installation location, and configure initial settings such as language and region.
9. Once the installation is complete, the virtual machine will restart.

> As this is a server installation, it does not include a graphical user interface (GUI). You can follow this comprehensive guide for step-by-step instructions on the on-screen installation process: [Install Ubuntu Server | Ubuntu](https://ubuntu.com/tutorials/install-ubuntu-server#1-overview)
### Post-Installation Setup

1. Boot up Ubuntu on your virtual machine.
2. When prompted, log in using the credentials (username and password) you specified during the installation process.
3. Once logged in, open a terminal window.
4. Update the system by running the following command:
```
sudo apt update && sudo apt upgrade -y
```
  
This ensures that the Ubuntu system is up-to-date with the latest software packages and security patches, providing improved stability, performance, and protection against vulnerabilities.

Congratulations! You have successfully installed an Ubuntu Server virtual machine in VirtualBox. You can now use this virtual machine for various tasks within a secure and isolated environment.
