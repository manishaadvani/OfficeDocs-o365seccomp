---
title: "Set up Office 365 ATP Safe Attachments policies"
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 078eb946-819a-4e13-8673-fe0c0ad3a775
description: "Define Safe Attachments policies to protect your organization from malicious files in email."
---

# Set up Office 365 ATP Safe Attachments policies

People regularly send, receive, and share attachments, such as documents, presentations, spreadsheets, and more. It's not always easy to tell whether an attachment is safe or malicious just by looking at an email message. And the last thing you want is a malicious attachment to get through, wreaking havoc for your organization. Fortunately, [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) can help. You can set up [ATP Safe Attachments](atp-safe-attachments.md) policies to help ensure that your organization is protected against attacks by unsafe email attachments. 
  
## What to do 
  
1. [Review the prerequisites](#review-the-prerequisites)
    
2. [Set up an ATP Safe Attachments policy](#set-up-an-atp-safe-attachments-policy)
    
3. [Learn about ATP Safe Attachments policy options](#learn-about-atp-safe-attachments-policy-options)
    
## Step 1: Review the prerequisites

- Make sure that your organization has [Office 365 Advanced Threat Protection](office-365-atp.md).
    
- Make sure that you have the necessary [permissions for the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).
    
- [Learn about ATP Safe Attachments policy options](#learn-about-atp-safe-attachments-policy-options) (in this article). Some options, such as the Monitor or Replace options, can result in a minor delay of email while attachments are scanned. To avoid message delays, consider using [Dynamic Delivery and previewing](dynamic-delivery-and-previewing.md).
    
- Allow up to 30 minutes for your new or updated policy to spread to all Office 365 datacenters.
    
## Step 2: Set up (or edit) an ATP Safe Attachments policy
  
1. As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account. 
    
2. In the Office 365 Security &amp; Compliance Center, in the left navigation pane, under **Threat management**, choose **Policy** \> **Safe Attachments**.
    
3. If you see **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**, we recommend that you select this option. This will enable [Office 365 Advanced Threat Protection for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) for your Office 365 environment. 
    
4. Choose **New** (the New button resembles a plus sign ( **+**)) to start creating your policy.
    
5. Specify the name, description, and settings for the policy.<br/><br/>**Example:** To set up a policy called "no delays" that delivers everyone's messages immediately and then reattaches attachments after they're scanned, you might specify the following settings: 
    
      - In the **Name** box, type no delays.
    
      - In the **Description** box, type a description like, Delivers messages immediately and reattaches attachments after scanning.
    
      - In the response section, choose the **Dynamic Delivery** option. ([Learn more about Dynamic Delivery and previewing with ATP Safe Attachments](dynamic-delivery-and-previewing.md).)
    
      - In the **Redirect attachment** section, select the option to enable redirect and type the email address of your Office 365 global administrator, security administrator, or security analyst who will investigate malicious attachments. 
    
      - In the **Applied To** section, choose **The recipient domain is**, and then select your domain. Choose **Add**, and then choose **OK**.
    
6. Choose **Save**.
    
Consider setting up multiple ATP Safe Attachments policies for your organization. These policies will be applied in the order they're listed on the **ATP Safe Attachments** page. After a policy has been defined or edited, allow at least 30 minutes for the polices to take effect throughout Microsoft datacenters. 
  
## Step 3: Learn about ATP Safe Attachments policy options

As you set up your ATP Safe Attachments policies, you choose from among many options, including Monitor, Block, Replace, Dynamic Delivery, and so on. In case you're wondering about what these options do, the following table summarizes each and its effect.
  
|**Option**|**Effect**|**Use when you want to:**|
|:-----|:-----|:-----|
|**Off** <br/> |Does not scan attachments for malware  <br/> Does not delay message delivery  <br/> |Turn scanning off for internal senders, scanners, faxes, or smart hosts that will only send known, good attachments  <br/> Prevent unnecessary delays in routing internal mail  <br/> **This option is not recommended for most users. It enables you to turn ATP Safe Attachments scanning off for a small group of internal senders.**           |
|**Monitor** <br/> |Delivers messages with attachments and then tracks what happens with detected malware  <br/> |See where detected malware goes in your organization  <br/> |
|**Block** <br/> |Prevents messages with detected malware attachments from proceeding  <br/> Sends messages with detected malware to [quarantine in Office 365](manage-quarantined-messages-and-files.md) where a security administrator or analyst can review and release (or delete) those messages  <br/> Blocks future messages and attachments automatically  <br/> |Safeguard your organization from repeated attacks using the same malware attachments  <br/> |
|**Replace** <br/> |Removes detected malware attachments  <br/> Notifies recipients that attachments have been removed  <br/> Sends messages with detected malware to [quarantine in Office 365](manage-quarantined-messages-and-files.md) where a security administrator or analyst can review and release (or delete) those messages  <br/> |Raise visibility to recipients that attachments were removed because of detected malware  <br/> |
|**Dynamic Delivery** <br/> |Delivers messages immediately  <br/> Replaces attachments with a placeholder file until scanning is complete, and then reattaches the attachments if no malware is detected  <br/> Includes attachment previewing capabilities for most PDFs and Office files during scanning  <br/> Sends messages with detected malware to Quarantine where a security administrator or analyst can review and release (or delete) those messages  <br/> [Learn about Dynamic Delivery and previewing with ATP Safe Attachments](dynamic-delivery-and-previewing.md) <br/> |Avoid message delays while protecting recipients from malicious files  <br/> Enable recipients to preview attachments in safe mode while scanning is taking place  <br/> |
|**Enable redirect** <br/> |Applies when the Monitor, Block, or Replace option is chosen  <br/> Sends attachments to a specified email address where security administrators or analysts can investigate  <br/> |Enable security administrators and analysts to research suspicious attachments  <br/> |
   
## Next steps

Once your ATP Safe Attachments policies are in place, you can see how ATP is working for your organization by viewing reports. See the following resources to learn more:
- [View reports for Office 365 Advanced Threat Protection](view-reports-for-atp.md)
- [Use Explorer in the Security &amp; Compliance Center](use-explorer-in-security-and-compliance.md)
 