---
author: [Alfresco Documentation, Alfresco Documentation]
audience: 
---

# Migrating servers

The process of migrating an instance of Alfresco Content Services running on one server to another server follows a similar pattern to the backup process, with additional steps to ensure any configuration is also copied over.

The `dir.root` property is usually defined in the alfresco-global.properties file.

The `dir.root` is often a directory named `alf_data` within the directory where Alfresco Content Services is installed, and will hold both content and full text indexes by default. The `dir.root` location is also reported in the logs when the server is started.

-   **[Backing up Alfresco Content Services Server 1](../tasks/migrate-backup-server.md)**  
This task describes how to back up the first server for migration.
-   **[Restoring to Alfresco Content Services Server 2](../tasks/migrate-restore-server.md)**  
This task describes how to restore a back up of a server to another server.

**Parent topic:**[Migrating](../concepts/migrating.md)

