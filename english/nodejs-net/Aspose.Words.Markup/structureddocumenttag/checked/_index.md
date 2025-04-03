---
title: StructuredDocumentTag.checked property
linktitle: checked property
articleTitle: checked property
second_title: Aspose.Words for NodeJs
description: "StructuredDocumentTag.checked property. Gets/Sets current state of the Checkbox SDT"
type: docs
weight: 60
url: /nodejs-net/Aspose.Words.Markup/structureddocumenttag/checked/
---

## StructuredDocumentTag.checked property

Gets/Sets current state of the Checkbox **SDT**.
Default value for this property is ``false``.



```js
get checked(): boolean
```

### Remarks

Accessing this property will only work for [SdtType.Checkbox](../../sdttype/#Checkbox)
SDT types.


For all other SDT types exception will occur.




### Examples

Show how to create a structured document tag in the form of a check box.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let sdtCheckBox = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.Checkbox, aw.Markup.MarkupLevel.Inline);
sdtCheckBox.checked = true;

// We can set the symbols used to represent the checked/unchecked state of a checkbox content control.
sdtCheckBox.setCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.setUncheckedSymbol(0x00AE, "Times New Roman");

builder.insertNode(sdtCheckBox);

doc.save(base.artifactsDir + "StructuredDocumentTag.checkBox.docx");
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTag](../)

