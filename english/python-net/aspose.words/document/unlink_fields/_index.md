---
title: unlink_fields method
second_title: Aspose.Words for Python via .NET API Reference
description: "Unlinks fields in the whole document."
type: docs
weight: 700
url: /python-net/aspose.words/document/unlink_fields/
---

## unlink_fields() {#default}

Unlinks fields in the whole document.


```python
def unlink_fields(self):
    ...
```

Replaces all the fields in the whole document with their most recent results.

To unlink fields in a specific part of the document use [Range.unlink_fields()](../../range/unlink_fields/#default).




### Examples

Shows how to unlink all fields in the document.

```python
doc = aw.Document(MY_DIR + "Linked fields.docx")

doc.unlink_fields()
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

