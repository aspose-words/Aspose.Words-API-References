---
title: StructuredDocumentTagCollection.get_by_id method
linktitle: get_by_id method
articleTitle: get_by_id method
second_title: Aspose.Words for Python
description: "StructuredDocumentTagCollection.get_by_id method. Returns the structured document tag by identifier."
type: docs
weight: 30
url: /de/python-net/aspose.words.markup/structureddocumenttagcollection/get_by_id/
---

## get_by_id(id) {#int}

Returns the structured document tag by identifier.


```python
def get_by_id(self, id: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| id | int | The structured document tag identifier. |

### Remarks

Returns null if the structured document tag with the specified identifier cannot be found.




### Examples

Shows how to get structured document tag.

```python
doc = aw.Document(file_name=MY_DIR + 'Structured document tags by id.docx')
# Rufe das strukturierte Dokument-Tag anhand der Id ab.
sdt = doc.range.structured_document_tags.get_by_id(1160505028)
print(sdt.is_multi_section)
print(sdt.title)
# Rufe das strukturierte Dokument-Tag oder das bereichsbezogene Tag anhand des Titels ab.
sdt = doc.range.structured_document_tags.get_by_title('Alias4')
print(sdt.id)
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTagCollection](../)

