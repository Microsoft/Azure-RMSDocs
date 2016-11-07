﻿---
# required metadata

title: What is Azure Information Protection? | Azure Information Protection
description: An overview of the Azure Information Protection service.
author: cabailey
manager: mbaldwin
ms.date: 10/12/2016
ms.topic: article
ms.prod:
ms.service: information-protection
ms.technology: techgroup-identity
ms.assetid: cd8a88e2-3555-4be2-9637-3cdee992f2c8

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
#ms.reviewer: eymanor
#ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# What is Azure Information Protection?

>*Applies to: Azure Information Protection*

Azure Information Protection is a cloud-based solution that helps an organization to classify, label, and protect its documents and emails. This can be done automatically by administrators who define rules and conditions, manually by users, or a combination where users are given recommendations. 

The following picture shows an example of Azure Information Protection in action. The administrator has configured rules to detect sensitive data (in this case, credit card information). When a user saves a Word document that contains credit card information, she sees a custom tooltip that recommends she applies a specific label that the administrator configured, which classifies and optionally, protects the document. 

![Example of recommended classification for Azure Information Protection](../media/info-protect-recommend-callouts.png)

After your content is classified (and optionally protected), you can then track and control how it is used. You can analyze data flows to gain insight into your business, detect risky behaviors and take corrective measures, track access to documents, prevent data leakage or misuse, and so on.


![Example email footer and headers showing Azure Information Protection classification](../media/example-email-footer-header.png)


## How data is protected

The protection technology uses *Azure Rights Management* (often abbreviated to Azure RMS). This technology is integrated with other Microsoft cloud services and applications, such as Office 365 and Azure Active Directory. It can also be used with your own line-of-business applications and information protection solutions from software vendors, whether these applications and solutions are on-premises, or in the cloud.

This protection technology uses encryption, identity, and authorization policies. Similarly to the persistent labels, protection that is applied by using Rights Management stays with the documents and emails, independently of the location—inside or outside your organization, networks, file servers, and applications. This information protection solution keeps you in control of your data, even when it is shared with other people.

For example, you can configure a report document or sales forecast spreadsheet so that it can be accessed only by people in your organization, and control whether that document can be edited, or restricted to read-only, or prevent it from being printed. You can configure emails similarly, and in addition, prevent them from being forwarded or prevent the use of the Reply All option. These protection tasks can be simplified and streamlined by using *rights management templates*.

### Rights management templates

As soon as you activate the Azure Rights Management service, two default templates are created for you that restricts data access to users within your organization. You can use these templates to immediately help prevent data leaking from your organization. You can also supplement these default templates by configuring your own custom templates that apply more restrictive controls.

These templates can be part of a label's configuration, so that when a specific label is applied to a document (or email message), the data is both classified and automatically protected. The templates can also be selected by users or administrators in products and services that support the Azure Rights Management technology.

This example shows how you might select a template for a label when you configure the Azure Information Protection policy from the Azure portal:

![Example of selecting templates in the Azure portal](../media/templates-infoprotection-callouts.png)

The same templates can be selected from the Exchange admin center, to configure Exchange Online mail flow rules, which support the Azure Rights Management technology:

![Example of selecting templates for Exchange Online](../media/templates-exchangeonline-callouts.png)

For more information about the Azure Rights Management protection, see [What is Azure Rights Management?](what-is-azure-rms.md)

## Integration with end user workflows

Azure Information Protection integrates with end users' existing workflows when the Azure Information Protection client is installed. This client installs the Information Protection bar to Office applications, which we saw in the first picture. The same bar is added to Excel, PowerPoint, and Outlook. For example:

![Example of the Azure Information Protection bar in Excel](../media/excel2013-infoprotect-bar2.png)

This Information Protection bar makes it easy for end users to select labels for the correct classification, and where required, these labels can also automatically protect their documents and emails.

When users share their protected documents by email, they can use a document tracking site to monitor who is accessing these documents and when. If they suspect misuse, they can also revoke access to these documents.


## Resources for Azure Information Protection

- Announcement: [Azure Information Protection is now Generally Available](https://blogs.technet.microsoft.com/enterprisemobility/2016/10/04/azure-information-protection-is-now-generally-available/)

- Free trial: [Enterprise Mobility + Security E5](https://portal.office.com/Signup/Signup.aspx?OfferId=87dd2714-d452-48a0-a809-d2f58c4f68b7)

- Download the client: [Azure Information Protection client](https://www.microsoft.com/en-us/download/details.aspx?id=53018)

- FAQs: [Frequently asked questions for Azure Information Protection](../get-started/faqs.md)

- Yammer: [Azure Information Protection](https://www.yammer.com/askipteam/#/threads/inGroup?type=in_group&feedId=8652489&view=all)

- Video overview

    <iframe width="560" height="315" src="https://www.youtube.com/embed/N9Ip0m6d3G0" frameborder="0" allowfullscreen></iframe>

    In addition, Microsoft Ignite 2016 offers many on-demand sessions for Azure Information Protection:

    - [BRK2127: Adopt a comprehensive identity-driven solution for protecting and sharing data securely](https://myignite.microsoft.com/videos?q=BRK2127)
    
    - [THR2107: Collaborate securely using Azure Information Protection](https://myignite.microsoft.com/videos?q=THR2107)
    
    - [THR2108: Ensure comprehensive protection of your data with Azure Information Protection](https://myignite.microsoft.com/videos?q=THR2108)
    
    - [BRK3095: Learn how classification, labeling, and protection delivers persistent data protection](https://myignite.microsoft.com/videos?q=BRK3095)
    
    - [BRK2128: Send secure email to anyone with the power of Microsoft Office 365 and Azure Information Protection](https://myignite.microsoft.com/videos?q=BRK2128)


## Next steps

Configure and see Azure Information Protection for yourself, with our 5-step [Quick start tutorial for Azure Information Protection](../get-started/infoprotect-quick-start-tutorial.md).

Know Azure Information Protection or Azure Rights Management by another name? See [our list of alternative terms for the service](azure-rms-aka.md).
