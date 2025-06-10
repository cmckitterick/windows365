---
# required metadata
title: Concurrency buffer for Windows 365 Frontline Cloud PCs in dedicated mode
titleSuffix:
description: Learn about the concurrency buffer for Windows 365 Frontline Cloud PCs in dedicated mode.
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

# Concurrency buffer for Windows 365 Frontline Cloud PCs in dedicated mode

Windows 365 Frontline in dedicated mode includes a concurrency buffer to let a tenant temporarily exceed the maximum concurrency limit for Windows 365 Frontline Cloud PCs.

For example, when workers overlap during a shift change, a previous worker might need to finish up something before signing off. Or, an incoming worker might need to start a few minutes early. The concurrency buffer is intended to allow for such rare and brief over usage to make sure workers aren’t impacted by unforeseen lockouts.

The concurrency buffer can be used up to four times per day with maximum of one hour in each instance. This hour starts from the moment the tenant exceeded the max concurrency limit.

### Temporary blocks

Excessive use of the concurrency buffer temporarily blocks its further use for the next 48 hours. A temporary block is imposed when:

- On four or more occasions within a 24-hour period, the concurrency buffer is used for more than one hour.

While temporarily blocked, you can still use your Windows 365 Frontline Cloud PCs in dedicated mode up to the maximum concurrency limit.

### Permanent blocks

If the tenant is temporarily blocked more than two times in a seven day period, the tenant is permanently blocked from using the concurrency buffer.

While permanently blocked, you can still use your Frontline Cloud PCs up to the maximum concurrency limit.

To unblock your tenant, open a ticket with support from the Intune portal.

### Monitor the concurrency buffer

You can monitor the use of concurrency buffer with the Frontline connection hourly report. You can use the Frontline concurrency alert to receive alerts each time the concurrency buffer is activated. The concurrency buffer doesn't apply to GPU-enabled Cloud PCs and Frontline Cloud PCs in shared mode.

## Next steps

For more information about Windows 365 Frontline, see:

- [What is Windows 365 Frontline?](introduction-windows-365-frontline.md)
- [Windows 365 Frontline licensing](frontline-license.md)