---
author: [Alfresco Documentation, Alfresco Documentation]
audience: 
category: Alfresco Team
option: [activities feed, email]
---

# Managing activities feed emails

The Activities Feed shows the settings for activity emails in your Alfresco environment. Activity emails are sent to the Administrator user to provide information for managing Alfresco.

Email notification are sent for all events that you would see in the activity feed dashlet. This includes events that are triggered in all of the sites that you are a member of and of all people you are following. Scheduled activity digests are sent with an email, based on the data that is available in your personal activity feed.

1.  Open the Admin Console, and then click **Activities Feed**.

2.  On the Activities Feed page, click **Edit**.

    You see the Edit: Activities Feed page.

3.  To activate emails for the Activities Feed, select the **Feed Notifier Enabled** check box.

4.  Change the properties to control the frequency of emails and number of items shown.

    |Property|Example setting|What is it?|
    |--------|---------------|-----------|
    |**Maximum Age \(mins\)**|44640|This sets the maximum age in minutes of the activity events shown in the Activities Feed notification emails. Activities that are older than the maximum age are not shown in the Activities dashlet. The default is set to 44640 \(31-day month\).|
    |**Repeat Interval \(mins\)**|1440|This sets how often that you will receive the Activities Feed notification emails. The default is set for you to receive emails every day.|
    |**Maximum Size**|100|This sets the maximum number of activity events that are reported on in the Activities Feed notification emails.|

5.  When you've finished changing the properties, click **Save**.

    If you do not want to save the changes, click **Cancel**.

6.  Finally, you need to make sure that you have set the **Host** property on the Email \(Outbound\) page in the Admin Console.

    Setting this property to the email host means that users can receive emails, and send and receive site invites. Individual users can enable or disable email notifications in their **My Profile** settings.


-   **[Activities feed email notifications list](../concepts/adminconsole-email-notification-list.md)**  
The full list of individual events generated by Alfresco is defined in the share\\WEB-INF\\classes\\alfresco\\site-webscripts\\org\\alfresco\\components\\dashlets\\activity-list.get.properties file.

**Parent topic:**[Managing Alfresco using the Admin Console](../concepts/at-adminconsole.md)

**Related information**  


[Managing outbound emails](at-adminconsole-outboundemail.md)

