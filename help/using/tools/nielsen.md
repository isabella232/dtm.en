---
description: You can enable Nielsen tracking using dynamic tag management by creating the Nielsen tool and configuring the page code either automatically or manually. The automatic method is recommended for most users.
seo-description: You can enable Nielsen tracking using dynamic tag management by creating the Nielsen tool and configuring the page code either automatically or manually. The automatic method is recommended for most users.
seo-title: Nielsen Tool
title: Nielsen Tool
uuid: cf0c80e5-ab15-42a7-9291-fc0572292538
index: y
internal: n
snippet: y
---

# Nielsen Tool

You can enable Nielsen tracking using dynamic tag management by creating the Nielsen tool and configuring the page code either automatically or manually. The automatic method is recommended for most users.

* [Prerequisites](../tools/nielsen.md#section_44B0B2C13E5E495FA1F6C424C7239B6D) 
* [Add the Nielsen Tool](../tools/nielsen.md#section_E656FC0A6CD24EC2AB12130E8E043BE2) 
* [Set Up Nielsen Rules in DTM](../tools/nielsen.md#section_C3D440E62D4B487BB2D30F06CEC51BA5) 
* [Approve and Publish All Changes](../tools/nielsen.md#section_9948D02D35FC423FA44101C221265C0B)

## Prerequisites {#section_44B0B2C13E5E495FA1F6C424C7239B6D}

You must perform the following tasks before you deploy the Nielsen tool:

<table id="table_5F72D90F206C4D1B9D67FDF62D7EB61F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Task </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>1.</b> Embed dynamic tag management on the site (all site webpages). </p> </td> 
   <td colname="col2"> <p> You can add header and footer code that determines the loading of JavaScript and page content on your site. You must install both the header and footer code on every page of your site, regardless of the <a href="../deployment/deployment.md#concept_09612483C4934E16B20F5E9DA3B7EB7D" format="dita" scope="local"> hosting option </a> used. </p> <p>For more information, see <a href="../deployment/deployment.md#concept_3F6A0A508F294FCBABEBA1DF540B781B" format="dita" scope="local"> Header and Footer Code </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>2.</b> Add the Experience Cloud ID Service tool. </p> </td> 
   <td colname="col2"> <p>The <span class="keyword"> Experience Cloud Visitor ID Service </span> provides a universal visitor ID across <span class="keyword"> Experience Cloud </span>solutions. The visitor ID service replaces the legacy Analytics visitor ID mechanism, and is required by <span class="keyword"> Analytics </span> for <span class="keyword"> Target </span>; <span class="keyword"> video heartbeat </span>; and <span class="keyword"> Experience Cloud </span> integrations, including the Adobe/Nielsen integration. </p> <p>For general information about the service, see the <a href="https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid_service.html" format="https" scope="external"> Experience Cloud Visitor ID Service Guide </a>. </p> <p>For information about adding the Experience Cloud ID Service tool in DTM, see <a href="https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-dtm-settings.html" format="html" scope="external"> Experience Cloud ID Services settings </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>3.</b> Add the Adobe Analytics tool. </p> </td> 
   <td colname="col2"> <p>You can deploy <span class="keyword"> Adobe Analytics </span> (Standard and Premium) using dynamic tag management by creating the <span class="keyword"> Adobe Analytics </span> tool and configuring the page code either automatically or manually. The automatic method is recommended for most users. </p> <p>For more information, see <a href="../tools/analytics_dtm.md#concept_FBA6679A0B79490F8296437F11E5E4F8" format="dita" scope="local"> Add Adobe Analytics Tool </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Add the Nielsen Tool {#section_E656FC0A6CD24EC2AB12130E8E043BE2}

1. Click  **[!UICONTROL  *`Web Property Name`*]** > **[!UICONTROL Overview]** > **[!UICONTROL Add a Tool]** > **[!UICONTROL Nielsen]** .

   ![Step Result](assets/nielsen_tool.png) 

1. Fill in the fields:

<table id="table_1CFB53FE72E74CCB8CAA5D4E3873D286"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Tool Type </p> </td> 
   <td colname="col2"> <p>The type of tool, such as <span class="keyword"> Nielsen </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tool Name </p> </td> 
   <td colname="col2"> <p>A descriptive name for this tool. This name displays on the <span class="wintitle"> Overview </span> tab under <span class="wintitle"> Installed Tools </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Client ID </p> </td> 
   <td colname="col2"> <p>Specify the Client ID you obtained from Nielsen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Collection Server </p> </td> 
   <td colname="col2"> <p>Specify the collection server you obtained from Nielsen (secure-us or secure-au, for example). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="1"> <p>Integration Method </p> </td> 
   <td colname="col2"> <p> <b>Automatic</b>: Use dynamic tag management to manage the integration. </p> <p>After the accounts are connected, dynamic tag management pulls the <span class="keyword"> Adobe Analytics </span> report suite IDs and names into the tool configuration interface, allowing for increased speed in tool deployment with less possibility for user errors. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <b>Manual</b>: Manually manage the integration. </p> <p> <p>Note:  We strongly suggest that you use the Automatic integration method. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Click **[!UICONTROL Create Tool]** to create the tool and display it for editing. 
1. Fill in the fields:

<table id="table_F2635DE3831B4476AD1B12041DB16FBD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Application ID </p> </td> 
   <td colname="col2"> <p>Specify the application's ID that you obtained from Nielsen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Application Name </p> </td> 
   <td colname="col2"> <p>Specify the application's name that you obtained from Nielsen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Collection Server </p> </td> 
   <td colname="col2"> <p>Specify the collection server you obtained from Nielsen (secure-us or secure-au, for example). The collection server carries over from the information you specified above. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Content Group </p> </td> 
   <td colname="col2"> <p>Specify the content group you obtained from Nielsen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>VCID </p> </td> 
   <td colname="col2"> <p>Specify the VCID you obtained from Nielsen. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Click **[!UICONTROL Save Changes]**.

## Set Up Nielsen Rules in Dynamic Tag Management {#section_C3D440E62D4B487BB2D30F06CEC51BA5}

[!DNL Dynamic tag management] is a rule-based system. It looks for user interaction and associated data. When the criteria outlined in your rules are met, the rule triggers the tool, script, or HTML you identified. For general information, see [Rules](../rules/rules.md#concept_2D3F296DD3BD418BAB7A0E2415DD9C92).

When you add the Nielsen tool, dynamic tag management automatically creates a default Nielsen Time Tracking rule.

1. Click the **[!UICONTROL Rules]** tab > **[!UICONTROL Page Load Rules]** > **[!UICONTROL Nielsen]**. 
1. Set up the rules as desired by specifying when this page rule should fire.

    1. Click **[!UICONTROL Conditions]**, then specify where the rule fires (bottom of page, top of page, DOM ready, or onload). 
    1. Specify the criteria for firing the rule. 
    1. Include the path to the pages on which you want the rule to fire (for example, "videos"). 
    1. Click **[!UICONTROL Nielsen]** to see a set of pre-populated data elements.

       ![](assets/nielsen_rules.png) 
    
    1. Click **[!UICONTROL Data Elements]** to map where you want dynamic tag management to pull the information in these pre-populated data elements (Asset Name, Player ID, and so forth).

       For example, Asset Name might be pulled from a DIV to which you need to point.

   The following topics provide in-depth information:

    * [Page Load Rules Example](../rules/rules.md#concept_811F4216145A4E3A91190DFFC9C2D223) 
    * [Rule Conditions and Functions](../rules/rules.md#reference_662A7B7D177C46C98980CD317A7A8861) 
    * [Data Elements](../data_elements.md#concept_8A4591BD0F4241B6925D976482C43CD2)

## Approve and Publish All Changes {#section_9948D02D35FC423FA44101C221265C0B}

You must approve the changes you made in the previous sections before those changes become effective.

1. Click the **[!UICONTROL Approvals]** tab > **[!UICONTROL Approve]**.

