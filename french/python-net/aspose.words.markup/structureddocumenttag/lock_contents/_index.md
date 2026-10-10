---
title: StructuredDocumentTag.lock_contents property
linktitle: lock_contents property
articleTitle: lock_contents property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.lock_contents property. When set to ``True``, this property will prohibit a user from editing the contents of this SDT."
type: docs
weight: 200
url: /fr/python-net/aspose.words.markup/structureddocumenttag/lock_contents/
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
# Insérez une balise de document structuré en texte brut, qui agit comme une zone de texte invitant l'utilisateur à la remplir.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Définissez la propriété "LockContents" sur "true" pour empêcher l'utilisateur de modifier le contenu de cette zone de texte.
tag.lock_contents = True
builder.write('The contents of this structured document tag cannot be edited: ')
builder.insert_node(tag)
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Définissez la propriété "LockContentControl" sur "true" pour empêcher l'utilisateur de
# supprimer manuellement cette balise de document structuré dans Microsoft Word.
tag.lock_content_control = True
builder.insert_paragraph()
builder.write('This structured document tag cannot be deleted but its contents can be edited: ')
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.Lock.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

