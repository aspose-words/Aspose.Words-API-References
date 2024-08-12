---
title: StructuredDocumentTagCollection.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "StructuredDocumentTagCollection.remove method. Removes the structured document tag with the specified identifier."
type: docs
weight: 60
url: /python-net/aspose.words.markup/structureddocumenttagcollection/remove/
---

## remove(id) {#int}

Removes the structured document tag with the specified identifier.


```python
def remove(self, id: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| id | int | The structured document tag identifier. |

### Examples

Shows how to remove structured document tag.

```python
doc = aw.Document(file_name=MY_DIR + 'Structured document tags.docx')
structured_document_tags = doc.range.structured_document_tags
sdt = None
i = 0
while i < structured_document_tags.count:
    sdt = structured_document_tags[i]
    print(sdt.title)
    i += 1
sdt = structured_document_tags.get_by_id(1691867797)
self.assertEqual(1691867797, sdt.id)
self.assertEqual(5, structured_document_tags.count)
# Remove the structured document tag by Id.
structured_document_tags.remove(1691867797)
# Remove the structured document tag at position 0.
structured_document_tags.remove_at(0)
self.assertEqual(3, structured_document_tags.count)
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTagCollection](../)

