---
title: IStructuredDocumentTag.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for Python
description: "IStructuredDocumentTag.title property. Specifies the friendly name associated with this SDT"
type: docs
weight: 140
url: /es/python-net/aspose.words.markup/istructureddocumenttag/title/
---

## IStructuredDocumentTag.title property

Specifies the friendly name associated with this **SDT**.
Can not be null.



```python
@property
def title(self) -> str:
    ...

@title.setter
def title(self, value: str):
    ...

```

### Examples

Shows how to get structured document tag.

```python
doc = aw.Document(file_name=MY_DIR + 'Structured document tags by id.docx')
# Obtener la etiqueta de documento estructurado por Id.
sdt = doc.range.structured_document_tags.get_by_id(1160505028)
print(sdt.is_multi_section)
print(sdt.title)
# Obtener la etiqueta de documento estructurado o la etiqueta con rango por Título.
sdt = doc.range.structured_document_tags.get_by_title('Alias4')
print(sdt.id)
```

### See Also

* module [aspose.words.markup](../../)
* class [IStructuredDocumentTag](../)

