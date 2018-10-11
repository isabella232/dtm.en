---
description: A web property is a library of rules and one embed code. A web property can be any grouping of one or more domains and subdomains. You can manage and track these assets similarly. For example, suppose that you have multiple websites based on one template, and you want to track the same assets on all of them. You can apply one web property to multiple domains.
keywords: dynamic tag management;live;production;staging;switch;test;testing
seo-description: A web property is a library of rules and one embed code. A web property can be any grouping of one or more domains and subdomains. You can manage and track these assets similarly. For example, suppose that you have multiple websites based on one template, and you want to track the same assets on all of them. You can apply one web property to multiple domains.
seo-title: Web Properties
solution: Marketing Cloud,Analytics,Dynamic Tag Management
title: Web Properties
uuid: 966c5857-d4c3-4505-8051-b122546555de
index: y
internal: n
snippet: y
---

# Web Properties

A web property is a library of rules and one embed code. A web property can be any grouping of one or more domains and subdomains. You can manage and track these assets similarly. For example, suppose that you have multiple websites based on one template, and you want to track the same assets on all of them. You can apply one web property to multiple domains.

## Web Properties {#concept_8413810BEAEC4AA48996BE9AFCF141DD}

A web property is a library of rules and one embed code. A web property can be any grouping of one or more domains and subdomains. You can manage and track these assets similarly. For example, suppose that you have multiple websites based on one template, and you want to track the same assets on all of them. You can apply one web property to multiple domains.

<table id="table_945212E5A33F414DB053569EAE2840DC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> DTM Basics: Web Properties </th> 
   <th colname="col2" class="entry"> Time: 6:06 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 
     <div width="550px" class="video-iframe"> 
      <iframe src="https://video.tv.adobe.com/v/17182/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://video.tv.adobe.com/v/17182/</iframe>
     </div> </p> </td> 
   <td colname="col2"> <p>By then end of this video you should be able to: </p> <p> 
     <ul id="ul_6D341D136F5944F98229AD62937310F5"> 
      <li id="li_32CDF16E61EB42BC9A7CC10997ED7AC7">Explain what a web property is </li> 
      <li id="li_A3F245063C0942EE8CBF6580CB9371C0">Set up a web property </li> 
      <li id="li_EC807FD5E7A24B6CA505507AF670DC5F">Understand the web property's relationship with the embed code and report suites </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

This section contains the following information:

