---
# required metadata
title: Manage firmware settings for Windows 365 Link devices.
titleSuffix:
description: Learn about managing firmware settings for Windows 365 Link devices.
keywords:
author: ErikjeMS  
ms.author: erikje
manager: dougeby
ms.date: 04/10/2025
ms.topic: how-to
ms.service: windows-365-link
ms.subservice:
ms.localizationpriority: high
ms.assetid: 

# optional metadata

#ROBOTS:
#audience:

ms.reviewer: sajelaci
ms.suite: ems
search.appverid: MET150
#ms.tgt_pltfrm:
ms.custom: intune-azure; get-started; intro-hub-or-landing
ms.collection:
- M365-identity-device-management
- tier2
---

# Manage firmware settings for Windows 365 Link devices

You can use the [Surface Enterprise Management Mode (SEMM)](/surface/surface-enterprise-management-mode#surface-uefi-configurator) feature with Windows 365 Link to enroll, manage, and remove Unified Extensible Firmware Interface (UEFI) settings. You can access SEMM by using the UEFI Configurator in the [Surface IT Toolkit](/surface/surface-it-toolkit). You can use the configurator to enable or disable hardware components at the firmware level and enroll a Windows 365 LINK device in SEMM.

For full information about SEMM and instructions on how to use it, see [Get started with SEMM](/surface/surface-enterprise-management-mode#surface-uefi-configurator).

The rest of this article explains the differences and caveats for using SEMM to manage Windows 365 Link UEFI settings.

## Available configuration settings

The following UEFI components and settings can be configured on Windows 365 Link devices:

- Accessories
  - On-board Audio
  - On-board Microphone
  - Wired LAN
- Radio
  - Bluetooth
  - Wi-Fi
  - Wi-Fi & Bluetooth
- Advanced settings
  - Wake-on-power
  - Alternate boot
  - Network stack
- UEFI password (optoinal)
  - No change
  - Set or modify password
  - Clear password

## Create a UEFI configuration package

Creating a UEFI configuration package for Windows 365 Link is very similar to the process for doing the same with Surface. However, there are some differences explained in the following steps.

1. Install the [Surface IT Toolkit](/surface/surface-it-toolkit).
2. Have an USB key (16GB) available. This USB key is formatted during this process.
3. Follow the steps in [Create a Surface UEFI configuration package](/surface/surface-it-toolkit-uefi-config#create-a-surface-uefi-configuration-package) in the Surface documentation, with the following caveats:
    - For **Choose Deployment Build**, select **WinPE**.
    - For **Choose WinPE Package Type**, Select **Configuration Package**.
    - For **Choose Architecture**, select **x64**.
    - For **Select the Devices to be Configured**, select **Windows 365 Link**.
4. When you get to the **Final Review** page, insert or select the USB to be used to create the WinPE package.
5. When the device package creation is complete, note the last two characters of the certificate as this will be needed later and then select **Finish**.
6. Boot to WinPE using the newly created USB.
7. When prompted, enter the last two characters of the certificate thumbprint that you noted earlier.

## Unenroll devices from SEMM

The process to unenroll a Windows 365 Link device from SEMM is the same as the process to [Unenroll Surface devices from SEMM]( /surface/unenroll-surface-devices-from-semm).

<!-- ########################## -->
## Next steps

[Manage Windows 365 Link devices](device-management-overview.md)
