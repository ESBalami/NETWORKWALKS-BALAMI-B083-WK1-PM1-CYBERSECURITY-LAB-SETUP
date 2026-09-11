# Cybersecurity Lab Setup Using VirtualBox and Kali Linux

## Overview

This repository documents the setup and configuration of a cybersecurity laboratory environment using Oracle VirtualBox and Kali Linux as part of the NetworkWalks Internship Programme.

The objective was to create a secure, isolated, and reusable environment for cybersecurity training, penetration testing, vulnerability assessment, and network security exercises.

---

## Objectives

The objectives of this project were:

* Install and configure Oracle VirtualBox.
* Import and configure Kali Linux.
* Create a NAT Network using the 10.0.0.0/24 subnet.
* Configure a static IP address for Kali Linux.
* Enable internet connectivity.
* Configure shared folder functionality.
* Enable host-to-guest communication features.
* Create a secure environment for future cybersecurity exercises.

---

## Laboratory Architecture

The laboratory was configured using a NAT Network to provide internet access while maintaining isolation from the host network.

Host Machine
      |
      |
NAT Network (10.0.0.0/24)
      |
      |
Kali Linux VM
IP Address: 10.0.0.2
Gateway: 10.0.0.1

This architecture allows the virtual machine to access external resources while reducing the risk of affecting the host environment.

---

## Environment Configuration

### Host Environment

| Component               | Configuration     |
| ----------------------- | ----------------- |
| Operating System        | Windows           |
| Virtualisation Platform | Oracle VirtualBox |

### Guest Environment

| Component        | Configuration |
| ---------------- | ------------- |
| Operating System | Kali Linux    |
| Network Type     | NAT Network   |
| IP Address       | 10.0.0.2      |
| Gateway          | 10.0.0.1      |
| DNS Server       | 8.8.8.8       |

---

## Tools Used

* Oracle VirtualBox
* Kali Linux
* 7zip
* Terminal
* NAT Network
* Shared Folder Configuration
* DNS Services

---

## Implementation Process

### Step 1: Downloading and Installing VirtualBox

The first stage of the project involved downloading and installing Oracle VirtualBox on the host machine. VirtualBox was selected because it is a widely used virtualisation platform that enables multiple operating systems to run securely within isolated virtual environments.

The installation process involved:

1. Downloading the latest version of Oracle VirtualBox from the official website.
2. Running the installation package on the host operating system.
3. Accepting the default installation settings and required network components.
4. Completing the installation and verifying that VirtualBox launched successfully.

Once installed, VirtualBox provided the foundation for creating and managing the Kali Linux virtual machine used throughout the laboratory setup.


### Step 2: Creating the NAT Network

A NAT Network was created using the 10.0.0.0/24 subnet to provide internet connectivity while maintaining network isolation.

### Step 3: Downloading and Importing Kali Linux

The next stage involved obtaining and deploying Kali Linux as the guest operating system within the VirtualBox environment. Kali Linux was selected because it is a specialised Linux distribution widely used for cybersecurity training, penetration testing, digital forensics, and security research.

The implementation process involved:

1. Downloading the official Kali Linux VirtualBox image from the Kali Linux website.
2. Extracting the downloaded archive using 7-Zip.
3. Opening Oracle VirtualBox and selecting the option to add an existing virtual machine.
4. Importing the extracted Kali Linux virtual machine files into VirtualBox.
5. Reviewing and adjusting the virtual machine settings, including memory allocation, processor configuration, and network settings.
6. Starting the virtual machine and verifying that Kali Linux booted successfully.

Using the pre-configured VirtualBox image significantly reduced deployment time and ensured compatibility with the VirtualBox environment.

**Outcome**

Kali Linux was successfully imported into VirtualBox and prepared for further network and security configuration tasks.


### Step 4: Network Configuration

The network adapter was configured to use the NAT Network.

A static IP address was assigned:

```
IP Address: 10.0.0.2
Gateway   : 10.0.0.1
DNS Server: 8.8.8.8
```

### Step 5: Connectivity Testing

Connectivity was verified through:

* Gateway testing
* Internet connectivity testing
* DNS resolution testing

Example commands:

```bash
ping 8.8.8.8
ping google.com
```

Successful responses confirmed that the network configuration was functioning correctly.

### Step 6: Shared Folder Configuration

A shared folder was configured between the host operating system and Kali Linux to facilitate file transfer between environments.

This provided a reliable method for sharing:

* Project files
* Scripts
* Screenshots
* Tools
* Documentation

---

## Challenges Encountered

### Challenge 1: Kali Linux Deployment

During the initial setup process, importing and configuring Kali Linux required verification of the virtual machine settings to ensure compatibility with VirtualBox.

### Resolution

The official Kali Linux VirtualBox image was used and configured according to the recommended settings.

---

### Challenge 2: Internet Connectivity Validation

After assigning a static IP address, network connectivity required validation to ensure proper communication with the gateway and external networks.

### Resolution

The gateway, DNS configuration, and NAT Network settings were verified using connectivity tests.

---

### Challenge 3: Drag-and-Drop Functionality

The drag-and-drop feature between the host operating system and Kali Linux did not function correctly despite enabling bidirectional drag-and-drop within VirtualBox.

### Investigation

Several troubleshooting steps were performed, including reviewing VirtualBox integration settings and verifying guest configuration.

### Resolution

Instead of relying on drag-and-drop functionality, a shared folder was configured between the host and guest operating systems.

### Outcome

The shared folder provided a reliable and efficient method for transferring files between environments and allowed the laboratory setup to be completed successfully.

---

## Security Benefits

The completed laboratory environment provides:

* A safe penetration testing environment.
* Isolation from the host operating system.
* Controlled experimentation with cybersecurity tools.
* A platform for malware analysis and vulnerability assessment.
* Reduced risk when conducting security exercises.

---

## Results

The laboratory was successfully configured and validated.

Key achievements include:

* Successful deployment of Kali Linux.
* Functional NAT Network configuration.
* Static IP address assignment.
* Internet connectivity.
* DNS resolution.
* Shared folder integration.
* Secure isolation from the host environment.

The environment is now suitable for cybersecurity learning and practical security testing activities.

---

## Lessons Learned

This project provided practical experience in:

* Virtual machine deployment.
* VirtualBox administration.
* NAT Network configuration.
* Linux networking fundamentals.
* Static IP configuration.
* DNS troubleshooting.
* Shared folder configuration.
* Troubleshooting VirtualBox integration features.
* Host-to-guest communication methods.
* Cybersecurity laboratory design.

---

## Future Applications

This laboratory environment will be used throughout the NetworkWalks Programme for:

* Network scanning using Nmap.
* Vulnerability assessments.
* Web application security testing.
* Linux administration exercises.
* Capture-the-Flag (CTF) activities.
* Penetration testing laboratories.
* Cybersecurity research and experimentation.

---

## Conclusion

This project successfully established a secure cybersecurity laboratory using Oracle VirtualBox and Kali Linux. Despite challenges encountered during setup, practical solutions were implemented to ensure a fully functional environment. The completed laboratory provides a reliable platform for developing cybersecurity skills and conducting future security-focused activities.
