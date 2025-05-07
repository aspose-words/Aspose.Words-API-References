---
title: MarkdownExportAsHtml enumeration
linktitle: MarkdownExportAsHtml enumeration
articleTitle: MarkdownExportAsHtml enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.MarkdownExportAsHtml enumeration. Allows to specify the elements to be exported to Markdown as raw HTML."
type: docs
weight: 410
url: /nodejs-net/aspose.words.saving/markdownexportashtml/
---

## MarkdownExportAsHtml enumeration

Allows to specify the elements to be exported to Markdown as raw HTML.


### Members

| Name | Description |
| --- | --- |
| None | Export all elements using Markdown syntax without any raw HTML. |
| Tables | Export tables as raw HTML. |

### Examples

Shows how to export a table to Markdown as raw HTML.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Sample table:");

// Create table.
builder.insertCell();
builder.paragraphFormat.alignment = aw.ParagraphAlignment.Right;
builder.write("Cell1");
builder.insertCell();
builder.paragraphFormat.alignment = aw.ParagraphAlignment.Center;
builder.write("Cell2");

let saveOptions = new aw.Saving.MarkdownSaveOptions();
saveOptions.exportAsHtml = aw.Saving.MarkdownExportAsHtml.Tables;

doc.save(base.artifactsDir + "MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../)

