﻿---
title: TaskPane class
linktitle: TaskPane class
articleTitle: TaskPane class
second_title: Aspose.Words for Python
description: "aspose.words.webextensions.TaskPane class. Represents an add-in task pane object"
type: docs
weight: 10
url: /python-net/aspose.words.webextensions/taskpane/
---

## TaskPane class

Represents an add-in task pane object.
To learn more, visit the [Work with Office Add-ins](https://docs.aspose.com/words/python-net/work-with-office-add-ins/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [TaskPane()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [dock_state](./dock_state/) | Specifies the last-docked location of this task pane object. |
| [is_locked](./is_locked/) | Specifies whether the task pane is locked to the document in the UI and cannot be closed by the user. |
| [is_visible](./is_visible/) | Specifies whether the task pane shows as visible by default when the document opens. |
| [row](./row/) | Specifies the index, enumerating from the outside to the inside, of this task pane among other persisted task panes docked in the same default location. |
| [web_extension](./web_extension/) | Represents an web extension object. |
| [width](./width/) | Specifies the default width value for this task pane instance. |

### Examples

Shows how to add a web extension to a document.

```python
doc = aw.Document()

# Create task pane with "MyScript" add-in, which will be used by the document,
# then set its default location.
my_script_task_pane = aw.webextensions.TaskPane()
doc.web_extension_task_panes.add(my_script_task_pane)
my_script_task_pane.dock_state = aw.webextensions.TaskPaneDockState.RIGHT
my_script_task_pane.is_visible = True
my_script_task_pane.width = 300
my_script_task_pane.is_locked = True

# If there are multiple task panes in the same docking location, we can set this index to arrange them.
my_script_task_pane.row = 1

# Create an add-in called "MyScript Math Sample", which the task pane will display within.
web_extension = my_script_task_pane.web_extension

# Set application store reference parameters for our add-in, such as the ID.
web_extension.reference.id = "WA104380646"
web_extension.reference.version = "1.0.0.0"
web_extension.reference.store_type = aw.webextensions.WebExtensionStoreType.OMEX
web_extension.reference.store = "en-US"
web_extension.properties.add(aw.webextensions.WebExtensionProperty("MyScript", "MyScript Math Sample"))
web_extension.bindings.add(aw.webextensions.WebExtensionBinding("MyScript", aw.webextensions.WebExtensionBindingType.TEXT, "104380646"))

# Allow the user to interact with the add-in.
web_extension.is_frozen = False

# We can access the web extension in Microsoft Word via Developer -> Add-ins.
doc.save(ARTIFACTS_DIR + "Document.create_web_extension.docx")

# Remove all web extension task panes at once like this.
doc.web_extension_task_panes.clear()

self.assertEqual(0, doc.web_extension_task_panes.count)
```

### See Also

* module [aspose.words.webextensions](../)

