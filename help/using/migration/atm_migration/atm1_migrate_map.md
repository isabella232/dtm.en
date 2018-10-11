---
description: How to migrate from each Adobe Tag Manager 1.0 tag to a dynamic tag management tag.
seo-description: How to migrate from each Adobe Tag Manager 1.0 tag to a dynamic tag management tag.
seo-title: Adobe Tag Manager 1.0 to Dynamic Tag Management Mapping
solution: Dynamic Tag Management
title: Adobe Tag Manager 1.0 to Dynamic Tag Management Mapping
uuid: 80b5a404-ca60-4019-b8b5-911e8f1010fc
index: y
internal: n
snippet: y
---

# Adobe Tag Manager 1.0 to Dynamic Tag Management Mapping

How to migrate from each Adobe Tag Manager 1.0 tag to a dynamic tag management tag.

* [Custom Core JavaScript](../../migration/atm_migration/atm1_migrate_map.md#section_4ED3898D44994C71AC06E5B6AFB4E758) 
* [Product Code](../../migration/atm_migration/atm1_migrate_map.md#section_97CE3C7BB84C48388F2991D7598F782C) 
* [Custom Code (after products)](../../migration/atm_migration/atm1_migrate_map.md#section_7C14C9392E6A470FA9A2AB06D2D798A5)

## Custom Core JavaScript {#section_4ED3898D44994C71AC06E5B6AFB4E758}

<table id="table_8117F3D67FA84846B2C4130CB4BAC71B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Tag Manager 1.0 tag </th> 
   <th colname="col2" class="entry"> Dynamic Tag Management </th> 
   <th colname="col3" class="entry"> Migration Instructions </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Custom Core JavaScript </p> </td> 
   <td colname="col2"> <p>JavaScript / Third Party Tag </p> </td> 
   <td colname="col3"> <p> Custom JavaScript can be deployed directly into the JavaScript / Third Party Tags section of a rule. In most cases, you can paste the page code provided by the vendor directly into a tag with no additional configuration. </p> <p> If any product specific code was included in this section in Adobe Tag Management, it will need to be specifically migrated into the applicable tool in dynamic tag management. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Product Code {#section_97CE3C7BB84C48388F2991D7598F782C}

<table id="table_4EB3B9F9DF19450093634021DA562BC4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Tag Manager 1.0 Product Code Tag </th> 
   <th colname="col2" class="entry"> Dynamic Tag Management </th> 
   <th colname="col3" class="entry"> Migration Instructions </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="keyword"> SiteCatalyst </span> </p> <p> <span class="keyword"> SiteCatalyst </span> &gt; <span class="keyword"> Survey </span></p> <p> <span class="keyword"> SiteCatalyst </span> &gt; Video Tracking </p> <p> <span class="keyword"> SiteCatalyst </span> &gt; <span class="keyword"> Genesis </span> Integrations </p> </td> 
   <td colname="col2"> <p>Adobe Analytics Tool </p> </td> 
   <td colname="col3"> <p> Follow the instructions in <a href="../../tools/analytics_dtm.md#concept_FBA6679A0B79490F8296437F11E5E4F8" format="dita" scope="local"> Adobe Analytics Settings </a> to add an Adobe Analytics tool in dynamic tag management. </p> <p> <b>Option 1</b> </p> <p> Host code using the <span class="uicontrol"> Managed by Adobe </span> option. This method leverages the base version of the <span class="keyword"> AppMeasurement </span> code and allows you to choose between the latest available code versions. </p> <p style="text-align: center;"> <img href="assets/library_mgmt_atm1.png" id="image_874AA16BDD684CF38037C4A03EC9FD2C"> </img> </p> <p>With this option, <i>above this line</i> customization can be configured in the available interface fields or pasted into the <span class="wintitle"> Customize Page Code </span> editor. </p> <p> <b>Option 2</b> </p> <p> Manually host the s_code / <span class="keyword"> AppMeasurement </span> file in dynamic tag management. This method is recommended when the current code is highly customized or if a legacy code version is used. </p> 
    <ol id="ol_80FC5BB741644D88A0C7C325C9481F7C"> 
     <li id="li_6DAD5A8B05D24ED493F0F8689F3B6B34">In <span class="keyword"> Adobe Tag Management </span> 1.0, click <span class="uicontrol"> Edit </span> next to the latest container file. </li> 
     <li id="li_08F74BC7775D4C0F8354400F39BC31D3">Click <span class="uicontrol"> Preview </span> to view the generated file. </li> 
     <li id="li_EE10C87733184A80B86DBA93FF31FC77">Copy all of the <i>above this line</i> code. </li> 
    </ol> <p>This is all of the code beginning with the <span class="codeph"> s_account </span> declaration and ending with the first <span class="codeph"> s.setTagContainer </span> command. (Do not include this <span class="codeph"> s.setTagContainer </span> in this situation). Here is an example: </p> <p style="text-align: center;"> <img href="assets/prev_generated_code.png" id="image_8DB1405D0C8C46618579044FDDC083A7" /> </p> <p> Paste this code into the Custom editor in the <span class="keyword"> Adobe Analytics </span> tool in dynamic tag management. </p> <p style="text-align: center;"> <img href="assets/library_mgmt_custom.png" id="image_3FA5909D024A4A26BF050C6FAF4B4896"> </img> </p> <p>Then, from the same preview file in ATM, copy the below the line code. This code begins with: </p> <p> 
     <codeblock>
       ‘/*************&amp;nbsp;DO&amp;nbsp;NOT&amp;nbsp;ALTER&amp;nbsp;ANYTHING&amp;nbsp;BELOW&amp;nbsp;THIS&amp;nbsp;LINE!&amp;nbsp;**************/’ 
     </codeblock> </p> <p>and ends with the second <span class="term"> setTagContainer </span> function. (In this case, include the <span class="term"> setTagContainer </span> function, because this code should not be altered). Ensure the code only in this block is included. Any code set in the Custom Code (after products) section is included after this code block in the preview file, so ensure that only the intended code block is included in the copy. For example: </p> <p style="text-align: center;"> <img href="assets/prev_generated_code2.png" id="image_60D6A2F4F7B44044A2FB9797038147E0" /> </p> <p style="text-align: center;"> <img href="assets/prev_generated_code3.png" id="image_280C927B78F24145A97F5EB19432B1C6" /> </p> <p>Paste the code into the same Custom editor in dynamic tag management after the <span class="term"> above this line </span> code. </p> <p> <p>Note:  Since mistakes can occur with copy / paste, please be sure to review the implementation in dynamic tag management thoroughly and test extensively in staging before publishing to production to ensure the expected behavior is accomplished. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Demdex </p> </td> 
   <td colname="col2"> Adobe Audience Manager Tool </td> 
   <td colname="col3"> <p> Add and configure an <a href="../../tools/audiencemgmt.md#concept_F9887945039A473A9B2C6B16CBA5D822" format="dita" scope="local"> audience management </a> tool. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Custom Code (after products) {#section_7C14C9392E6A470FA9A2AB06D2D798A5}

<table id="table_EAF79577BEE441E7AB27301BB7B05A80"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 1.0 Custom Code Tag </th> 
   <th colname="col2" class="entry"> Dynamic Tag Management </th> 
   <th colname="col3" class="entry"> Migration Instructions </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>HTML </p> </td> 
   <td colname="col2"> <p>HTML </p> </td> 
   <td colname="col3"> <p> Create a rule with conditions mimicking the ATM firing rules. Copy all of the code into the <b>JavaScript / Third Party Tags</b> editor in the rule. Select between non-sequential and sequential HTML as applicable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>JavaScript </p> </td> 
   <td colname="col2"> <p>JavaScript </p> </td> 
   <td colname="col3"> <p> Create a rule with conditions mimicking the ATM firing rules. Copy all of the code into the <b>JavaScript / Third Party Tags</b> editor in the rule. Select between non-sequential and sequential JavaScript as applicable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Image Beacon </p> </td> 
   <td colname="col2"> <p>HTML </p> </td> 
   <td colname="col3"> <p> Create a rule with conditions mimicking the ATM firing rules. Copy the image URL from the 1.0 tag into the <b>JavaScript / Third Party Tags</b> editor of the rule. Wrap the <b>image url</b> in &lt;img&gt; tags and configure as non-sequential or sequential HTML as applicable. </p> <p> For example: <span class="codeph"> &lt;img height="1" width="1" style="border-style:none;" alt="" src=" imageurl"/&gt; </span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Remote Script </p> </td> 
   <td colname="col2"> <p>HTML </p> </td> 
   <td colname="col3"> <p> Create a rule with conditions mimicking the ATM firing rules. Copy the script URL from the 1.0 tag into the <b>JavaScript / Third Party Tags</b> editor of the rule. Wrap the <b>script url</b> in script tags and configure as non-sequential or sequential HTML as applicable. </p> <p> For example: <span class="codeph"> &lt;script type="text/javascript" src=" scripturl"&gt;&lt;/script&gt; </span></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>IFrame </p> </td> 
   <td colname="col2"> <p>HTML </p> </td> 
   <td colname="col3"> <p> Create a rule with conditions mimicking the ATM firing rules. Copy the iframe URL from the 1.0 tag into the <b>JavaScript / Third Party Tags</b> editor of the rule. Wrap the <b>iframe url</b> in iframe tags and configure as non-sequential or sequential HTML as applicable. </p> <p> For example: <span class="codeph"> &lt;iframe height="0" width="0" style="display:none;visibility:hidden" src=" iframeurl"&gt;&lt;/iframe&gt; </span></p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>If the conditions set in the firing rules are the same between each custom tag, they can be placed into a single rule in dynamic tag management.

