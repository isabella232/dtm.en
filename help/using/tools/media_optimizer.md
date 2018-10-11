---
description: Information about deploying Adobe Media Optimizer using dynamic tag management.
keywords: dynamic tag management;Experience Cloud ID service;visitor ID
seo-description: Information about deploying Adobe Media Optimizer using dynamic tag management.
seo-title: Adobe Media Optimizer Tool
solution: Marketing Cloud,Analytics,Target,Dynamic Tag Management
title: Adobe Media Optimizer Tool
uuid: 3911902e-d481-4f83-b799-c23a3950774c
index: y
internal: n
snippet: y
---

# Adobe Media Optimizer Tool

Information about deploying Adobe Media Optimizer using dynamic tag management.

## Adobe Media Optimizer Tool {#concept_1A33BC0F5B6A4709929EC6F876236657}

Information about deploying Adobe Media Optimizer using dynamic tag management. 

**[!UICONTROL <Web Property Name>]** > **[!UICONTROL Overview]** > **[!UICONTROL Add a Tool]** > **[!UICONTROL Adobe Media Optimizer]**

<!-- 

<p>Values are applied to every rule using this Tool. Getting new content from Anna, she'll route to Greg/Cory then me. </p>

 -->

<table id="table_1484B14A786A43CCA8A000B8249B28FF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Setting </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Tool Name </td> 
   <td colname="col2"> <p>A descriptive name for this implementation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> User ID </td> 
   <td colname="col2"> <p>Your advertising management account has an associated numeric user ID. It is displayed in the JavaScript generated for a pixel. </p> <p>For example: </p> 
    <codeblock>
      1234
    </codeblock> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Transaction ID </td> 
   <td colname="col2"> <p> Indicate a transaction ID property (ev_transid=<span class="term"> &lt;transid&gt;</span>) to include in the tag. When you include the ID, the advertiser must generate a unique value for &lt;<span class="term"> transid</span>&gt; (for example, an actual order ID) when the transaction is complete. The value is passed back to advertising management. Advertising management uses the transaction ID to eliminate duplicate transactions with the same transaction ID and property value. </p> <p> The transaction ID is included in the Transaction Report in advertising management, which you can use to validate advertising management data with the advertiser's data. </p> <p> If the advertiser's data does not include a unique ID per transaction, Media Optimizer still generates one, based on transaction time. </p> <p> The transaction ID cannot contain ampersand symbols (&amp;), which are reserved as parameter separators. </p> <p>Note:  If you use the <span class="keyword"> Media Optimizer</span> combo tracking service, you must submit the transaction ID (<span class="varname"> ev_transid</span>) for the online part of the transaction in the feed data for offline parts of the transaction. <p>For more information, see the Tracking section of the advertising management online help. </p> </p> <p> <span class="term"> Transaction ID</span> can be set globally at the tool level or conditionally at the rule level. A globally configured transaction ID is inherited by any dynamic tag management rules utilizing the Adobe Media Optimizer tool, unless specifically overridden in the rule. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Load Media Optimizer page code at (Page Top or Page Bottom) </td> 
   <td colname="col2"> <p>Determines where and when the page code loads. The recommended location is selected by default. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Media Optimizer page code already present </td> 
   <td colname="col2"> <p>Prevents dynamic tag management from installing advertising management code if the code exists on your site. This method lets you use dynamic tag management to add to your existing advertising management implementation, rather than starting a new implementation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Conversion Property Name / Value </p> </td> 
   <td colname="col2"> <p> A conversion property to be tracked when an end user views a page containing the conversion tag. </p> <p> <p>Note:  Properties added to this list are not integrated with the client's Transaction Properties list in the Admin view in advertising management. However, properties are added to the client's Transaction Properties list automatically, once advertising management actually gathers data for a property. Gathering happens when the conversion tag is implemented on a page and an end user completes a transaction that opens that page. </p> </p> <p> Conversion properties can be set globally at the tool level and conditionally at the rule level. A globally configured Conversion Property is inherited by any dynamic tag management rules utilizing the Adobe Media Optimizer tool <span class="term"> in addition</span> to any conversion properties set in the rule. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Segment ID (Optional) </p> </td> 
   <td colname="col2"> <p>Indicate the numeric ID for an advertising management segment in which to add the users who complete the tracked transaction. (For JavaScript tags and for display campaigns only) </p> <p> <p>Note:  If you associate multiple conversion tags with the same audience segment, the segment will include all of the users who complete those transaction types. </p> </p> <p> Segment ID can be set globally at the tool level or conditionally at the rule level. A globally configured Segment ID is inherited by any dynamic tag management rules utilizing the Adobe Media Optimizer tool, unless specifically overridden in the rule. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tag Property / Value </p> </td> 
   <td colname="col2"> <p> A conversion property name / value to be included in the tag when the specific rule is fired. </p> <p> <p>Note:  Properties added to this list are not integrated with the client's Transaction Properties list in the Admin view in advertising management. However, properties are added to the client's Transaction Properties list automatically, once advertising management gathers data for a property. Gathering happens when the conversion tag is implemented on a page and an end user completes a transaction. </p> </p> <p> Conversion properties can be set globally at the tool level and conditionally at the rule level. If a rule uses the Adobe Media Optimizer tool, the configured global value is inherited and used <span class="term"> in addition</span> to any conversion properties configured in the rule. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SKU </p> </td> 
   <td colname="col2"> <p> Select the configured data element to populate the SKU value in the tag. </p> <p> See <a href="../data_elements.md#concept_8A4591BD0F4241B6925D976482C43CD2" format="dita" scope="local"> Data Elements</a> for more information. </p> <p> SKU can be set globally at the tool level or conditionally at the rule level. If a rule uses the Adobe Media Optimizer tool and the rule does not specifically set a SKU, the configured global value is inherited and used. If the rule sets a SKU, any global SKU configuration is overridden in that rule. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Media Optimizer Rule Example {#task_FC14320055254A30BD7F71FA6E905216}

An example of how to enable Adobe Media Optimizer in dynamic tag management for a specific rule when an Adobe Media Optimizer tool is installed. 

<!-- 

t_media_opt_rule.xml

 -->

In this example, when this rule fires, Adobe Media Optimizer loads and fires a tag including the SKU value for the data element *`ecomm_prodid`* instead of the SKU configured at the tool level. The tag also includes any Transaction ID, Segment ID, and Conversion tags configured globally in the installed Adobe Media Optimizer tool. 

1. Click **[!UICONTROL Property]** > **[!UICONTROL Rules]** > **[!UICONTROL Event Based Rules]** > **[!UICONTROL Create New Rule]**.
1. Name and configure the rule condition.

   ![Step Result](assets/rule_media_opt_01.png)

   Configure the rule so that it fires only in the desired cases. In this example, the rule fires on the click of *`Add to cart`* as indicated by the selector *`div`* with a class of *`addtocart`*.

   >[!NOTE]
   >
   >Adobe Media Optimizer is also available in page load and direct call rules in dynamic tag management once an Adobe Media Optimizer tool is installed in the property. See [Conditions and Functions](../rules/rules.md#section_198A5095854F415C86ABBA9165D53370) for information about available rule criteria.

1. Expand **[!UICONTROL Adobe Media Optimizer]** in the rule.

   ![Step Result](assets/rule_media_opt_02.png) 
1. Enable **[!UICONTROL Load Adobe Media Optimizer for this rule]**.
1. Configure the settings you want to apply in this rule.

   All of the settings are optional, because global configurations from the installed Adobe Media Optimizer tool are inherited. 

