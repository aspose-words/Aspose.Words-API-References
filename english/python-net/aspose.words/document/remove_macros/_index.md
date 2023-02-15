---
title: remove_macros method
second_title: Aspose.Words for Python via .NET API Reference
description: "Removes all macros (the VBA project) as well as toolbars and command customizations from the document."
type: docs
weight: 660
url: /python-net/aspose.words/document/remove_macros/
---

## remove_macros() {#default}

Removes all macros (the VBA project) as well as toolbars and command customizations from the document.


```python
def remove_macros(self):
    ...
```

By removing all macros from a document you can ensure the document contains no macro viruses.




### Examples

Shows how to remove all macros from a document.

```python
doc = aw.Document(MY_DIR + "Macro.docm")

self.assertTrue(doc.has_macros)
self.assertEqual("Project", doc.vba_project.name)

# Remove the document's VBA project, along with all its macros.
doc.remove_macros()

self.assertFalse(doc.has_macros)
self.assertIsNone(doc.vba_project)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

