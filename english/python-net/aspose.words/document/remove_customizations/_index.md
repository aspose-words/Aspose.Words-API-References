---
title: Document.remove_customizations method
linktitle: remove_customizations method
articleTitle: remove_customizations method
second_title: Aspose.Words for Python
description: "Document.remove_customizations method. Removes toolbar and keyboard command customizations from the document."
type: docs
weight: 710
url: /python-net/aspose.words/document/remove_customizations/
---

## remove_customizations() {#default}

Removes toolbar and keyboard command customizations from the document.


```python
def remove_customizations(self):
    ...
```

### Examples

Shows how to remove toolbar and keyboard command customizations from the document.

```python
doc = aw.Document(file_name=MY_DIR + 'Customized menu.docx')
# Remove all custom document UI customizations, including custom context menu entries.
doc.remove_customizations()
doc.save(file_name=ARTIFACTS_DIR + 'Document.RemoveCustomizations.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

