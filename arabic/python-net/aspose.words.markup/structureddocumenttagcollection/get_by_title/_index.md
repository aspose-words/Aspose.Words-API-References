---
title: StructuredDocumentTagCollection.get_by_title method
linktitle: get_by_title method
articleTitle: get_by_title method
second_title: Aspose.Words for Python
description: "StructuredDocumentTagCollection.get_by_title method. Returns the first structured document tag encountered in the collection with the specified title."
type: docs
weight: 50
url: /ar/python-net/aspose.words.markup/structureddocumenttagcollection/get_by_title/
---

## get_by_title(title) {#str}

Returns the first structured document tag encountered in the collection with the specified title.


```python
def get_by_title(self, title: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| title | str | The title of structured document tag. |

### Remarks

Returns null if the structured document tag with the specified title cannot be found.




### Examples

Shows how to get structured document tag.

```python
doc = aw.Document(file_name=MY_DIR + 'Structured document tags by id.docx')
# احصل على علامة المستند المهيكلة بواسطة المعرف Id.
sdt = doc.range.structured_document_tags.get_by_id(1160505028)
print(sdt.is_multi_section)
print(sdt.title)
# احصل على علامة المستند المهيكلة أو العلامة ذات النطاق بواسطة العنوان Title.
sdt = doc.range.structured_document_tags.get_by_title('Alias4')
print(sdt.id)
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTagCollection](../)