* [Best Practices for Planning Web Properties](web_property.md#section_E34FD37B5F2A41D3B40C850A49DE067F) 
* [How Web Properties Compare to Analytics Report Suites](web_property.md#section_0C440F337C614C1A972B3E1EF107C53F) 
* [Separating the DTM Environment for Multiple Entities](web_property.md#section_3F0608BEA6B344D09DE071635017CA3F) 
* [Deactivating a Web Property](web_property.md#section_CE19CAE345CD49668D903626F935E24B)

## Best Practices for Planning Web Properties {#section_E34FD37B5F2A41D3B40C850A49DE067F}

Considering the following when planning web properties: 

<table id="table_E8C2D909CC554F0F85409165A48030E3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Consideration </th> 
   <th colname="col2" class="entry"> Best Practice </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Data </p> </td> 
   <td colname="col2"> <p>For all of your websites, is the data you are going to collect very similar, somewhat similar, or unique? </p> <p>If the data you need to collect is similar across websites, it might make sense to group those sites into one web property to avoid duplicating rules or copying rules from one property to another. </p> <p>If your data collection needs are unique for each site, it might make sense to separate those sites in their own web properties. This method lets you control the data collection more specifically for each site, without using large amounts of conditional logic in custom scripts. </p> <p>For example, if 80 percent of the data you are collecting across your sites is the same, or similar, it makes sense to group those sites together into the same web property. If the data is unique for each site, it makes sense to put each site into its own web property. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Variables </p> </td> 
   <td colname="col2"> <p>Similar to data, for all of your websites, are the variables you are going to set in your <span class="keyword"> Analytics</span> and other tools very similar, somewhat similar, or unique? </p> <p>For example, if eVar27 is used for the same source value across all of your websites, it might make sense to group those sites together so you can set those common variables across your sites in just one web property. </p> <p>If your variable usage is unique for each site, it might make more sense to separate those sites into their own web properties so you can control the variables more specifically for each site without using large amounts of conditional logic in custom scripts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Tools, Tags, and Systems </p> </td> 
   <td colname="col2"> <p>Are the tools, tags and systems you are going to deploy through dynamic tag management very similar, somewhat similar, or unique? </p> <p>If the tools, tags, and systems you are going to deploy through dynamic tag management are very similar across your sites, you might want to include those sites in the same web property. </p> <p>If you are deploying <span class="keyword"> Adobe Analytics</span> on only one site, and your other tools and tags are also unique to certain sites, you might want to create separate web properties for those sites so you can control those specific tools in one web property. </p> <p>For example, If you are deploying Adobe Analytics, Target, and the same 3rd-party tags and tools across your sites, that is a reason to group sites together. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> People </p> </td> 
   <td colname="col2"> <p>For the individuals, teams, and organizations that are working in dynamic tag management, will they need access to all of your websites, some of them, or just one of your domains or sub-domains? </p> <p>The User Management features allow you to assign different roles to different people for all of your web properties, or on a per-property basis. The only role that includes all web properties within a dynamic tag management company account is the Admin role. If someone is an Admin, that person can perform administrative actions across all the web properties in that dynamic tag management company. All the other roles can be assigned on a per-property basis. You can even hide a web property from certain users (non-admins) by not giving them any role in that web property. </p> </td> 
  </tr> 
 </tbody> 
</table>

Each implementation can be very different in dynamic tag management, with a wide variety of data-collection needs, variable usage, tools, third-party tags, other systems and technologies, people, teams, geographic regions, and so on. Using the flexible User Management features and web properties, you can create a configuration that matches your workflow and processes.

If the scenarios you are tracking, the data you are collecting, the tools you are deploying, and the variables you are setting are similar across all or some of your domains and subdomains, it is easier to have those domains and subdomains grouped into the same web property in dynamic tag management. If those are unique for each domain and subdomain, it is easier to have those domains and subdomains in their own web property. If you choose to group domains and subdomains in a single property now, you can always change your mind and later create several web properties.

## How Web Properties Compare to Analytics Report Suites {#section_0C440F337C614C1A972B3E1EF107C53F}

In [!DNL Adobe Analytics], you can dynamically determine the report suite to which you want to send the data, if you are not tracking all the websites in one suite of reports.

A web property can contain any number of domains or subdomains. It can also send analytics data to one or several report suites in [!DNL Analytics]. You can set multi-suite tagging, or you can use conditional logic that sets *`s.account`* according to your particular needs.

If you want to send data to two report suites for every page view and event, you would add a comma-separated list of report suite IDs in the user interface in dynamic tag management, in the Account Numbers fields, on the Adobe [!DNL Analytics] Global Settings page.

If you want to send data to a particular report suite based on conditional logic, you would add your logic in the Editor, in the [!UICONTROL General] section of the Adobe [!DNL Analytics] Global Settings page.

## Separating the DTM Environment for Multiple Entities {#section_3F0608BEA6B344D09DE071635017CA3F}

There are a few ways to handle multiple geo markets, business units, domains, and subdomains in dynamic tag management.

First, you can have one or several dynamic tag management Company accounts. Companies contain web properties. You can have one or several or any number of web properties within a Company account. Within a web property, you can have one or any number of domains or subdomains.

Some customers have one Company that contains all of their web properties. Some have a Company that contains many web properties, one for each domain. Some have a Company that contains several web properties, one for each type of site they manage.

For example, you might have three web properties within your Company account where one contains all of your blog sites, another contains all of your ecommerce sites, and the third contains all of your lead-generation sites.

>[!NOTE]
>
>Each web property requires its own Embed Codes in your page templates. Any domains or subdomains you want included in a particular web property would have the same Embed Codes in the page templates when dynamic tag management is first installed on your site.

**Can we use separate instances for each?**

As described above, you can use separate Company accounts for your three entities, or you can combine the entities into one Company account and split the domains / subdomains into different web properties within that Company account.

**Is there a clear way to separate domains and settings within the same dynamic tag management instance?**

Within a Company account, you can use multiple web properties to separate domains and settings, or you can put multiple domains into the same web property.

**What are the pros and cons for using one dynamic tag management instance?**

With one web property that contains multiple domains and subdomains, you will eventually add conditional logic to separate unique data collection and tracking needs that only apply to individual domains, subdomains, or subsets of domains / subdomains.

**What is the approach recommended by Adobe: one or separate companies?**

Most clients use one Company account that contains all of their web properties. Information on this page can help you determine the best plan for your particular needs within those properties.

## Deactivating a Web Property {#section_CE19CAE345CD49668D903626F935E24B}

Deactivating a web property does not deactivate everything within the property, it just prevents the associated library files from getting rebuilt (i.e. the staging and production libraries remain in the state they were in when the property was deactivated).

If you deactivate a property and expect a tool or rule to stop firing, you should deactivate those item(s) in the property and then publish that change, if applicable, before deactivating the property.

If the property is already deactivated, you might need to reactivate the property, inactivate the desired items, publish (if applicable), and then deactivate the property again. 

## Create a web property {#task_AE34E23EC47B4E9C8634782C05D9DC09}

Create a web property in dynamic tag management. 

<!-- 

t_create_web_property.xml

 -->

>[!NOTE]
>
>Only a user with Admin rights can create a property. For more information about roles, see [Create and Manage Groups in DTM](groups.md#concept_6494F1EF2400457ABCED8D860951CD36).

Before beginning, review the [Best Practices](web_property.md#section_E34FD37B5F2A41D3B40C850A49DE067F) for web properties. 

1. Navigate to your company page, then click **[!UICONTROL Add Property]**.

   ![](assets/create_web_property.png) 
1. Fill in the fields:

<table id="table_376D72251C4D4C4CA878D10C18D2532C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="uicontrol"> Name</span> </td> 
   <td colname="col2"> <p>The name of your property. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="uicontrol"> URL</span> </td> 
   <td colname="col2"> <p>The base URL of the property. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="uicontrol"> This site spans multiple domains </span> </td> 
   <td colname="col2"> <p>You can add and remove domains if you want visitor data to persist between domains. </p> <p>This setting lets you specify how you would like to track traffic moving between your associated <a href="web_property.md#concept_8413810BEAEC4AA48996BE9AFCF141DD" format="dita" scope="local"> subdomains or domains</a>. </p> <p> <p>Note:  If you do not intend to integrate an analytics tool, this step is unnecessary and does not affect processing. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

1. (Optional) Configure [!UICONTROL Advanced Settings].

<table id="table_6E687FBE6ACC4301BCCD837F4DCBB9C9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="uicontrol"> Allow Multi-Rule Approvals</span> </td> 
   <td colname="col2"> <p>Allows multiple rules for this property to be approved at one time. (The default approval allows only single-rule approval.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="uicontrol"> Enable Selective Publish</span> </td> 
   <td colname="col2"> <p>Specifies whether to allow users to selectively publish approved rules. (This is the default option.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="uicontrol"> Tracking Cookie Name</span> </td> 
   <td colname="col2"> <p>Overrides the default tracking cookie name. You can customize the name that dynamic tag management uses to track your opt-out status for receiving other cookies. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="uicontrol"> Tag Timeout</span> </td> 
   <td colname="col2"> <p>Specifies how long dynamic tag management waits for a tag to fire before timing out. </p> <p> Because of how dynamic tag management works, don't worry about this being a high number, as we have other, better methods of ensuring that slow tags do not affect the user experience. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="uicontrol"> Anchor Delay</span> </td> 
   <td colname="col2"> <p>Specifies how long dynamic tag management waits for tags to fire on clicked links before moving to the next page. The default value is 100 milliseconds. </p> <p>Longer delays improve tracking accuracy. Adobe recommends a delay of 500 milliseconds or less, which the user will not perceive. </p> <p>Dynamic Tag Management will wait up to the time specified, but if the beacon fires sooner, the delay is cut short. (That is, user won't always wait the full length of the delay.) </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Click **[!UICONTROL Create Property]**.

## Delete a web property {#task_98FAD87F2E574E54B2705CDE6C804695}

Delete a web property from dynamic tag management. 

<!-- 

t_delete_web_property.xml

 -->

>[!NOTE]
>
>Property removal cannot be reversed. The requestor must be an admin-level user. This request cannot be undone.

1. Navigate to the [!UICONTROL Overview] page for the desired property.

   ![](assets/remove_property.png) 
1. Click **[!UICONTROL Edit Property]** > **[!UICONTROL Remove Property]**, then confirm the removal of the property.

   ![Step Result](assets/remove_property_2.png) 