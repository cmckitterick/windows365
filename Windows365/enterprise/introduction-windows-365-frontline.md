---
# required metadata
title: What is Windows 365 Frontline?
titleSuffix:
description: Learn about Windows 365 Frontline.
keywords:
author: ErikjeMS  
ms.author: erikje
manager: dougeby
ms.date: 06/20/2025
ms.topic: overview
ms.service: windows-365
ms.subservice: windows-365-enterprise
ms.localizationpriority: high
ms.assetid: 

# optional metadata

#ROBOTS:
#audience:

ms.reviewer: gkomatsu
ms.suite: ems
search.appverid: MET150
#ms.tgt_pltfrm:
ms.custom: intune-azure; get-started
ms.collection:
- M365-identity-device-management
- tier2
---

# What is Windows 365 Frontline?

Windows 365 Frontline is a version of [Windows 365](../overview.md) that helps organizations save costs by letting them provision a Cloud PC that can be used by multiple users with a single [license](frontline-license.md).

Windows 365 Frontline is currently only available for Azure Global Cloud.

Frontline Cloud PCs can't be accessed directly from Remote Desktop app. Instead, you must use Windows App if you want to access your Frontline Cloud PC. You can find [Windows App](/windows-app/overview) at the [Microsoft Store](https://apps.microsoft.com/detail/9n1f85v9t8bn?ocid=pdpshare&hl=en-us&gl=US) or access [windows.cloud.microsoft](https://windows.cloud.microsoft) with your browser.

Windows 365 Frontline has two different modes: dedicated mode and shared mode.

## Windows 365 Frontline in dedicated mode

A single license:

- Lets you provision up to three Cloud PCs that can be used nonconcurrently, each assigned to a single user.
- Provides one concurrent session.

Windows 365 Frontline dedicated mode is designed specifically for workers who need a dedicated Cloud PC but don't need 24/7 access. This system better supports organizations that are more elastic and distributed, working across various devices. Frontline Cloud PCs in dedicated mode can be helpful for users who are:

- On a rotation schedule.
- Working across time zones and regions.
- Part-time workers.
- Contingent staff.

The maximum number of active Windows 365 Frontline Cloud PC sessions in your organization is equal to the number of Windows 365 Frontline licenses that you purchased. For example, if you purchase 10 licenses, up to 30 Cloud PCs can be provisioned in dedicated mode. Ten of those Cloud PCs can be active at a given time. The active sessions are managed automatically. When a user signs off from their Cloud PC, the session is released for another user to start using their Cloud PC. A concurrency buffer exists to exceed the maximum a limited number of times per day. For more information, see [Exceeding the maximum concurrency limit](#exceeding-the-maximum-concurrency-limit).

> [!NOTE]
>
> Windows 365 Frontline Cloud PCs in dedicated mode will automatically power off after the user signs off from the Cloud PC, and will be powered on when the user attempts to connect. It may take more time for the user to connect when the Cloud PC is being powered on. This connection time does not include executing logon scripts set by organizations.
> After the user signs off, the Cloud PC remains powered on for two hours. If the user attempts to reconnect while the Cloud PC is powered on, the connection time will be same as Windows 365 Enterprise Cloud PCs.

## Windows 365 Frontline in shared mode

A single license:

- Lets you provision one Cloud PC that can be shared noncurrently among a group of users.
- Provides one concurrent session.

Windows 365 Frontline in shared mode is designed specifically for workers who

- Require access to a Cloud PC to perform specialized tasks for a short time during their work day.
- Don't require data persistence.

Frontline Cloud PCs in shared mode can be helpful for users who are:

- Customer-facing workers.
- External contractors.

The maximum number of active Windows 365 Frontline Cloud PC sessions in your organization is equal to the number of Windows 365 Frontline licenses that you set up for a specific group. For example, if you assign 10 Windows 365 Frontline shared licenses, 10 Cloud PCs can be provisioned for the group. Only a single user can connect to a shared Cloud PC at a given time. When a user signs out from the Cloud PC, all user data is deleted and the Cloud PC is released for another user to start using. Concurrency buffer doesn't exist for a Frontline Cloud PC in shared mode.  

### Monitor the concurrency buffer

You can monitor the use of concurrency buffer with the Frontline connection hourly report. You can use the Frontline concurrency alert to receive alerts each time the concurrency buffer is activated. The concurrency buffer doesn't apply to GPU-enabled Cloud PCs and Frontline Cloud PCs in shared mode.

## Features not yet supported Windows 365 Frontline

The following features aren't yet supported for Windows 365 Frontline.

- Resize a Cloud PC remote action
- Cross region disaster recovery
- [Microsoft Purview Customer Key](purview-customer-key.md)

Windows 365 Frontline in shared mode can only be provisioned in the following Azure regions:

- Australia East
- Canada Central
- North Europe
- Central India
- Japan East
- Japan West
- South Africa North
- UK South
- Central US
- East US
- East US 2
- West US 3
- South Central US
- East Asia
- Southeast Asia

## Next steps

For more information about Windows 365 Frontline, see:

- [Bulk reprovision Windows 365 Frontline Cloud PCs in shared mode](frontline-shared-bulk-reprovision.md)
- [Connected Frontline Cloud PCs report](report-connected-frontline-cloud-pcs.md)
- [Windows 365 Frontline licensing](frontline-licensing.md)
