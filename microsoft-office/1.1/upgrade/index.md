---
title: Upgrade Alfresco Office Services
---

Alfresco Office Services replaces the Microsoft SharePoint Protocol Support that was available until Alfresco One 4.2. Use this information to upgrade from Microsoft SharePoint Protocol Support, or from a previous version of AOS.

1. [Upgrade Alfresco]({% link content-services/6.0/upgrade/index.md %}).

    > **Note:** Make sure that you install the `alfresco-aos-module-1.1.x.amp`, and deploy the `_vti_bin.war` file.

    See [Install Alfresco Office Services]({% link microsoft-office/1.1/install/index.md %}) for more information.

2. Launch Alfresco Share.

    Test that you can edit your Microsoft Office documents by using the **Edit in Microsoft Office** action on any Office document in Alfresco Share.

3. Alternatively, open a Microsoft Office application (for example, Word) and select the **File** tab and **Open**. Enter the Alfresco server address in the **File name** field in the format: `http://servername:portnumber/alfresco/aos` and browse to a folder to edit an Office document.

    Any version history from the previous version of Alfresco will not be available in Microsoft Office, but is available in Alfresco Share.
