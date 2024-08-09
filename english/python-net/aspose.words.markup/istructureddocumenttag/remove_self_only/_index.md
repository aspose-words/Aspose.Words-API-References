---
title: IStructuredDocumentTag.remove_self_only method
linktitle: remove_self_only method
articleTitle: remove_self_only method
second_title: Aspose.Words for Python
description: "IStructuredDocumentTag.remove_self_only method. Removes just this SDT node itself, but keeps the content of it inside the document tree."
type: docs
weight: 180
url: /python-net/aspose.words.markup/istructureddocumenttag/remove_self_only/
---

## remove_self_only() {#default}

Removes just this SDT node itself, but keeps the content of it inside the document tree.


```python
def remove_self_only(self):
    ...
```

### Examples

Shows how to remove structured document tag, but keeps content inside.

```python
doc = aw.Document(MY_DIR + 'Structured document tags.docx')
# This collection provides a unified interface for accessing ranged and non - ranged structured tags.
sdts = [tag for tag in doc.range.structured_document_tags]
self.assertEqual(5, len(sdts))
# Here we can get child nodes from the common interface of ranged and non - ranged structured tags.
for std in sdts:
    if std.get_child_nodes(aw.NodeType.ANY, False).count > 0:
        std.remove_self_only()
sdts = [tag for tag in doc.range.structured_document_tags]
self.assertEqual(0, len(sdts))
```

### See Also

* module [aspose.words.markup](../../)
* class [IStructuredDocumentTag](../)

