---
description: Use dynamic tag management to add header and footer code that determines the loading of JavaScript and page content on your site. You must install both the header and footer code on every page of your site, regardless of the hosting option used.
keywords: dynamic tag management
seo-description: Use dynamic tag management to add header and footer code that determines the loading of JavaScript and page content on your site. You must install both the header and footer code on every page of your site, regardless of the hosting option used.
seo-title: Header and Footer Code
solution: Marketing Cloud,Analytics,Dynamic Tag Management
title: Header and Footer Code
uuid: f704fdf9-bab2-4445-92da-20609822c380
index: y
internal: n
snippet: y
---

# Header and Footer Code

Use dynamic tag management to add header and footer code that determines the loading of JavaScript and page content on your site. You must install both the header and footer code on every page of your site, regardless of the hosting option used.

<table id="table_945212E5A33F414DB053569EAE2840DC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> DTM Basics: Embedding Code </th> 
   <th colname="col2" class="entry"> Time: 4:20 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 
     <div width="550px" class="video-iframe"> 
      <iframe src="https://video.tv.adobe.com/v/17171/" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" oallowfullscreen="true" msallowfullscreen="true" allowfullscreen="allowfullscreen" scrolling="no" width="550" height="345">https://video.tv.adobe.com/v/17171/</iframe>
     </div> </p> </td> 
   <td colname="col2"> <p>By then end of this video you should be able to: </p> <p> 
     <ul id="ul_6D341D136F5944F98229AD62937310F5"> 
      <li id="li_32CDF16E61EB42BC9A7CC10997ED7AC7">Understand the embedding elements </li> 
      <li id="li_0A65BFE7ED104A9B9270BEFF9A1FD27E">Explain the difference between staging and production </li> 
      <li id="li_C4FED8A9C34E420FB5EA6F0AD22651E1">Not confuse embedding codes with the s.code </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Because dynamic tag management includes a snippet of code in both your header and footer, you can run rules at the beginning or end of a page. This ability allows you to implement testing tools and other technologies while retaining control over tracking your pages.

Dynamic tag management creates staging and production embed codes you can use to test your changes in your staging environment before pushing changes to your production environment.

>[!IMPORTANT]
>
>For a successful implementation, it is critical that you follow these instructions as they appear in Adobe Help. Specifically, you must place the header code in the `<head>` section of your document templates. Also, you must place the footer code just before the closing `</body>` tag. Placing either of these embed codes elsewhere in your markup, or using asynchronous methods to append the embed codes, or wrapping the embed codes in any way, are *not* a supported implementations of dynamic tag management. The embed codes must be implemented exactly as provided.

An unsupported implementation will yield unexpected results and prevent Customer Care and Engineering from assisting with your implementation.

Because dynamic tag management includes a snippet of code in both your header and footer, you can run rules at the beginning or end of a page. This ability allows you to implement testing tools and other technologies while retaining control over tracking your pages. 
