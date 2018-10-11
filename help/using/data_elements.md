---
description: Data elements are the building blocks for rules. Data elements let you create a data dictionary (or data map) of commonly used items on a page, regardless of where they originate (query strings, URLs, or cookie values) for any object that is contained on your site. You use data elements to build a data layer that can be used for Analytics and other data collection tools.
keywords: dynamic tag management
seo-description: Data elements are the building blocks for rules. Data elements let you create a data dictionary (or data map) of commonly used items on a page, regardless of where they originate (query strings, URLs, or cookie values) for any object that is contained on your site. You use data elements to build a data layer that can be used for Analytics and other data collection tools.
seo-title: Data Elements
solution: Marketing Cloud,Analytics,Target,Dynamic Tag Management
title: Data Elements
uuid: 6c2bcc83-ebd8-4d0c-9161-f07d55e0fcde
index: y
internal: n
snippet: y
---

# Data Elements

Data elements are the building blocks for rules. Data elements let you create a data dictionary (or data map) of commonly used items on a page, regardless of where they originate (query strings, URLs, or cookie values) for any object that is contained on your site. You use data elements to build a data layer that can be used for Analytics and other data collection tools.

## Data Elements {#concept_8A4591BD0F4241B6925D976482C43CD2}

Data elements are the building blocks for rules. Data elements let you create a data dictionary (or data map) of commonly used items on a page, regardless of where they originate (query strings, URLs, or cookie values) for any object that is contained on your site. You use data elements to build a data layer that can be used for Analytics and other data collection tools. 

**[!UICONTROL Rules]** > **[!UICONTROL Data Elements]** > **[!UICONTROL Edit]** .

Use data elements as widely as possible throughout rule creation to consolidate the definition of dynamic data and to improve the efficiency of your tagging process. You define data rules once and then use them many times.

The concept of reusable data elements is very powerful and you should use them as best practice.

For example, if there is a particular way that you reference page names or product IDs, or grab information from query string parameters from an affiliate marketing link or from AdWords, and so forth, you can create a data dictionary (data elements) by getting information from various sources and then using this data in various dynamic tag management rules.

Using page name as an example, suppose you use a particular page-name schema by referencing a data layer, `document.title` element, or a title tag within the website. In dynamic tag management, you can create a data element as a single point of reference for that particular point of data. You can then use this data element in any rule that needs to reference the page name. If for some reason in the future you decide to change the way you reference page name (for example, you have been referencing `document.title` but you now want to reference a particular data layer), you don't need to edit many different rules to change that reference. You simply change the reference once in the data element and all rules that reference that data element automatically update.

Data elements are populated with data when they are used in rules or when manually calling in scripts. At a high level, you:

