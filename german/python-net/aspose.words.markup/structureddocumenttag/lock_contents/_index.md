---
title: StructuredDocumentTag.lock_contents property
linktitle: lock_contents property
articleTitle: lock_contents property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.lock_contents property. When set to ``True``, this property will prohibit a user from editing the contents of this SDT."
type: docs
weight: 200
url: /de/python-net/aspose.words.markup/structureddocumenttag/lock_contents/
---

## StructuredDocumentTag.lock_contents property

When set to ``True``, this property will prohibit a user from editing the contents of this **SDT**.



```python
@property
def lock_contents(self) -> bool:
    ...

@lock_contents.setter
def lock_contents(self, value: bool):
    ...

```

### Examples

Shows how to apply editing restrictions to structured document tags.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie ein strukturiertes Dokument-Tag für Klartext ein, das als Textfeld fungiert und den Benutzer auffordert, es auszufüllen.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Setzen Sie die Eigenschaft "LockContents" auf "true", um dem Benutzer das Bearbeiten des Inhalts dieses Textfelds zu untersagen.
tag.lock_contents = True
builder.write('The contents of this structured document tag cannot be edited: ')
builder.insert_node(tag)
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Setzen Sie die Eigenschaft "LockContentControl" auf "true", um dem Benutzer zu verbieten,
# dieses strukturierte Dokument-Tag manuell in Microsoft Word zu löschen.
tag.lock_content_control = True
builder.insert_paragraph()
builder.write('This structured document tag cannot be deleted but its contents can be edited: ')
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.Lock.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

