---
title: "Merge | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 06/17/2019
ms.reviewer: ""
ms.service: dynamics-365-ai
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 83200632-a36b-4401-ba41-952e5b43f939
caps.latest.revision: 31
author: "jimholtz"
ms.author: "jimholtz"
manager: "kvivek"
---
# Merge

The merge phase is the last phase in the data unification process. Its purpose is reconciling conflicting data. Examples of conflicting data might be a customer name that resides in two of your datasets but shows up a little differently in each (“Grant Marshall” versus “Grant,” for example), or a phone number format that differs slightly (617-8030-91X versus 617803091X). Merging those conflicting data points is done on an attribute-by-attribute basis. 

Once you've completed the match phase, you can start the merge phase by selecting the **Merge** tile on the **Unify** page.

## Step 1: Review system recommendations

After you select the **Merge** tile, you see the **Merge** page.

> [!div class="mx-imgBorder"] 
> ![Merge page](media/configure-data-merge-profile-attributes-full-name.png "Merge page")

On this page, you can choose and exclude attributes:

- Choose all the attributes that should be merged within your unified customer profile entity (the end result of the configuration process). Notice that some attributes were already auto-merged by the system.

   The following attribute information is shown on the **Merge** page:

   - The attribute's name appears in the first column.
   - The attribute's entity is specified in the second column.
   - The attribute's data source is specified in the third column.
   
- If you wish to view the attributes that are included in one of your auto-merged attributes, select that merged attribute. The two attributes that compose that merged attribute will show up in two new rows beneath the merged attribute.

   > [!div class="mx-imgBorder"] 
   > ![Select merged attribute](media/configure-data-merge-profile-attributes.png "Select merged attribute")

- If you wish to unmerge any of the auto-merged attributes, use the button shown in the following example:

   > [!div class="mx-imgBorder"] 
   > ![Unmerge attributes](media/configure-data-merge-profile-attributes-add-merged.png "Unmerge attributes")
   
-  In the drop-down menu, select **Separate fields**.
   
   
   <!-- I don't see "Separate fields" in the drop-down menu shown in this screenshot. -->
   
   > [!div class="mx-imgBorder"] 
   > ![Separate fields](media/configure-data-merge-profile-attributes2.png "Separate fields")

- Remove attributes from the customer profile entity. If you think that some attributes should be excluded from the final customer profile entity, select the  **Remove** option from the same drop-down menu.


<!-- I don't see a Remove option in the drop-down menu shown in the screenshot. -->

   > [!div class="mx-imgBorder"] 
   > ![Exclude attributes](media/configure-data-merge-dont-merge.png "Exclude attributes")

   Attributes will move to the **Removed from customer record** section.
   
   
   <!-- I don't see a section with that name in the screenshot. -->

   > [!div class="mx-imgBorder"] 
   > ![Remoted attributes](media/configure-data-merge-exclude-from-profile.png "Removed attributes")

## Step 2: Manually add a merged attribute

Add a merged attribute with **Combine fields**, as shown in this example.


<!-- I don't see a Combine fields option in the screenshot. -->


> [!div class="mx-imgBorder"] 
> ![Add merged attributes](media/merge-add-merge-attribute.png "Add merged attributes")

We will perform the manual merge process within the **Combine fields** pane.


<!-- Should it be "Merged field" as shown in the screenshot? -->


> [!div class="mx-imgBorder"] 
> ![Merge attribute name](media/configure-data-merge-attribute-name2.png "Merge attribute name")

This pane consists of four parts:

**Name**: Type an attribute name. You can identify it on the **Merge** page later.

**Display name**: Give your merged attribute a more friendly name that will appear in the unified Customer Profile entity. 

**Select duplicate attributes**: Within this menu, select the attributes that you want to merge from the matched entities. You can also use Search to locate the attributes. 


<!-- Regarding the above, the screenshot shows "Select duplicate fields." -->


**Rank by importance:** Prioritize one attribute above the others—the values for your merged attribute will come only from that source. In the example below, since we think that the *WebAccountCSV* entity includes the most accurate data about the *Full Names* attribute, we will prioritize this entity over *ContactCSV* by selecting the arrow next to *WebAccountCSV*. As a result, *WebAccountCSV* moves to first priority, while *ContactCSV* moves to second priority when pulling values for the *Full Name* attribute:

> [!div class="mx-imgBorder"] 
> ![Merged attributes](media/configure-data-merge-attributes2.png "Merged attributes")

## Step 3: Run your merge

Whether you manually merge attributes or let the system merge for you, at this point you can run your merge. Select **Save** and then **Run** at the top of the page.

> [!div class="mx-imgBorder"] 
> ![Data merge Save and Run](media/configure-data-merge-save-run.png "Data merge Save and Run")

Note that if **Run** is disabled at this point, you should try two things:

- First, refresh your page and see if the button becomes active.

  > [!div class="mx-imgBorder"] 
  > ![Data merge](media/configure-data-merge-image18.png "Data merge")

- Second, go back to the **Match** page and reselect **Run**. Then, return to the **Merge** page and see if that resolved the problem.

Once the **Merge is running** message disappears, merge has completed and resolved contradictions in your data according to the policies that you have defined. Both your merged and unmerged attributes will be included in your unified profile entity, while your excluded attributes will not.

> [!div class="mx-imgBorder"] 
> ![Data merge in progress](media/configure-data-merge-image17.png "Data merge in progress")

> [!div class="mx-imgBorder"] 
> ![Save and Run](media/configure-data-merge-save-run.png "Save and Run")


### Next Step

Congratulations! You have completed both the data ingestion and data unification phases. Now you are ready to do one of the following:

- Complete more data configurations (**Activities**, **Relationships**, or **Enrichment**). Although they are  optional, they can help you unlock richer insights into your customers. 

- Continue to insight exploration via the **Segments**, **Customer Card**, and **Connectors** sections. Note that **Segments** will equip you with aggregate-level insights on your customer base, while **Customer Card** and **Connectors** will enable you to unlock insights on each of your customers.
 
