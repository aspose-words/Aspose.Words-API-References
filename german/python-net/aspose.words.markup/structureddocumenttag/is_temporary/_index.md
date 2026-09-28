---
title: StructuredDocumentTag.is_temporary property
linktitle: is_temporary property
articleTitle: is_temporary property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.is_temporary property. Specifies whether this SDT shall be removed from the WordProcessingML document when its contents are modified."
type: docs
weight: 160
url: /de/python-net/aspose.words.markup/structureddocumenttag/is_temporary/
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
# Fügen Sie ein strukturiertes Dokument-Tag für Klartext ein,
# das als Klartextformular dient, in das der Benutzer Text eingeben kann.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Setzen Sie die Eigenschaft "IsTemporary" auf "true", um das strukturierte Dokument-Tag verschwinden zu lassen und
# übernehmen Sie dessen Inhalt in das Dokument, nachdem der Benutzer es einmal in Microsoft Word bearbeitet hat.
# Setzen Sie die Eigenschaft "IsTemporary" auf "false", um dem Benutzer zu erlauben, den Inhalt zu bearbeiten
# des strukturierten Dokument-Tags beliebig oft.
tag.is_temporary = is_temporary
builder = aw.DocumentBuilder(doc=doc)
builder.write('Please enter text: ')
builder.insert_node(tag)
# Fügen Sie ein weiteres strukturiertes Dokument-Tag in Form einer Checkbox ein und setzen Sie dessen Standardzustand auf "checked".
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.CHECKBOX, aw.markup.MarkupLevel.INLINE)
tag.checked = True
# Setzen Sie die Eigenschaft "IsTemporary" auf "true", um die Checkbox zu einem Symbol zu machen
# sobald der Benutzer darauf in Microsoft Word klickt.
# Setzen Sie die Eigenschaft "IsTemporary" auf "false", um dem Benutzer zu erlauben, die Checkbox beliebig oft anzuklicken.
tag.is_temporary = is_temporary
builder.write('\nPlease click the check box: ')
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.IsTemporary.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

