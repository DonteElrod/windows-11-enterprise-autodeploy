# Enterprise Windows 11 Automated Deployment

## Overview
This repository contains a highly optimized `autounattend.xml` answer file designed for zero-touch deployment of Windows 11 in corporate and professional environments. It automates the OOBE setup while applying security baselines, debloating the OS, and optimizing the system out-of-the-box.

## Key Features
* **Zero-Touch Installation:** Fully bypasses the OOBE setup screens and automates disk partitioning (EFI/Recovery/Windows).
* **Enterprise Security Baseline:** Retains Windows Defender (Endpoint Protection), User Account Control (UAC), and Virtualization-Based Security (VBS). Blocks firmware-injected bloatware (WPBT).
* **Local Account Setup:** Bypasses Microsoft Account (MSA) requirements and automatically provisions a local administrator.
* **Debloat & Privacy:** Removes consumer-grade bloatware (Clipchamp, Bing, Copilot, etc.) and disables unnecessary telemetry/tracking features like Windows Recall.
* **Dynamic Hostnames:** Generates random computer names to prevent network conflicts in Active Directory environments.

## How to Use
1. Format a USB drive and create a bootable Windows 11 installation media (e.g., via Rufus or Windows Media Creation Tool).
2. Download the `autounattend.xml` file from this repository.
3. Place the `autounattend.xml` file strictly into the **root directory** of your bootable USB drive.
4. Boot the target machine from the USB drive. The OS installation, partitioning, and post-install configuration will proceed completely unattended.

## Skills Demonstrated
* OS Deployment & Provisioning
* XML Configuration & Automation
* PowerShell Scripting
* Windows Security & Administration

## Test Environment
This deployment script has been thoroughly tested in the following environments:
* **Hypervisor:** Microsoft Hyper-V / VMware Workstation (Generation 2 VMs)
* **Security:** UEFI Secure Boot & TPM 2.0 Enabled
* **Network:** Both connected and isolated (air-gapped) networks
