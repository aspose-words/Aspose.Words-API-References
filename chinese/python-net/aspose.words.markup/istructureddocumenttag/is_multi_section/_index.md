---
title: IStructuredDocumentTag.is_multi_section property
linktitle: is_multi_section property
articleTitle: is_multi_section property
second_title: Aspose.Words for Python
description: "IStructuredDocumentTag.is_multi_section property. Returns true if this instance is a ranged (multi-section) structured document tag."
type: docs
weight: 40
url: /zh/python-net/aspose.words.markup/istructureddocumenttag/is_multi_section/
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
* class [IStructuredDocumentTag](../)

