---
title: StructuredDocumentTagCollection.get_by_id method
linktitle: get_by_id method
articleTitle: get_by_id method
second_title: Aspose.Words for Python
description: "StructuredDocumentTagCollection.get_by_id method. Returns the structured document tag by identifier."
type: docs
weight: 30
url: /zh/python-net/aspose.words.markup/structureddocumenttagcollection/get_by_id/
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
# 通过 Id 获取结构化文档标签。
sdt = doc.range.structured_document_tags.get_by_id(1160505028)
print(sdt.is_multi_section)
print(sdt.title)
# 通过 Title 获取结构化文档标签或有范围标签。
sdt = doc.range.structured_document_tags.get_by_title('Alias4')
print(sdt.id)
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTagCollection](../)

