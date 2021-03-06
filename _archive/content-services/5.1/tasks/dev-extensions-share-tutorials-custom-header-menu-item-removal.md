---
author: Alfresco Documentation
---

# Removing a menu item \(Aikau\)

This tutorial shows you how to remove menu items.

You should complete the [previous tutorials](dev-extensions-share-tutorials-custom-header-admin-menu.md) before attempting this one.

In this tutorial you customize the Share header menu. In the previous two tutorials you saw how to add menu items and customize them. In this one you learn how to remove menu items. This is demonstrated using two different techniques: using a built-in helper function,`widgetUtils.deleteObjectFromArray`, and through configuration exposed by the `alfresco/header/AlfSitesMenu` widget.

1.  In the first part of this tutorial you use the helper function `widgetUtils.deleteObjectFromArray` to remove menu items. This function takes three arguments:

    1.  The object to remove the widget definition from \(you can typically just use `model.jsonModel`\)
    2.  The attribute to search for \(you should use `id`\)
    3.  The value to match against the target attribute \(the `id` attribute of the widget definition to remove\)
    For example, to remove the **My Files** link from the menu bar you would include the following code in the file share-header.get.js \(see the two previous tutorials\):

    ```
    
                        
    widgetUtils.deleteObjectFromArray(model.jsonModel, "id", "HEADER_MY_FILES");                    
                        
                    
    ```

    Try this out by removing the **My Files** menu item.

2.  In your IDE edit the file share-header.get.js that you created in the previous tutorials.

3.  At the end of the file add the following code:

    ```
    
            
    widgetUtils.deleteObjectFromArray(model.jsonModel, "id", "HEADER_MY_FILES");        
            
        
    ```

    Save the file.

4.  Restart the application server by running the [run.sh](../concepts/alfresco-sdk-cmd-reference-aio.md) command to update your Surf extension module.

5.  Log in to Share, you will see that the **My Files** menu item is no longer present on the main menu.

    In this part of the tutorial you have seen how to use the helper function to remove a menu item. Note your code could have been more complex. For example, to hide MyFiles for users who are not admins you could use the following code:

    ```
    
                        
    if (!user.isAdmin)
    {
      widgetUtils.deleteObjectFromArray(model.jsonModel, "id", "HEADER_MY_FILES");
    }                    
                        
                    
    ```

6.  In this part of the tutorial you see how to remove items from the Sites drop-down menu. Although you saw how to customize the Sites menu in the [previous tutorial](dev-extensions-share-tutorials-custom-header-sites-menu.md), you can also use configuration attributes that allow the easy removal of Site menu items.

    These boolean attributes are as follows:

    |Attribute|Description|
    |---------|-----------|
    |showCreateSite|Controls whether the **Create Site** menu item is displayed.|
    |showSiteFinder|Controls whether the **Site Finder** menu item is displayed.|
    |showUsefulGroup|Controls whether the **Useful** menu group is displayed. Will override `showCreateSite`, `showSiteFinder` and `showFavourites`.|
    |showRecentSites|Controls whether the **Recent Sites** menu group is displayed.|
    |showFavourites|Controls whether the **Facvourites** menu item and favourite controls \(such as add/remove\) are displayed.|

    For example, to hide the **Site Finder**, you would include the following code in share-header.get.js:

    ```
    
                        
    // Find the "Sites" menu...
    var sitesMenu = 
      widgetUtils.findObject(model.jsonModel, "id", "HEADER_SITES_MENU");
    if (sitesMenu != null)
    {
      // Hide the site finder...
      sitesMenu.config.showSiteFinder = false;
    }                    
                        
                    
    ```

7.  In your IDE edit the file share-header.get.js that you created in the previous tutorials.

8.  At the end of the file add the following code:

    ```
    
            
    // Find the "Sites" menu...
    var sitesMenu = 
      widgetUtils.findObject(model.jsonModel, "id", "HEADER_SITES_MENU");
    if (sitesMenu != null)
    {
      // Hide the site finder...
      sitesMenu.config.showSiteFinder = false;
    }        
        
    ```

    Save the file.

9.  Restart the application server by running the [run.sh](../concepts/alfresco-sdk-cmd-reference-aio.md) command to update your Surf extension module.

10. Log in to Share. Select the Sites menu item from the main menu bar, you will see that the Site Finder is no longer present on the drop-down menu.


In this tutorial, you used two techniques for removing menu items from the main header menu bar.

**Parent topic:**[Customizing the Share header menu \(Aikau\)](../tasks/dev-extensions-share-tutorials-custom-share-header-menu.md)

