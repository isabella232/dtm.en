---
description: Information about creating the Adobe Target tool for deploying Adobe Target in dynamic tag management. You can configure the library automatically (recommended) or manually.
keywords: dynamic tag management
seo-description: Information about creating the Adobe Target tool for deploying Adobe Target in dynamic tag management. You can configure the library automatically (recommended) or manually.
seo-title: Adobe Target Tool
solution: Marketing Cloud,Target,Dynamic Tag Management
title: Adobe Target Tool
uuid: 555a61e8-ca82-4c71-bc6e-7802310c445a
index: y
internal: n
snippet: y
---

# Adobe Target Tool

Information about creating the Adobe Target tool for deploying Adobe Target in dynamic tag management. You can configure the library automatically (recommended) or manually.

## Adobe Target Tool {#concept_90D4021A9B6E409D8101FA1AFADE1215}

Information about creating the Adobe Target tool for deploying Adobe Target in dynamic tag management. You can configure the library automatically (recommended) or manually.

>[!NOTE]
>
>For best practices, see [Best Practices for Implementing Adobe Target Using Dynamic Tag Management](https://marketing.adobe.com/resources/help/en_US/target/dtm/).

**[!UICONTROL <Web Property Name>]** > **[!UICONTROL Overview]** > **[!UICONTROL Add a Tool]** > **[!UICONTROL Adobe Target]**

![](assets/target_tool.png)

## Field Descriptions - Add a Tool (Adobe Target) {#section_957AFF495DC04E548D0084C0F3063DBF}

The following table describes the fields and options on the [!UICONTROL Add a Tool] page (and the tool edit page) for [!DNL Adobe Target]. This table provides information for the automatic and manual configuration settings. 

<table id="table_CA5DF97568E64EDEACC0859DA5CA7D7F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Setting </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Tool Type </p> </td> 
   <td colname="col2"> <p> The type of tool, such as <span class="keyword"> Adobe Target</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tool Name </p> </td> 
   <td colname="col2"> <p> The name for this tool. This name displays on the <span class="wintitle"> Overview</span> tab under <span class="wintitle"> Installed Tools</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Library retrieval method </p> </td> 
   <td colname="col2"> <p> Specifies whether Adobe should manage your <span class="keyword"> Adobe Target</span> code automatically, or whether you would like to provide your own custom code manually. </p> <p> <b> Manual Configuration Method</b> </p> <p>You can manually manage the <span class="keyword"> Adobe Target</span> code. You can download the <span class="filepath"> at.js</span> or <span class="filepath"> mbox.js</span> file from the Target solution interface as follows: </p> 
    <ul id="ul_CD6362924F5F486B8036B4A1F3E731AC"> 
     <li id="li_261F495AF88041E9A48F99A8BF74FFCD">Target Standard: <span class="uicontrol"> Setup</span> &gt; <span class="uicontrol"> Implementation</span> &gt; <span class="uicontrol"> Download at.js</span> </li> 
     <li id="li_E1D96647B04844909C61806D9BCDAD27">Target Standard: <span class="uicontrol"> Setup</span> &gt; <span class="uicontrol"> Implementation</span> &gt; <span class="uicontrol"> Download mbox.js</span> </li> 
     <li id="li_68A9E7B987A348BA9E11D8415BFD7CE6">Target Classic: <span class="uicontrol"> Configuration-</span> &gt; <span class="uicontrol"> mbox.js</span> &gt; <span class="uicontrol"> Download</span> </li> 
    </ul> <p> After you download the code locally, copy and paste the code into the editor field in the Library Management section of the tool settings. You also have the option of hosting the code at a specific URL as an alternative to manually pasting in the code. </p> <p> <b>Automatic Configuration Method</b> </p> <p> <p>Note:  This works for mbox.js only. </p> </p> <p> Dynamic tag management automatically retrieves the latest <span class="filepath"> mbox.js</span> code from your <span class="keyword"> Adobe Target</span> account configuration. If you select <span class="uicontrol"> Automatic</span>, you must either be logged in via the Experience Cloud, or you must provide a Client Code value described below. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Client code retrieval method </p> </td> 
   <td colname="col2"> <p>(Automatic method) A code unique to your <span class="keyword"> Adobe Target</span> account. It is required for your code to be provided and managed automatically by Adobe. If you chose the Automatic method, you must either be logged in via the Experience Cloud, or provide your Client Code value after selecting <span class="uicontrol"> Manual</span> as the retrieval method. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Client Code </p> </td> 
   <td colname="col2"> <p> (Automatic method) The Client Code value can be retrieved from the <span class="keyword"> Adobe Target</span> solution interface as follows: </p> 
    <ul id="ul_1744D4D51DFE44158C5AC5A77FF5198C"> 
     <li id="li_D9CE4F3E201241BABA81D3C527D5CB77">Target Classic: <span class="uicontrol"> Configuration</span> &gt; <span class="uicontrol"> mbox.js</span> &gt; <span class="uicontrol"> Edit</span> &gt; <i>copy value for Client</i>. </li> 
     <li id="li_AA670B39F39446A282FD684F83340735">Target Standard: <span class="uicontrol"> Setup</span> &gt; <span class="uicontrol"> Implementation</span> &gt; <span class="uicontrol"> Download mbox.js</span> &gt; <i>copy value for Client from within mbox.js file</i>. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Library Management - Adobe Target {#concept_DD6234BB44134EE88F7CD67191366CBC}

Descriptions of the fields and options in the Adobe Target Library Management settings in dynamic tag management. 

<!-- 

target_library_management.xml

 -->

<!-- 

<p>TAGS for ditamap </p>

 -->

**[!UICONTROL Property]** > **[!UICONTROL   ![](assets/settings_gear.png) Edit Tool]** > **[!UICONTROL Library Management]**

![](assets/target_library.png) 

<table id="table_12095D9D6F124374B921573FFFFC5987"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Load Adobe Target Library synchronously </p> </td> 
   <td colname="col2"> <p> This option ensures the <span class="filepath"> at.js</span> or <span class="filepath"> mbox.js</span> code is loaded synchronously in the <span class="codeph"> &lt;head&gt;</span> section. It is generally recommended that you leave this option enabled. It is an <span class="keyword"> Adobe Target</span> best practice to load the code in this way. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Code Configuration </p> </td> 
   <td colname="col2"> <p> <b> Managed by Adobe:</b>(mbox.js only) This option is equivalent to the Automatic configuration method available when creating the tool. This option loads the <span class="filepath"> mbox.js</span> code directly from Adobe. </p> <p>This feature optimizes the configuration process when using a manual method, because no more copying or pasting from the <span class="keyword"> Adobe Target</span> admin console is required. </p> 
    <ul id="ul_54AC746FFAB145909B0B034D41454497"> 
     <li id="li_8F8C980369E64412B8921B06FC39657E">You must be logged in via Experience Cloud or have provided the appropriate <a href="../tools/target.md#section_957AFF495DC04E548D0084C0F3063DBF" format="dita" scope="local"> Client Code</a> for this option to be available. </li> 
     <li id="li_1B2263F4D63741E38223C2C04F9526D4">Clicking <span class="uicontrol"> Check for Updates</span> automatically checks for new versions of the <span class="filepath"> mbox.js</span> code within your associated <span class="keyword"> Adobe Target</span> account. If a new version is identified, you have the option to use it or retain the current version. </li> 
    </ul> <p> <b> Custom:</b> You can manually configure the<span class="filepath"> at.js</span> or <span class="filepath"> mbox.js</span> code. Two methods are available to manually host the code in dynamic tag management: </p> 
    <ul id="ul_FF7CA4BE72484558AFECD8B85868C7F3"> 
     <li id="li_40115E76F6D54640B12D9200458957EA"> <b>In DTM:</b> Click <span class="uicontrol"> Edit Code</span> and paste the code in the editor. If you were using <span class="term"> Managed by Adobe</span> and switch to <span class="term"> custom</span>, the editor automatically populates with your <span class="filepath"> mbox.js</span> code. You can replace this with the content of the <span class="filepath"> at.js</span> library. </li> 
     <li id="li_F8A46A7A25934A4BA37DA6CC75B2DB1F"> <b>At URL:</b> If your <span class="filepath"> at.js</span> or <span class="filepath"> mbox.js</span> is configured as desired, you can provide the URL to the file. Dynamic tag management will consume it for use in the <span class="keyword"> Adobe Target</span> tool. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Global Parameters - Adobe Target {#concept_0946C2AAB8044A9297FF498DB7157F42}

Descriptions of the fields and options in the Global Parameters settings in dynamic tag management for an Adobe Target Tool. 

<!-- 

target_global_params.xml

 -->

Global parameters let you pass additional data to the global [!DNL Adobe Target] mbox, and also on a per-page basis via page load rules.

The parameters configured in dynamic tag management do not override parameters already defined on the page, but instead appends and sequences to create maximum flexibility and customization on a per page basis.

**[!UICONTROL Property]** > **[!UICONTROL   ![](assets/settings_gear.png) Edit Tool]** > **[!UICONTROL Library Management]**

![](assets/target_global.png) 

<table id="table_1BC88AFFC99648C7995D3B88BB0DAA8C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Name </p> </td> 
   <td colname="col2"> <p> Indicate the name of the additional parameter(s) you wish to pass to the global mbox. </p> 
    <!--<p>Adobe Target does not accept the usage of <i>&amp;</i> in this field. Using it leads to errors on the web page. </p>--> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Value </p> </td> 
   <td colname="col2"> <p> Indicate the value of the additional parameter(s) you want to pass to the global mbox. The value is typically a data element. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Mbox rule example for Dynamic Tag Management {#task_2642B010AB204834A2AF7CEACDAC23F7}

An example of how to place wrapping mboxes with built-in flicker handling via dynamic tag management when an Adobe Target tool is installed. 

<!-- 

t_target_example.xml

 -->

This functionality currently uses the *`mboxUpdate`* method. 

1. Click **[!UICONTROL Property]** > **[!UICONTROL Rules]** > **[!UICONTROL Page Load Rules]** > **[!UICONTROL Create New Rule]**.
1. Name and configure the rule.

   ![Step Info](assets/target_example_1.png)

   Configure the rule so that it fires only on the pages where you want to deploy the mbox.

   >[!NOTE]
   >
   >Adobe recommends load rules triggering mboxes at *`Top of Page`* to ensure the default content is hidden until the mbox response has been received.

   See [Rule Conditions and Functions](../rules/rules.md#reference_662A7B7D177C46C98980CD317A7A8861) for information about available rule criteria. 

1. Expand **[!UICONTROL Adobe Target]**.

   ![](assets/target_example_2.png)

   Specify the element to wrap with the mbox using a CSS selector, name the mbox, then configure the timeout if needed. (It is generally recommended to leave this at the default 1500 ms). 

1. Configure the parameters you want to add to the [!DNL Target] mbox or to the global [!DNL Target mbox].

   ![Step Result](assets/target_example_3.png)

   In this example, this rule deploys an mbox named `Hero` that wraps a `div` element with an `id` of `hero` and includes an mbox parameter named `Page Name` with a value of `homepage`. It also includes a parameter named `Path` with a value of `home` that it passes to the global mbox.

   ![](assets/target_example_4.png)

   >[!NOTE]
   >
   >You can also use data elements in the parameter UI fields to dynamically populate the value. See [Data Elements](../data_elements.md#concept_8A4591BD0F4241B6925D976482C43CD2) for more information on data elements.

