---
title: StructuredDocumentTag.checked property
linktitle: checked property
articleTitle: checked property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.checked property. Gets/Sets current state of the Checkbox SDT"
type: docs
weight: 60
url: /python-net/aspose.words.markup/structureddocumenttag/checked/
---

## StructuredDocumentTag.checked property

Gets/Sets current state of the Checkbox **SDT**.
Default value for this property is ``False``.


Accessing this property will only work for [SdtType.CHECKBOX](../../sdttype/#CHECKBOX)
SDT types.


For all other SDT types exception will occur.




### Examples

Show how to create a structured document tag in the form of a check box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

sdt_check_box = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.CHECKBOX, aw.markup.MarkupLevel.INLINE)
sdt_check_box.checked = True

# We can set the symbols used to represent the checked/unchecked state of a checkbox content control.
sdt_check_box.set_checked_symbol(0x00A9, "Times New Roman")
sdt_check_box.set_unchecked_symbol(0x00AE, "Times New Roman")

builder.insert_node(sdt_check_box)

doc.save(ARTIFACTS_DIR + "StructuredDocumentTag.check_box.docx")
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

