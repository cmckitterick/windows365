---
# required metadata
title: Change screen time-out for Windows 365 Link devices
titleSuffix:
description: Learn how to change screen time-out for Windows 365 Link devices
keywords:
author: ErikjeMS  
ms.author: erikje
manager: dansimp
ms.date: 05/16/2025
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

# Change screen time-out for Windows 365 Link devices

By default, Windows 365 Link has a default screen time-out that turns off the display after about five minutes of inactivity. This time-out acts like a [local Lock event](sign-in.md), and when the user wakes the device, it opens on the sign-in screen. You can change this time-out by using Intune's **Turn off the display (plugged in)** setting.

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431) > **Devices** > **Configuration** (under **Manage devices**) > **Create** > **New Policy**.
2. Under **Create a profile**, select the following options:
    - **Platform**: **Windows 10 and later**
    - **Profile Type**: **Settings catalog**
3. Select **Create**.
4. Enter a **Name** for the policy, like "Windows 365 Link Screen Timeout" and a useful **Description**.
5. Select **Next**.
6. On the **Configuration settings** page, select **Add settings**.
7. Search for **Video and Display** and select that category.
8. Select **Turn off the display (plugged in)** and close the **Settings picker**.
9. Expand **Administrative Templates** and set **Turn off the display (plugged in)** to **Enabled**.
10. Set **When plugged in, turn display off after (seconds)** to your preferred value.
11. Select **Next**.
12. On the **Scope tags** page, select any desired scope tags to apply, then select **Next**.
13. On the **Assignments** page, target Windows 365 Link devices per your preferred method. For example, you can use **Add all devices** with an **Include** filter using a Windows 365 Link device filter. This filter targets the policy at all Windows 365 Link devices.
12. Select **Next**.
13. On the **Review + create** page, review the settings.
14. Select **Create** to deploy the profile.

<!-- ########################## -->
## Next steps

[Manage Windows 365 Link devices](device-management-overview.md)
