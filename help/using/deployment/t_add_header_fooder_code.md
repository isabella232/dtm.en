---
description: Add header and footer code in dynamic tag management.
keywords: dynamic tag management
seo-description: Add header and footer code in dynamic tag management.
seo-title: Add header and footer code
solution: Marketing Cloud,Analytics,Dynamic Tag Management
title: Add header and footer code
uuid: 701a5c9f-f6c6-4376-b047-760b9f318c8d
index: y
internal: n
snippet: y
---

# Add header and footer code

Add header and footer code in dynamic tag management.

1. Copy the production header code and place it within the [!DNL HEAD] section of your site HTML.

   Place the code as close to the [!DNL <head>] tag as possible. This code snippet should be placed on every page of your live production site.

   >[!NOTE]
   >
   >Production embed code reflects only the published items in that [property](../web_property.md#concept_8413810BEAEC4AA48996BE9AFCF141DD). However, embed code for staging reflects all items in the associated property, regardless of the published or unpublished state. To test unpublished items on your production site, locally enable staging in the console by following the instructions in [Test unpublished rules for Akamai hosting](../t_rules_create/t_test_rules_amazon.md#task_B397167F9E9B4487957AD6CE2AD47259).

1. Copy the production footer code and place it in the [!DNL BODY] section of your site HTML.

   Place the code as close to the [!DNL </body>] tag as possible. 
1. Copy the staging header and footer code, then repeat the steps above on your staging site.

   >[!NOTE]
   >
   >The difference between production and staging code snippets is the addition of [!DNL -staging] to the filename in the staging version. The footer code remains the same in staging and production.

