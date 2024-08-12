---
title: Range.structured_document_tags property
linktitle: structured_document_tags property
articleTitle: structured_document_tags property
second_title: Aspose.Words for Python
description: "Range.structured_document_tags property. Returns a [Range.structured_document_tags](./) collection that represents all structured document tags in the range."
type: docs
weight: 50
url: /python-net/aspose.words/range/structured_document_tags/
---

## Range.structured_document_tags property

Returns a [Range.structured_document_tags](./) collection that represents all structured document tags in the range.



```python
@property
def structured_document_tags(self) -> aspose.words.markup.StructuredDocumentTagCollection:
    ...

```

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

* module [aspose.words](../../)
* class [Range](../)

