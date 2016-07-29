---
# required metadata

title: How to configure a label for visual markings for Azure Information Protection | Azure Rights Management
description:
author: cabailey
manager: mbaldwin
ms.date: 07/29/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: df2676eeb062-f25a-4cf8-a782-e59664427d54

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
#ms.reviewer: eymanor
#ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# How to configure a label for visual markings for Azure Information Protection

>*Applies to: Azure Information Protection preview*

**[ This information is preliminary and subject to change. During the preview, blank articles might be published as placeholders. ]**

When you assign a label to a document or email message, you can select several options to make the chosen classification easily visible. These visual markings are a header, a footer, and a watermark:

The visual markings are applied to Word, Excel, and PowerPoint documents when the label is applied, and when the documented is saved. For email messages, the visual markings are applied when the email message is sent.

Additional information about these visual markers:

- Headers and footers apply to Word, Excel, PowerPoint, and Outlook.

- Watermarks apply to Word, Excel, and PowerPoint:

    - Excel: Watermarks are visible only in Page layout and Print preview modes, and when printed.

	- PowerPoint: Watermarks are applied to the master slide, as a background image.

Use the following instructions to configure visual markings for a label.

1. Sign in to the [Azure portal](https://portal.azure.com).
 
2. On the hub menu, click **Browse** and start typing **Information** in the Filter box. Select **Azure Information Protection**.

3. On the **Azure Information Protection** blade, select the label that you want to configure for visual markings.

4. On the **Label** blade, in the **Set visual marking (such as header or footer)** section, configure the settings for the visual markers that you want, and then click **Save**:

    - To configure a header: For **Documents with this label have a header**, select **On** if you want a header, and **Off** if you do not. If you select **On**, then specify the header text, size, color, and alignment for the header.

    - To configure a footer: For **Documents with this label have a footer**, select **On** if you want a footer, and **Off** if you do not. If you select **On**, then specify the footer text, size, color, and alignment for the header.

    - To configure a watermark: For **Documents with this label have a watermark**, select **On** if you want a watermark, and **Off** if you do not. If you select **On**, then specify the watermark text, size, color, and layout for the header.

5. To make your changes available to users, on the **Azure Information Protection** blade, click **Publish**.

## Next steps

For more information about configuring your Azure Information Protection policy, use the links in the [Configuring your organization's policy](configure-policy.md#configuring-your-organization-s-policy) section.  


