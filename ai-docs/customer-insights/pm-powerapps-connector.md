---
title: "Microsoft connector | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 08/09/2019
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
# Microsoft connector

Use the Microsoft connector to connect your PowerApps to Customer Insights or automate workflows with Microsoft Flow.

## Using the connector in PowerApps

Follow these steps to connect your app to Customer Insights:

1. Go to [https://powerapps.microsoft.com/](https://powerapps.microsoft.com/).

2. Select **New** and then create a **Blank app**. Choose phone or tablet layout. Tablet layout gives you more workspace.
   
   > [!div class="mx-imgBorder"] 
   > ![Create Blank app](media/connector-powerapps1.png "Create Blank app")

3. Add the Customer Insights connector by going to **View** > **Data Sources**.

   > [!div class="mx-imgBorder"] 
   > ![Select View > Data sources](media/connector-powerapps2.png "Select View > Data sources")

4. Select **Add data source**.

   > [!div class="mx-imgBorder"] 
   > ![Select Add data source](media/connector-powerapps3.png "Select Add data source")

5. Select **New connection**.

   > [!div class="mx-imgBorder"] 
   > ![Select New connection](media/connector-powerapps4.png "Select New connection")

6. Search for "Dynamics 365 Customer Insights" and select the **Dynamics 365 Customer Insights (Preview)** connector.

   > [!div class="mx-imgBorder"] 
   > ![Select Dynamics 365 Customer Insights (Preview)](media/connector-powerapps5.png "Select Dynamics 365 Customer Insights (Preview)")

7. Create the connection and sign in with the account you use for Customer Insights.

   > [!div class="mx-imgBorder"] 
   > ![Create the connection](media/connector-powerapps6.png "Create the connection")

8. Select the Customer Insights instance you want to fetch data from.

   > [!div class="mx-imgBorder"] 
   > ![Select an instance](media/connector-powerapps7.png "Select an instance")

9. Choose one or both of the following entities:

   - Customer: to use data from the unified customer profile.
   - Unified Customer Activity: to display the unified timeline on the app.

   > [!div class="mx-imgBorder"] 
   > ![Choose an entity](media/connector-powerapps8.png "Choose an entity")

10. You are now ready to start building an app with Customer Insights data. For example, let's add a gallery element to list the customers we have ingested on Customer Insights.

    > [!div class="mx-imgBorder"] 
    > ![Add a gallery element](media/connector-powerapps9.png "Add a gallery element")

11. Select **Customer** as the data source for items.

    > [!div class="mx-imgBorder"] 
    > ![Select a data source](media/connector-powerapps10.png "Select a data source")

    > [!div class="mx-imgBorder"] 
    > ![Select a data source](media/connector-powerapps11.png "Select a data source")

12.	You can change the data panel on the right to select which field for the Customer entity to show on the gallery.



    <!--Please confirm that the names in this and the next two screenshots are from an approved fictitious names list. -->


    > [!div class="mx-imgBorder"] 
    > ![Select field for Customer entity](media/connector-powerapps12.png "Select field for Customer entity")

13.	If you want to show any field from the selected customer on the gallery, fill in the Text property of a label:  **{Name_of_the_gallery}.Selected.{property_name}** 

    Example: Gallery1.Selected.address1_city
 
    > [!div class="mx-imgBorder"] 
    > ![Fill in Text property](media/connector-powerapps13.png "Fill in Text property")

14.	To display the unified timeline for a customer, add a Gallery element, and add the Items property: **Filter('Unified Customer Activity', CustomerId = {Customer_Id})** 

    Example: Filter('Unified Customer Activity', CustomerId = Gallery1.Selected.CustomerId)

    > [!div class="mx-imgBorder"] 

    > ![](media/connector-powerapps14.png "Add Gallery element")

## Automate workflows with Microsoft Flow

You can automate your business processes involving Dynamics 365 Customer Insights through [Microsoft Flow](https://flow.microsoft.com/). For more information, see the [Dynamics 365 Customer Insights connector reference](https://docs.microsoft.com/connectors/customerinsights/) and [Microsoft Flow documentation](https://docs.microsoft.com/flow/).

