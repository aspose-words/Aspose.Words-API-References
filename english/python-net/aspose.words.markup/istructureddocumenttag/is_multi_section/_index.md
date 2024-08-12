---
title: IStructuredDocumentTag.is_multi_section property
linktitle: is_multi_section property
articleTitle: is_multi_section property
second_title: Aspose.Words for Python
description: "IStructuredDocumentTag.is_multi_section property. Returns true if this instance is a ranged (multi-section) structured document tag."
type: docs
weight: 40
url: /python-net/aspose.words.markup/istructureddocumenttag/is_multi_section/
---

## IStructuredDocumentTag.is_multi_section property

Returns true if this instance is a ranged (multi-section) structured document tag.


```python
@property
def is_multi_section(self) -> bool:
    ...

```

### Examples

Shows how to get structured document tag.

```python
doc = aw.Document(file_name=MY_DIR + 'Structured document tags by id.docx')
# Get the structured document tag by Id.
sdt = doc.range.structured_document_tags.get_by_id(1160505028)
print(sdt.is_multi_section)
print(sdt.title)
# Get the structured document tag or ranged tag by Title.
sdt = doc.range.structured_document_tags.get_by_title('Alias4')
print(sdt.id)
```

### See Also

* module [aspose.words.markup](../../)
* class [IStructuredDocumentTag](../)

