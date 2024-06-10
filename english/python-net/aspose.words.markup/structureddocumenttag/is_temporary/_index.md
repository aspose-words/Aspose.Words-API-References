---
title: StructuredDocumentTag.is_temporary property
linktitle: is_temporary property
articleTitle: is_temporary property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.is_temporary property. Specifies whether this SDT shall be removed from the WordProcessingML document when its contents are modified."
type: docs
weight: 160
url: /python-net/aspose.words.markup/structureddocumenttag/is_temporary/
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
# Insert a plain text structured document tag,
# which will act as a plain text form that the user may enter text into.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Set the "is_temporary" property to "True" to make the structured document tag disappear and
# assimilate its contents into the document after the user edits it once in Microsoft Word.
# Set the "is_temporary" property to "False" to allow the user to edit the contents
# of the structured document tag any number of times.
tag.is_temporary = is_temporary
builder = aw.DocumentBuilder(doc)
builder.write('Please enter text: ')
builder.insert_node(tag)
# Insert another structured document tag in the form of a check box and set its default state to "checked".
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.CHECKBOX, aw.markup.MarkupLevel.INLINE)
tag.checked = True
# Set the "is_temporary" property to "True" to make the check box become a symbol
# once the user clicks on it in Microsoft Word.
# Set the "is_temporary" property to "False" to allow the user to click on the check box any number of times.
tag.is_temporary = is_temporary
builder.write('\nPlease click the check box: ')
builder.insert_node(tag)
doc.save(ARTIFACTS_DIR + 'StructuredDocumentTag.is_temporary.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

