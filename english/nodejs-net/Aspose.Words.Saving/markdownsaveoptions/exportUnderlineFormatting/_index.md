---
title: MarkdownSaveOptions.exportUnderlineFormatting property
linktitle: exportUnderlineFormatting property
articleTitle: exportUnderlineFormatting property
second_title: Aspose.Words for Node.js
description: "MarkdownSaveOptions.exportUnderlineFormatting property. Gets or sets a boolean value indicating either to export underline text formatting as sequence of two plus characters ++"
type: docs
weight: 40
url: /nodejs-net/aspose.words.saving/markdownsaveoptions/exportUnderlineFormatting/
---

## MarkdownSaveOptions.exportUnderlineFormatting property

Gets or sets a boolean value indicating either to export underline
text formatting as sequence of two plus characters "++".
The default value is ``false``.



```js
get exportUnderlineFormatting(): boolean
```

### Examples

Shows how to export underline formatting as ++.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.underline = aw.Underline.Single;
builder.write("Lorem ipsum. Dolor sit amet.");

let saveOptions = new aw.Saving.MarkdownSaveOptions() { ExportUnderlineFormatting = true };
doc.save(base.artifactsDir + "MarkdownSaveOptions.exportUnderlineFormatting.md", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [MarkdownSaveOptions](../)

