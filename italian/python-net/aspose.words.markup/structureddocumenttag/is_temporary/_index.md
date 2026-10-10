---
title: StructuredDocumentTag.is_temporary property
linktitle: is_temporary property
articleTitle: is_temporary property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.is_temporary property. Specifies whether this SDT shall be removed from the WordProcessingML document when its contents are modified."
type: docs
weight: 160
url: /it/python-net/aspose.words.markup/structureddocumenttag/is_temporary/
---

## StructuredDocumentTag.is_temporary property

Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents
are modified.



```python
@property
def is_temporary(self) -> bool:
    ...

@is_temporary.setter
def is_temporary(self, value: bool):
    ...

```

### Examples

Shows how to make single-use controls.

```python
doc = aw.Document()
# Inserisci un tag di documento strutturato di testo semplice,
# che fungerà da modulo di testo semplice in cui l'utente può inserire del testo.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Imposta la proprietà "IsTemporary" su "true" per far scomparire il tag di documento strutturato e
# assimila il suo contenuto nel documento dopo che l'utente lo modifica una volta in Microsoft Word.
# Imposta la proprietà "IsTemporary" su "false" per consentire all'utente di modificare il contenuto
# del tag di documento strutturato un numero qualsiasi di volte.
tag.is_temporary = is_temporary
builder = aw.DocumentBuilder(doc=doc)
builder.write('Please enter text: ')
builder.insert_node(tag)
# Inserisci un altro tag di documento strutturato sotto forma di casella di controllo e imposta il suo stato predefinito su "checked".
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.CHECKBOX, aw.markup.MarkupLevel.INLINE)
tag.checked = True
# Imposta la proprietà "IsTemporary" su "true" per far diventare la casella di controllo un simbolo
# una volta che l'utente fa clic su di essa in Microsoft Word.
# Imposta la proprietà "IsTemporary" su "false" per consentire all'utente di fare clic sulla casella di controllo un numero qualsiasi di volte.
tag.is_temporary = is_temporary
builder.write('\nPlease click the check box: ')
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.IsTemporary.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

