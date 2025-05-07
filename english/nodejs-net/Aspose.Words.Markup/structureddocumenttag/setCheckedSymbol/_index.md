---
title: StructuredDocumentTag.setCheckedSymbol method
linktitle: setCheckedSymbol method
articleTitle: setCheckedSymbol method
second_title: Aspose.Words for Node.js
description: "StructuredDocumentTag.setCheckedSymbol method. Sets the symbol used to represent the checked state of a check box content control."
type: docs
weight: 350
url: /nodejs-net/aspose.words.markup/structureddocumenttag/setCheckedSymbol/
---

## setCheckedSymbol(characterCode, fontName) {#number_string}

Sets the symbol used to represent the checked state of a check box content control.


```js
setCheckedSymbol(characterCode: number, fontName: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| characterCode | number | The character code for the specified symbol. |
| fontName | string | The name of the font that contains the symbol. |

### Remarks

Accessing this method will only work for [SdtType.Checkbox](../../sdttype/#Checkbox) SDT types.

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

