---
# required metadata

title: Azure Information Protection quick start tutorial | Azure Rights Management
description: An introduction tutorial to quickly try out Microsoft Azure Information Protection for your organization with just 4 steps that should take you less than 15 minutes.
author: cabailey
manager: mbaldwin
ms.date: 07/29/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: 1260b9e5-dba1-41de-84fd-609076587842

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
#ms.reviewer: eymanor
#ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Quick start tutorial for Azure Information Protection 

>*Applies to: Azure Information Protection preview*

**[ This information is preliminary and subject to change. During the preview, blank articles might be published as placeholders. ]**

Use this tutorial to quickly try out Azure Information Protection preview for your organization, with just 4 steps that should take you less than 15 minutes. Optionally, you’ll activate the Azure Rights Management service, look at and modify the default Azure Information Protection policy, install the Azure Information Protection client, and then use a Word document to see classification, labeling, and protection in action.

This tutorial is aimed at IT administrators and consultants, to help them evaluate Azure Information Protection as an enterprise information protection solution for an organization. In a production environment, the instructions to activate the service, configure the Information Protection policy, and install the client for users would be done by an administrator. The instructions to label the document would be done by end users. Both sets of instructions are included in this tutorial, to demonstrate the end-to-end scenario of classifying, labeling, and protecting your organization's data. 

If you have any problems completing this tutorial, using the preview release of Azure Information Protection, or want to see what others are saying about it, head over to the [Azure Information Protection Yammer site](https://www.yammer.com/askipteam/#/threads/inGroup?type=in_group&feedId=8652489&view=all).

## Prerequisites 
To complete this tutorial, you will need the following:

- Any subscription that includes Azure Rights Management, which will give you access to the preview release of Azure Information Protection. Azure Information Protection is available in all regions that support Azure Rights Management. For more information about the available subscriptions and links to free trials, see [Azure RMS requirements: Cloud subscriptions that support Azure RMS](../get-started/requirements-subscriptions.md).

- A subscription for Azure, so you can access the Azure portal, to configure the Azure Information Protection policy. If you do not already have an Azure subscription for your organization, you can get one by signing up for a free trial: Go to the [Azure Get started page](https://account.windowsazure.com/organization) and follow the instructions.

  > [!TIP] 
  > If you need to get one or both of these subscription, do this in advance because this process can sometimes take a while to complete.

- A global administrator account to sign in to the Office 365 admin center or the Azure classic portal if you need to activate the Rights Management service. This account must also have an email address and a working email service (for example, Exchange Online or Exchange Server).

- A computer running Windows (minimum of Windows 7 with Service Pack 1), and which has installed either Office Professional Plus 2016, Office Professional Plus 2013 with Service Pack 1, or Office Professional Plus 2010. 

- If you have Active Directory Rights Management Services (AD RMS) deployed in your organization: The computer must be a workgroup computer that has not previously used AD RMS. This is required if you want to protect documents, and ensures that the computer downloads templates only from Azure Rights Management. It is not supported for a computer to connect to both AD RMS and Azure RMS at the same time. If you are interested in migration information, see [Migrating from AD RMS to Azure Rights Management](../plan-design/migrate-from-ad-rms-to-azure-rms.md).   

Let's get started.

>[!div class="step-by-step"]
[&#187; Step 1](infoprotect-tutorial-step1.md)


