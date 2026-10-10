---
title: StructuredDocumentTag.is_temporary property
linktitle: is_temporary property
articleTitle: is_temporary property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.is_temporary property. Specifies whether this SDT shall be removed from the WordProcessingML document when its contents are modified."
type: docs
weight: 160
url: /sv/python-net/aspose.words.markup/structureddocumenttag/is_temporary/
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
# Infoga ett strukturerat dokumenttagg med vanlig text,
# som kommer att fungera som ett vanligt textformulär som användaren kan skriva in text i.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Ställ in egenskapen "IsTemporary" till "true" för att få den strukturerade dokumenttaggen att försvinna och
# integrera dess innehåll i dokumentet efter att användaren har redigerat det en gång i Microsoft Word.
# Ställ in egenskapen "IsTemporary" till "false" för att tillåta användaren att redigera innehållet
# i den strukturerade dokumenttaggen hur många gånger som helst.
tag.is_temporary = is_temporary
builder = aw.DocumentBuilder(doc=doc)
builder.write('Please enter text: ')
builder.insert_node(tag)
# Infoga en annan strukturerad dokumenttagg i form av en kryssruta och sätt dess standardtillstånd till "checked".
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.CHECKBOX, aw.markup.MarkupLevel.INLINE)
tag.checked = True
# Ställ in egenskapen "IsTemporary" till "true" för att få kryssrutan att bli en symbol
# när användaren klickar på den i Microsoft Word.
# Ställ in egenskapen "IsTemporary" till "false" för att tillåta användaren att klicka på kryssrutan hur många gånger som helst.
tag.is_temporary = is_temporary
builder.write('\nPlease click the check box: ')
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.IsTemporary.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

