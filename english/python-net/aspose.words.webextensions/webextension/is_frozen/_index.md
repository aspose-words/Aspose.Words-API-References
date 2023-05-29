---
title: WebExtension.is_frozen property
linktitle: is_frozen property
articleTitle: is_frozen property
second_title: Aspose.Words for Python
description: "WebExtension.is_frozen property. Specifies whether the user can interact with the web extension or not."
type: docs
weight: 40
url: /python-net/aspose.words.webextensions/webextension/is_frozen/
---

## WebExtension.is_frozen property

Specifies whether the user can interact with the web extension or not.


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

* module [aspose.words.webextensions](../../)
* class [WebExtension](../)

