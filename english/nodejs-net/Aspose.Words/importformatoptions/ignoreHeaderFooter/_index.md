---
title: ImportFormatOptions.ignoreHeaderFooter property
linktitle: ignoreHeaderFooter property
articleTitle: ignoreHeaderFooter property
second_title: Aspose.Words for NodeJs
description: "ImportFormatOptions.ignoreHeaderFooter property. Gets or sets a boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KeepSourceFormatting](../../importformatmode/#KeepSourceFormatting) mode is used"
type: docs
weight: 40
url: /nodejs-net/Aspose.Words/importformatoptions/ignoreHeaderFooter/
---

## ImportFormatOptions.ignoreHeaderFooter property

Gets or sets a boolean value that specifies that source formatting of headers/footers content ignored
if [ImportFormatMode.KeepSourceFormatting](../../importformatmode/#KeepSourceFormatting) mode is used.
The default value is ``True``.



```js
get ignoreHeaderFooter(): boolean
```

### Examples

Shows how to specifies ignoring or not source formatting of headers/footers content.

```js
let dstDoc = new aw.Document(base.myDir + "Document.docx");
let srcDoc = new aw.Document(base.myDir + "Header and footer types.docx");

let importFormatOptions = new aw.ImportFormatOptions();
importFormatOptions.ignoreHeaderFooter = false;

dstDoc.appendDocument(srcDoc, aw.ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.save(base.artifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [ImportFormatOptions](../)

