---
# required metadata

title: How to configure conditions for automatic and recommended classification for Azure Information Protection | Azure Rights Management
description:
author: cabailey
manager: mbaldwin
ms.date: 07/29/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: e915f959-eafb-4375-8d2c-2f312edf2d29

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
#ms.reviewer: eymanor
#ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# How to configure conditions for automatic and recommended classification for Azure Information Protection

>*Applies to: Azure Information Protection preview*

**[ This information is preliminary and subject to change. During the preview, blank articles might be published as placeholders. ]**

When you configure conditions for a label, you can automatically assign a label to a document or email. Or, you can prompt users to select the label that you recommend: 

- Automatic classification applies to Word, Excel, and PowerPoint when files are saved, and apply to Outlook when emails are sent. You cannot use automatic classification for files that were previously manually labeled.
 
- Recommended classification applies to Word, Excel, and PowerPoint when files are saved.

When you configure conditions, you can use predefined patterns, such as “Credit card numbers” or “USA Social Security Number”. Or, you can define a custom string or pattern as a condition for automatic classification. For more information about the conditions, see the [Information about the built-in conditions](#information-about-the-built-in-conditions) section.

How multiple conditions are evaluated when they apply to more than one label:

1. The labels are ordered for evaluation, according to their position that you specify in the policy: The label positioned first has the lowest position (least sensitive) and the label positioned last has the highest position (most sensitive).

2. The most sensitive label is applied.
 
3. The last sub-label is applied.

> [!TIP]
>For the best user experience and to ensure business continuity, we recommend that you start with user recommended classification, rather than automatic classification. This configuration gives your users the ability to accept the labeling or protection action, or override these suggestions if they are not suitable for their document or email message.

An example prompt for when you configure a condition to apply a label as a recommended action, with a custom policy tip:

![Azure Information Protection detection and recommendation](../media/info-protect-recommend-callouts.png)

In this example, the user can click **Change now** to apply the recommended label, or override the recommendation by closing the bar.

## To configure recommended or automatic classification for a label

1. Make sure that you are signed in to the Azure portal by using this special link for Azure Information Protection: https://portal.azure.com/?microsoft_azure_informationprotection=true
 
2. On the hub menu, click **Browse** and start typing **Information** in the Filter box. Select **Azure Information Protection**.

3. On the **Azure Information Protection** blade, select the label that you want to configure for automatic or recommended classification.

4. On the **Label** blade, in the **Configure conditions for automatically applying this label** section, click **Add a new condition**.

5. On the **Condition** blade, select **Built-in** if you want to use a predefined condition, or **Custom** if you want to specify your own, and then click **Save**:

    - For **Built-in**: Select from the list of available conditions, and then select the minimum number of occurrences and whether the occurence should have a unique value to be included in the occurrence count.
        
        For more information about the detection rules for these conditions and some examples, see the [Information about the built-in conditions](#information-about-the-built-in-conditions) section.

    - For **Custom**: Specify a name and phrase to match, which must exclude quotation marks and special characters. Then specify whether to match as a regular expression, use case sensitivity, and the minimum number of occurrences and whether the occurence should have a unique value to be included in the occurrence count.
        
    **Example of the occurrences options**: You select the built-in social security number option and set the minimum number of occurrences as 2, and a document has the same social security number listed twice: If you set the **Count occurrences with unique values only** to **On**, the condition would not be met; if you set this option to **Off**, the condition would be met.

6. On the **Label** blade, configure the following, and then click **Save**:

    - Choose automatic or recommended classification: For **Select how this label is applied: automatically or recommended to user**, select **Automatic** or **Recommended**.

    - Specify the text for the user prompt or policy tip: Keep the default text or specify your own string.

7. To make your changes available to users, on the **Azure Information Protection** blade, click **Publish**.

## Information about the built-in conditions

During the preview period, you can select the following conditions:

- [SWIFT Code](#swift-code )

- [Credit Card Number](#credit-card-number )

- [ABA Routing Number](#aba-routing-number )

- [USA Social Security Number (SSN)](#usa-social-security-number-ssn)

- [International Banking Account Number (IBAN)](#international-banking-account-number-iban)


### SWIFT Code

Match this information type when the content includes the following:  

1. One of the following phrases: **swift**, **swiftnumber**, **swiftroutingnumber** 

2. A Swift code, in a formatted pattern:  

    a. 4 letters (bank code)  

    b. 2 letters (country code)  

    c. 2 letters or digits (location code)  

    d. Optional 3 letters or digits (branch code)  


Examples for testing:

- **NEDSZAJJXXX Swiftroutingnumber**

- **NEDSZAJJ100 Swiftnumber** 

----


### Credit Card Number

Match this information type when the content includes the following:  

- A valid credit card number, in a formatted or unformatted pattern, that  passes the [luhn check](https://wikipedia.org/wiki/Luhn_algorithm). This information type detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, American Express, and Diners.

    - **Formatted**:
    
        - 16 digits: (dddd-dddd-dddd-dddd)  
        
    - **Unformatted**:
    
        - (dddddddddddddddd)  


Examples for testing:

- **4242-4242-4242-4242**

- **4242424242424242** 

----

### ABA Routing Number

Match this information type when the content includes the following:  

1. At least one of the following phrases: **aba**, **rtn**, **routing number** 

2. An ABA routing number, which includes 9 digits that can be in a formatted or unformatted pattern: 

    - **Formatted**: 
        
        a. Four digits that start with 0, 1, 2, 3, 6, 7, or 8 
        
        b. A hyphen 
        
        c. Four digits 
        
        d. A hyphen 
        
        e. A digit 
        
        Example: 3456-9876-1 ABA 
        
    - **Unformatted**: 
        
        9 consecutive digits that start with 0, 1, 2, 3, 6, 7, or 8 
        
        Example: 345698761 RTN 
 

Examples for testing:

- **3456-9876-1 ABA**

- **345698761 RTN** 

----

### USA Social Security Number (SSN)

Match this information type when the content includes the following:  

1. At least one of the following phrases: **ssn**, **social security**, **ssid**, **ss#** 

2. A social security number: 9 digits, which can be in a formatted or unformatted pattern:

    - **Formatted**: 
    
        - Nine digits in the following format: ddd-dd-dddd OR ddd dd dddd 
        
    - **Unformatted**: 
    
        - Nine digits in the following format: ddddddddd 


Examples for testing:

- **SSN 123-45-6789**

- **SS# 123456789** 


----

### International Banking Account Number (IBAN)

Match this information type when the content includes the following:  

1. The following phrase: **IBAN** 

2. An IBAN number: Starts with a country code (two letters), then check digits (two digits), then bban number (up to and including 30 digits).


Examples for testing:

- **GB29 NWBK 6016 1331 9268 19 IBAN**


## Next steps

For more information about configuring your Azure Information Protection policy, use the links in the [Configuring your organization's policy](configure-policy.md#configuring-your-organization-s-policy) section.  



