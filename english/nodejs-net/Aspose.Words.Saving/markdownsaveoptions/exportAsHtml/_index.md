---
title: MarkdownSaveOptions.exportAsHtml property
linktitle: exportAsHtml property
articleTitle: exportAsHtml property
second_title: Aspose.Words for Node.js
description: "MarkdownSaveOptions.exportAsHtml property. Allows to specify the elements to be exported to Markdown as raw HTML"
type: docs
weight: 30
url: /nodejs-net/aspose.words.saving/markdownsaveoptions/exportAsHtml/
---

## MarkdownSaveOptions.exportAsHtml property

Allows to specify the elements to be exported to Markdown as raw HTML.
Default value is [MarkdownExportAsHtml.None](../../markdownexportashtml/#None).



```js
get exportAsHtml(): Aspose.Words.Saving.MarkdownExportAsHtml
```

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

* module [Aspose.Words.Saving](../../)
* class [MarkdownSaveOptions](../)

