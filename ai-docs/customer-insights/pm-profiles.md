---
title: "Profiles | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 02/21/2019
ms.reviewer: ""
ms.service: "dynamics-365-ai"
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
# Profiles

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

The **Profiles** page presents consolidated view on each customer, based on profile data you gathered from all of your data sources. The page also lets you search for customers. Each customer profile is represented by a Customer Card tile as shown below.

> [!div class="mx-imgBorder"] 
> ![](media/profiles-customers.png "Customer profiles")

In order to view more customers profiles, move to the next profiles page using the button shown below in red.

> [!div class="mx-imgBorder"] 
> ![](media/profiles-customers2.png "Customer profiles")

**Note:** Customer profiles are available once you create the unified Customer entity. Make sure to complete the Data Configuration process in order to unlock richer view on your customers. Visit the *Configure Data* section to learn more.

> [!div class="mx-imgBorder"] 
> ![](media/customer-card-tile.png "Customer Card tiles")

After selecting a customer tile, you will see additional information on that specific customer. As shown below, that information may include attributes such as **Country**, **Email**, **Address**, and **Phone** that exist in one or more of your data sources.

> [!div class="mx-imgBorder"] 
> ![](media/customer-card-tile-customer-info.png "Customer Card tile customer info")

## Search for customers

Searching for customers can be done using the Search field. You can simply type a value for one of the profile attributes' names (for example, the customer’s name). To enable search, an admin needs to configure the searchable attributes in the **Search, sort & filter** page. Note that the search will be executed only within the Customer Profile entity created during the data configuration process.

> [!div class="mx-imgBorder"] 
> ![](media/customer-card-tile-search.png "Customer Card tile search")

After clicking one of the customers' tiles, you can also search for a specific attribute within this customer's information.

> [!div class="mx-imgBorder"] 
> ![](media/customer-card-tile-search2.png "Customer Card tile search")

## Filter customers

Filtering customers can be done via a menu that includes your Customer Profile entity fields as filters. 

First, select **Filter**.

> [!div class="mx-imgBorder"] 
> ![](media/customer-card-tile-filter.png "Customer Card tile filter")

Then, simply check the boxes next to the filters with which to search customers by as shown below. Same as for the **Search** field, you will be able to filter only by attributes that exist in your Customer Profile entity and that were defined by the administrator in the **Search, sort & filter** page.

> [!div class="mx-imgBorder"] 
> ![](media/profiles-customers3.png "Customer profiles")

You can remove your saved filters using **Clear filters**.

> [!div class="mx-imgBorder"] 
> ![](media/customer-card-tile-clear-filter.png "Customer Card tile clear filter")

## Next Step
Make sure to review both the **Data Sources** and **Configure Data** sections where you will learn to ingest and configure your data.