---
title: ImportFormatOptions.smartStyleBehavior property
linktitle: smartStyleBehavior property
articleTitle: smartStyleBehavior property
second_title: Aspose.Words for NodeJs
description: "ImportFormatOptions.smartStyleBehavior property. Gets or sets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents"
type: docs
weight: 80
url: /nodejs-net/Aspose.Words/importformatoptions/smartStyleBehavior/
---

## ImportFormatOptions.smartStyleBehavior property

Gets or sets a boolean value that specifies how styles will be imported
when they have equal names in source and destination documents.
The default value is ``false``.



```js
get smartStyleBehavior(): boolean
```

### Remarks

When this option is **enabled**, the source style will be expanded into a direct attributes inside a
destination document, if [ImportFormatMode.KeepSourceFormatting](../../importformatmode/#KeepSourceFormatting) importing mode is used.

When this option is **disabled**, the source style will be expanded only if it is numbered. Existing
destination attributes will not be overridden, including lists.




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

* module [Aspose.Words](../../)
* class [ImportFormatOptions](../)

