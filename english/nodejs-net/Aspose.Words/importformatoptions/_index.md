---
title: ImportFormatOptions class
linktitle: ImportFormatOptions class
articleTitle: ImportFormatOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.ImportFormatOptions class. Allows to specify various import options to format output"
type: docs
weight: 630
url: /nodejs-net/aspose.words/importformatoptions/
---

## ImportFormatOptions class

Allows to specify various import options to format output.
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/nodejs-net/specify-load-options/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [ImportFormatOptions()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [adjustSentenceAndWordSpacing](./adjustSentenceAndWordSpacing/) | Gets or sets a boolean value that specifies whether to adjust sentence and word spacing automatically. The default value is ``false``. |
| [forceCopyStyles](./forceCopyStyles/) | Gets or sets a boolean value indicating either to copy conflicting styles in [ImportFormatMode.KeepSourceFormatting](../importformatmode/#KeepSourceFormatting) mode. The default value is ``false``. |
| [ignoreHeaderFooter](./ignoreHeaderFooter/) | Gets or sets a boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KeepSourceFormatting](../importformatmode/#KeepSourceFormatting) mode is used. The default value is ``true``. |
| [ignoreTextBoxes](./ignoreTextBoxes/) | Gets or sets a boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KeepSourceFormatting](../importformatmode/#KeepSourceFormatting) mode is used. The default value is ``true``. |
| [keepSourceNumbering](./keepSourceNumbering/) | Gets or sets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. The default value is ``false``. |
| [mergePastedLists](./mergePastedLists/) | Gets or sets a boolean value that specifies whether pasted lists will be merged with surrounding lists. The default value is ``false``. |
| [smartStyleBehavior](./smartStyleBehavior/) | Gets or sets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents. The default value is ``false``. |

### Examples

Shows how to resolve duplicate styles while inserting documents.

```js
let dstDoc = new aw.Document();
let builder = new aw.DocumentBuilder(dstDoc);

let myStyle = builder.document.styles.add(aw.StyleType.Paragraph, "MyStyle");
myStyle.font.size = 14;
myStyle.font.name = "Courier New";
myStyle.font.color = "#0000FF";

builder.paragraphFormat.styleName = myStyle.name;
builder.writeln("Hello world!");

// Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
// If we insert the clone into the original document, the two styles with the same name will cause a clash.
let srcDoc = dstDoc.clone(); // TODO cast to Document
srcDoc.styles.at("MyStyle").font.color = "#FF0000";

// When we enable SmartStyleBehavior and use the KeepSourceFormatting import format mode,
// Aspose.words will resolve style clashes by converting source document styles.
// with the same names as destination styles into direct paragraph attributes.
let options = new aw.ImportFormatOptions();
options.smartStyleBehavior = true;

builder.insertDocument(srcDoc, aw.ImportFormatMode.KeepSourceFormatting, options);

dstDoc.save(base.artifactsDir + "DocumentBuilder.smartStyleBehavior.docx");
```

### See Also

* module [Aspose.Words](../)