1. [Create a data element](data_elements.md#task_962EF08CE2AE49B3B739295F6E4792C2), if you haven't done so already. 
1. Use the data element in a [rule](rules/rules.md#concept_2D3F296DD3BD418BAB7A0E2415DD9C92) or a custom script.

This section contains the following information:

* [Types of Data Elements](data_elements.md#section_92407DCB477045D3B50DF8105AB2E6F4) 
* [Persistence](data_elements.md#section_7F9C583A49874ACC9E14F0644B1E5783) 
* [Built-In Data Elements](data_elements.md#section_D75D9250EB3F4563BDB22D38B1C071AA) 
* [Data Element Usage](data_elements.md#section_2CD92AAA2B7C462EBFDA562AED299E6A) 
* [Data Element Availability](data_elements.md#section_43A5C65D7C5E4E23B2C1186090C2D5B2) 
* [How to Collect Values from JavaScript Variables](data_elements.md#section_EFA406CC945B4DF5ACEE157CD99D2D29)

## Types of Data Elements {#section_92407DCB477045D3B50DF8105AB2E6F4}

The following table describes the types of data elements. 

<table id="table_FCEF0808C3BD4D178284DB9918D0CB57"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type </th> 
   <th colname="col2" class="entry"> Description </th> 
   <th colname="col3" class="entry"> Example </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>JavaScript Object </p> </td> 
   <td colname="col2"> <p>Any available JavaScript object or variable can be referenced using the <span class="term"> path </span> field. </p> </td> 
   <td colname="col3"> <p> <span class="filepath"> window.document.title </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>CSS Selector </p> </td> 
   <td colname="col2"> <p>Any element value can be retrieved, such as a div or H1 tag. </p> </td> 
   <td colname="col3"> <p>CSS Selector Chain: </p> <p> <span class="codeph"> id#dc logo img </span> </p> <p>Get the value of: </p> <p> <span class="codeph"> src </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookie </p> </td> 
   <td colname="col2"> <p>Any available domain cookie can be referenced in the <span class="term"> cookie name </span> field. </p> </td> 
   <td colname="col3"> <span class="filepath"> cookieName </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>URL Parameter </p> </td> 
   <td colname="col2"> <p>Specify a single URL parameter in the <span class="term"> URL Parameter </span> field. </p> <p>Only the name section is necessary and any special designators like "?" or "=" should be omitted </p> </td> 
   <td colname="col3"> <p> <span class="filepath"> contentType </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Custom Script </p> </td> 
   <td colname="col2"> <p>Custom JavaScript can be entered into the UI by clicking <span class="uicontrol"> Open Editor </span> and inserting code into the editor window. </p> <p>A return statement is necessary in the editor window in order to indicate what value should be set as the data element value. If a return statement is not included, the default value or an empty string will be returned as the data element value. </p> </td> 
   <td colname="col3"> 
    <codeblock>
      var&nbsp;pageType&nbsp;=&nbsp;$('div.page-wrapper').attr('class').split(' 
     
')[1]; 
     
if&nbsp; 
     
(window.location.pathname&nbsp;==&nbsp;'/'){return&nbsp;'homepage';&nbsp; 
     
} 
     
else 
     
{ 
     
return&nbsp;pageType; 
     
&nbsp;} 
    </codeblock> </td> 
  </tr> 
 </tbody> 
</table>

## Persistence {#section_7F9C583A49874ACC9E14F0644B1E5783}

<table id="table_74FAF529CC6F41C0B944F50C2C4716F9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Page view </p> </td> 
   <td colname="col2"> 
    <ul id="ul_2B0DD0154E934D738682C1A4C17962B3"> 
     <li id="li_F55EA309E47C4BEEA1A6A274F7BA1A26">Available only while the page persists. </li> 
     <li id="li_121F039474A540BC821B00103055D0A1">Can be created and set in scripts using <span class="varname"> _satellite </span> object syntax: <p> <span class="codeph"> _satellite.setVar('data_element_name') </span> </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Session </p> </td> 
   <td colname="col2"> 
    <ul id="ul_36A30A88AE544AA1BC75CF3F7C40E7A1"> 
     <li id="li_4BE70E7A60E04C668DAF48D7C6D1DEF2"> Sets a session-level cookie in the browser. </li> 
     <li id="li_87F026FC3FC34FA0BCB12FA1F5CFC7E8"> Available throughout the site visit. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Visitor </p> </td> 
   <td colname="col2"> 
    <ul id="ul_D71DD611FE6D49429792DD0DBFAC2073"> 
     <li id="li_330A9F4DBD3E47969AB2F3721BA88AF1"> Sets a 2-year cookie. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookie manipulation </p> </td> 
   <td colname="col2"> <p>Can be manipulated using _satellite cookie methods: </p> 
    <ul id="ul_4521AD79AB004BC6B563C8A6E9B6BA25"> 
     <li id="li_98ABEFEE2B6D4812919CE27486308E29"> <span class="codeph"> _satellite.setCookie(name,value,days); </span> </li> 
     <li id="li_CF8FB0DC7DCA4B94A004F4A18CFF7ED8"> <span class="codeph"> _satellite.readCookie(name); </span> </li> 
     <li id="li_E0C9783616A34852974ED26FDEC43A18"> <span class="codeph"> _satellite.removeCookie(name); </span> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Built-In Data Elements {#section_D75D9250EB3F4563BDB22D38B1C071AA}

<table id="table_3AF3D1A8B7364D3692606DCD77CBEA0A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>URI </p> </td> 
   <td colname="col2"> 
    <ul id="ul_8A3E0EFC09AB44F8B4C03B0EBFDAA957"> 
     <li id="li_013F21D65CCF4D15B681D9107AB38BB7"> Used in rule: <span class="codeph"> %URI% </span> </li> 
     <li id="li_AE7E766797F040B7B08F2D3B4A6F9597"> Returns <span class="codeph"> document.location.pathname </span> + <span class="codeph"> document.location.search </span> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Protocol </p> </td> 
   <td colname="col2"> 
    <ul id="ul_5BEDE329D3FD4B5D98A5295F8EA7BEB0"> 
     <li id="li_8EE7F15977DF444DBC5D643CFC0C8194"> Used in rule: <span class="codeph"> %protocol% </span> </li> 
     <li id="li_50E944A4E6CB44A991DF8B2640D5D0E7"> Returns <span class="codeph"> document.location.protocol </span> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Hostname </p> </td> 
   <td colname="col2"> 
    <ul id="ul_7FC8E8957874450D9A254A15EDE43E90"> 
     <li id="li_FE9065FD5E5C4BA88FA1F010E98080AC"> Used in rule: <span class="codeph"> %hostname% </span> </li> 
     <li id="li_5A3C58CEF5F643CAA3DAECCA87CC62F0"> Returns <span class="codeph"> document.location.hostname </span> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Data Element Usage {#section_2CD92AAA2B7C462EBFDA562AED299E6A}

<p class="head"> <b>In Rules</b> </p>

You can use data elements in the rule editing interface by using the percent sign (%) syntax. Type a percent sign into the field and you will see a drop-down menu appear with the data elements that you created.

![](assets/rule_condition_data_availability.png) 

<p class="head"> <b>In Custom Script</b> </p>

You can use data elements in custom scripts by using the `_satellite` object syntax:

`_satellite.getVar('data element name');`

## Data Element Availability {#section_43A5C65D7C5E4E23B2C1186090C2D5B2}

If a data element is not referenced in a rule, it is not loaded on any page unless specifically called in custom script 

<p class="head"> <b>Forcing Data Element Retrieval through Custom Identifiers</b> </p>

Data elements can be set in the custom code section of a rule identifier to guarantee that the data element is available for the rule. This situation is sometimes necessary for specific timing considerations and issues with existing implementation code.

![](assets/custom.png)

For example, entering the following code forces the retrieval of the data element named *`sample data`* during the rule identification step, prior to any data manipulation that happens in the rest of the rule.

![](assets/rule_conditions.png)

The custom code section in the identifier must return *`true`*, regardless of whether a valid value is available for the data element. Otherwise, the rule never evaluates as *`true`* or runs.

## How to Collect Values from JavaScript Variables {#section_EFA406CC945B4DF5ACEE157CD99D2D29}

When you have JavaScript variables, or object properties in your markup, and you want to collect those values in dynamic tag management to use with your analytics tools, or testing tools, or even with third party tags, one way to capture those values is to use Data Elements in dynamic tag management. This way, you can refer to the Data Element throughout your Rules, and if the source of the data ever changes, you only need to change your reference to the source (the Data Element) in one place in dynamic tag management.

For example, let's say your markup contains a JavaScript variable called "Page_Name", like this:

```
<script> 
    //data layer 
    var Page_Name = "Homepage" 
  </script> 

```

When you create the Data Element in dynamic tag management, simply provide the path to that variable like this:

![](assets/faq_data_element.png)

If you use a data collector object as party of your data layer, simply use dot notation in the Path to reference the object and property you want to capture into the Data Element, like `_myData.pageName`, or `digitalData.pageName`, etc.

## Adobe Training Video: Data Elements {#section_3D594CC791AD48E3AE64CB90E7263AC9}

<table id="table_0C277DDB4FD04C17B5279FC98B160326"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> DTM Basics: Data Elements </th> 
   <th colname="col2" class="entry"> Time: 10:28 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 
     <div width="550px" class="video-iframe"> 
      <iframe src="https://video.tv.adobe.com/v/17168/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://video.tv.adobe.com/v/17168/</iframe>
     </div> </p> </td> 
   <td colname="col2"> <p>By then end of this video you should be able to: </p> <p> 
     <ul id="ul_EB6B76A11FDF496BB151686E6E9F5215"> 
      <li id="li_6C7B79D472FB4748867797C3B275A66B">Understand what a data element is </li> 
      <li id="li_A3E2F85924074FF3A676CEF718A14875">Explain the different element types </li> 
      <li id="li_509195A741CA454F83015CCA679832C8">Create a data element </li> 
      <li id="li_8505D652EA3C4905AF960261C4A436D3">Use a data element in a rule </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Create a data element {#task_962EF08CE2AE49B3B739295F6E4792C2}

Create a data element in dynamic tag management. 

<!-- 

t_data_element.xml

 -->

1. [Create a web property](web_property.md#task_AE34E23EC47B4E9C8634782C05D9DC09).
1. In the web property, click  **[!UICONTROL Rules]** > **[!UICONTROL Data Elements]** .
1. Click **[!UICONTROL Create New Data Element]**.
1. Complete the following fields and options:

    <table id="choicetable_681F7D5B86534FF0B6DB67E117B8E381"> 
 <thead class="chhead sthead"> 
  <th class="choptionhd"> Option </th> 
  <th class="chdeschd"> Description </th> 
 </thead> 
 <tr class="chrow strow"> 
  <td class="choption"><strong>Name</strong></td> 
  <td class="chdesc stentry"> <p>The data element friendly name that a marketer can recognize. For example, 
    <userinput>
      Product ID 
    </userinput>. </p> <p> <p>Note:  The name is referenced by the rules builder, not an ID. If you change the name of the Data Element , you must change its reference in every rule that uses it. </p> </p> </td> 
 </tr> 
 <tr class="chrow strow"> 
  <td class="choption"><strong>Type</strong></td> 
  <td class="chdesc stentry"> <p> Specifies where the data is pulled from, such as JS Object, CSS Selector, Cookie, URL Parameter, or Custom Script. </p> <p>Depending on which type you select, different options display. See <a href="data_elements.md#section_92407DCB477045D3B50DF8105AB2E6F4" format="dita" scope="local"> Types of Data Elements </a> for more information and examples. </p> </td> 
 </tr> 
 <tr class="chrow strow"> 
  <td class="choption"><strong>Default Value</strong></td> 
  <td class="chdesc stentry"> <p>A default element. This value ensures that the data element always has a value, even if a URL parameter does not exist or cannot be found by dynamic tag management. </p> <p> <p>Note:  If there is no value and no default value, then nothing is returned. Any variable referencing that data element won't get set. Note also that the default value field is ignored if it's a "custom code" data element. </p> </p> </td> 
 </tr> 
 <tr class="chrow strow"> 
  <td class="choption"><strong>Force lowercase value</strong></td> 
  <td class="chdesc stentry"> <p>Dynamic tag management automatically makes the value lowercased. </p> </td> 
 </tr> 
 <tr class="chrow strow"> 
  <td class="choption"><strong>Remember this value for</strong></td> 
  <td class="chdesc stentry"> <p>How long you want dynamic tag management to remember this value. </p> <p> Valid values include: </p> 
   <ul id="ul_52F6CD8FC22942208F3F45492E914104"> 
    <li id="li_32E4366C5B2E46D788CD8478620FE3E0"> <p>Session: Session-based timing can vary depending on the implementation. Session data elements are set to the session cookie. However, this setting could be based on a web server or the browser. It is not related to the session used in marketing reports &amp; analytics. </p> </li> 
    <li id="li_8A944564BF7643E4B21F0EF2394B3FE8"> <p>Pageview </p> </li> 
    <li id="li_5C8A2F2392FD475AA89DDA7D5B5CF88B"> <p>Visitor </p> </li> 
   </ul> </td> 
 </tr> 
</table>

   See [Data Elements](data_elements.md#concept_8A4591BD0F4241B6925D976482C43CD2) for more information about how to use data elements.
1. Click **[!UICONTROL Save Data Element]**.
