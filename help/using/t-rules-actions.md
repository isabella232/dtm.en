---
description: Set up actions that you want the condition to trigger.
keywords: dynamic tag management
seo-description: Set up actions that you want the condition to trigger.
seo-title: Set up actions for the condition to trigger
solution: Analytics,Marketing Cloud,Dynamic Tag Management
title: Set up actions for the condition to trigger
uuid: 407b9f59-7d97-4703-b2ae-6cd157390e3a
index: y
internal: n
snippet: y
---

# Set up actions for the condition to trigger

Set up actions that you want the condition to trigger.

After setting up the condition, you must set up the actions that you want the condition to trigger. These actions can include [!DNL Analytics] events, third-party tags, and custom scripts. This example describes how to set up scripts or third-party tags.

Beyond integrated tools like [!DNL Adobe Analytics] and Google Analytics, dynamic tag management can trigger any type of JavaScript or inject HTML into your site, in select pages or in specific scenarios.

Each rule can trigger as many scripts or HTML injections as you want.

>[!NOTE]
>
>Because DTM allows you to inject custom code into your page, please take care not to create cross-site scripting (XSS) vulnerabilities (see [OWASP’s guide](https://www.owasp.org/index.php/Cross-site_Scripting_(XSS)) for more info). Using data elements within a script requires particular attention. Always assume data element values might come from an untrusted source.

**To set up actions for the condition to trigger** 

1. Click **[!UICONTROL JavaScript / Third Party Tags]** to add a new script to your rule.

   ![](assets/scripts_actions.png)

1. Click **[!UICONTROL Add New Script]**.

   ![](assets/scripts_actions2.png)

1. Name the script.
1. Specify how you want the script to trigger, and paste the desired content into the text area. ![](assets/scripts_actions3.png)

1. Click **[!UICONTROL Save Code]**, and the script will be added to the queue for the rule. ![](assets/scripts_actions4.png)

