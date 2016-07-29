---
# required metadata

title: Azure Information Protection quick start tutorial step 4 | Azure Rights Management
description: Step 4 of an introduction tutorial to quickly try out Microsoft Azure Information Protection for your organization with just 4 steps that should take you less than 15 minutes.
author: cabailey
manager: mbaldwin
ms.date: 07/29/2016
ms.topic: article
ms.prod: azure
ms.service: rights-management
ms.technology: techgroup-identity
ms.assetid: 468748c1-49d6-4c3e-a612-9c584acdc782

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
#ms.reviewer: eymanor
#ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Step 4: See classification, labeling, and protection in action 

>*Applies to: Azure Information Protection preview*

**[ This information is preliminary and subject to change. During the preview, blank articles might be published as placeholders. ]**

Now that you've got a Word document open with the Azure Information Protection client installed, you're ready to see how easy it is to start labeling and protecting your document, using the policy that we configured.

Classification and protection happens when you save the document, but before we do that, we'll use our unsaved document to see how easy it is to apply and change labels.

### To manually change our default label:

- On the Information Protection bar, click the Edit label icon next to **Internal**. This displays the available labels. Choose **Personal** and you are prompted to justify why are lowering the classification level. Select **This file no longer requires that classification**, and click **Confirm**.  

    You'll see the **Sensitivity** value change to **Personal**.

    ![Azure Information Protection quick start tutorial step 4 - prompt to confirm why lowering](../media/confirm-lowering.png)

### To remove the classification completely:

- On the Information Protection bar, click the Edit label icon next to **Personal**. This displays the available labels. But instead of choosing one of the labels, this time, click the Remove label icon. Click **OK** to confirm and provide justification for this action.  

    You'll see the **Sensitivity** value display **Not set**, which is what users see initially if you don't set a default label.

    ![Azure Information Protection quick start tutorial step 4 - remove classification](../media/sensitivity-not-set.png)


### To see a recommendation prompt for labeling and automatic protection:

1. In the Word document, type a valid credit card number, for example: **4242-4242-4242-4242**. 

2. Save the document (use any file name, any location). 

3. You now see the prompt: **It is recommended to label this file as Confidential**. Click **Change now**.

    ![Azure Information Protection quick start tutorial step 4 - recommend prompt](../media/change-now.png)

    Immediately, you'll see the watermark of your organization name across the page, in addition to the footer of **Sensitivity: Confidential**. 

    If you chose the option to apply an RMS template, the document is also protected with the Azure Rights Management template you specified, which you can confirm when you click the **File** tab and view the information for **Protect Document**. If you used the default Confidential template, you'll see the information that the document is restricted to internal users (users outside your organization will not be able to open the document) and its contents cannot be copied or printed. As the owner of the document, you can copy from it and print it, but if you email it to another user in your organization, they won't be able to do these actions.

> [!NOTE]
>If you have any problems completing these steps, on the **Home** tab, in the **Protection** group, click **Protect**, and then click **Help and feedback**. 
>
>In the **Microsoft Azure Information Protection** dialog box, click **Send feedback**. This emails the Information Protection team, and automatically attaches log files from your PC to help diagnose any problems.

##  Next steps

Now you've seen the default Azure Information Protection policy and how to customize it, and how labeling works for a Word document, try some of the other settings and see how they work in the other Office applications that support Azure Information Protection: Excel, PowerPoint, Outlook. If these applications were open when you installed the Azure Information Protection client, close and reopen them before you try using them with Azure Information Protection.

For example, you can change the default title of **Sensitivity** on the Information Protection bar to a title of your own choice. You can change the tooltips, the label colors, the order of the labels, and their names. You can create new labels and define your own automatic rules. You can fine-tune your watermarks, by configuring the size, color, and change from diagonal to horizontal.

Note that if you're using watermarks with Excel, they are visible only in Page layout and Print preview modes, and when printed.

Each time you change any settings in the Azure portal for the Information Protection policy, remember to **save** the policy and then **publish** it. Because you can make changes on multiple blades, it's a good idea to check that all blades do not show the **Save** button as enabled, which indicates that you have unsaved changes. If your Office application was open when you published new changes, close your application and reopen it to download the latest policy.

When you've finished your own testing, you might find it useful to look over the [frequently asked questions for Azure Information Protection](faq.md).

