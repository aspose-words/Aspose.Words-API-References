---
title: StructuredDocumentTagCollection.remove_at method
linktitle: remove_at method
articleTitle: remove_at method
second_title: Aspose.Words for Python
description: "StructuredDocumentTagCollection.remove_at method. Removes a structured document tag at the specified index."
type: docs
weight: 70
url: /python-net/aspose.words.markup/structureddocumenttagcollection/remove_at/
---

## remove_at(index) {#int}

Removes a structured document tag at the specified index.


```python
def remove_at(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

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

