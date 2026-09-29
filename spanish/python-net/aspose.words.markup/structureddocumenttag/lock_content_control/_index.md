---
title: StructuredDocumentTag.lock_content_control property
linktitle: lock_content_control property
articleTitle: lock_content_control property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.lock_content_control property. When set to ``True``, this property will prohibit a user from deleting this SDT."
type: docs
weight: 190
url: /es/python-net/aspose.words.markup/structureddocumenttag/lock_content_control/
---

## StructuredDocumentTag.lock_content_control property

When set to ``True``, this property will prohibit a user from deleting this **SDT**.



```python
@property
def lock_content_control(self) -> bool:
    ...

@lock_content_control.setter
def lock_content_control(self, value: bool):
    ...

```

### Examples

Shows how to apply editing restrictions to structured document tags.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserte una etiqueta de documento estructurado de texto plano, que actúa como un cuadro de texto que solicita al usuario que lo complete.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Establezca la propiedad "LockContents" en "true" para prohibir que el usuario edite el contenido de este cuadro de texto.
tag.lock_contents = True
builder.write('The contents of this structured document tag cannot be edited: ')
builder.insert_node(tag)
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Establezca la propiedad "LockContentControl" en "true" para prohibir que el usuario
# eliminar esta etiqueta de documento estructurado manualmente en Microsoft Word.
tag.lock_content_control = True
builder.insert_paragraph()
builder.write('This structured document tag cannot be deleted but its contents can be edited: ')
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.Lock.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

