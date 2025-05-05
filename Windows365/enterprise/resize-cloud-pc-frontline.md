---
# required metadata
title: Resize Windows 365 Frontline Cloud PCs in dedicated mode
titleSuffix:
description: Learn how to resize Windows 365 Frontline Cloud PCs in dedicated mode.
keywords:
author: ErikjeMS  
ms.author: erikje
manager: dougeby
ms.date: 04/30/2025
ms.topic: overview
ms.service: windows-365
ms.subservice: windows-365-enterprise
ms.localizationpriority: high
ms.assetid: 

# optional metadata

#ROBOTS:
#audience:

ms.reviewer: abpineda
ms.suite: ems
search.appverid: MET150
#ms.tgt_pltfrm:
ms.custom: intune-azure; get-started
ms.collection:
- M365-identity-device-management
- tier2
---

# Resize Windows 365 Frontline Cloud PCs in dedicated mode (preview)

You can use a provisioning policy to resize Windows 365 Frontline Cloud PCs in dedicated mode.

Windows 365 Frontline Cloud PCs in shared mode can't be resized.

Resizing Windows 365 Frontline Cloud PCs in dedicated mode is in [public preview](..\public-preview.md).

For more information about resizing, see [Cloud PC resizing overview](resize-cloud-pc.md).

[!INCLUDE [Resize a Cloud PC requirements](../includes/resize-requirements.md)]

## Use a provisioning policy to resize Windows 365 Frontline Cloud PCs in dedicated mode

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431), select **Devices** > **Windows 365** > **Provisioning policies**.
2. Select a provisioning policy that includes an assignment with the Windows 365 Frontline Cloud PCs in dedicated mode that you want to resize.
3. On the policy page, select **Edit** next to **Assignments**.
4. On the **Assignments** tab, in the **Cloud PC size** column, select the Cloud PC Frontline entry that you want to resize. All Cloud PCs in the assignment will be resized.
5. In the **Select Cloud PC size** pane, under **Available sizes**, select the new Cloud PC size > **Next**.
6. On the **Assignments** page, select **Next**.
7. On the **Review + save** tab, select **Update** to initiate the resize.

You can monitor the progress of the resize on the **All Cloud PCs** page and the [**Cloud PC actions** report](report-cloud-pc-actions.md).

<!-- ########################## -->
## Next steps

For more information on Cloud PC sizes, see [Cloud PC size recommendations](cloud-pc-size-recommendations.md).
