---
author: Alfresco Documentation
---

# `getInstance`

`getInstance(workflowInstanceId)` gets the workflow instance with the specified ID.

## Parameters

-   **workflowInstanceId**

    A string representing the ID of the workflow instance.


## Returns

Returns the workflow instance with the given ID or null if no workflow instance with the given ID exists.

## Example

```

    var id = "activiti$164";

    model.instance = workflow.getInstance(id);      
        
```

**Parent topic:**[Workflow Manager](../references/API-JS-WorkflowManager.md)

