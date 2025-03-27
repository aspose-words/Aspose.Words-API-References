---
title: MarkdownSaveOptions.linkExportMode property
linktitle: linkExportMode property
articleTitle: linkExportMode property
second_title: Aspose.Words for NodeJs
description: "MarkdownSaveOptions.linkExportMode property. Specifies how links will be written to the output file"
type: docs
weight: 90
url: /nodejs-net/Aspose.Words.Saving/markdownsaveoptions/linkExportMode/
---

## MarkdownSaveOptions.linkExportMode property

Specifies how links will be written to the output file.
Default value is [MarkdownLinkExportMode.Auto](../../markdownlinkexportmode/#Auto).



```js
get linkExportMode(): Aspose.Words.Saving.MarkdownLinkExportMode
```

### Examples

Shows how to links will be written to the .md file.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.insertShape(aw.Drawing.ShapeType.Balloon, 100, 100);

// Image will be written as reference:
// ![ref1]
//
// [ref1]: aw_ref.001.png
let saveOptions = new aw.Saving.MarkdownSaveOptions();
saveOptions.linkExportMode = aw.Saving.MarkdownLinkExportMode.Reference;
doc.save(base.artifactsDir + "MarkdownSaveOptions.linkExportMode.reference.md", saveOptions);

// Image will be written as inline:
// ![](aw_inline.001.png)
saveOptions.linkExportMode = aw.Saving.MarkdownLinkExportMode.Inline;
doc.save(base.artifactsDir + "MarkdownSaveOptions.linkExportMode.inline.md", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [MarkdownSaveOptions](../)

