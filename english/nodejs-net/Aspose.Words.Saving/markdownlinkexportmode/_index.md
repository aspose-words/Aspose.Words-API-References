---
title: MarkdownLinkExportMode enumeration
linktitle: MarkdownLinkExportMode enumeration
articleTitle: MarkdownLinkExportMode enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.MarkdownLinkExportMode enumeration. Specifies how links are exported into Markdown."
type: docs
weight: 430
url: /nodejs-net/aspose.words.saving/markdownlinkexportmode/
---

## MarkdownLinkExportMode enumeration

Specifies how links are exported into Markdown.


### Members

| Name | Description |
| --- | --- |
| Auto | Automatically detect export mode for each link. |
| Inline | Export all links as inline blocks. |
| Reference | Export all links as reference blocks. |

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

* module [Aspose.Words.Saving](../)

