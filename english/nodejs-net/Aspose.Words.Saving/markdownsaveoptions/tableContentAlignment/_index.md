---
title: MarkdownSaveOptions.tableContentAlignment property
linktitle: tableContentAlignment property
articleTitle: tableContentAlignment property
second_title: Aspose.Words for Node.js
description: "MarkdownSaveOptions.tableContentAlignment property. Gets or sets a value that specifies how to align contents in tables when exporting into the [SaveFormat.Markdown](../../../aspose.words/saveformat/#Markdown) format"
type: docs
weight: 140
url: /nodejs-net/aspose.words.saving/markdownsaveoptions/tableContentAlignment/
---

## MarkdownSaveOptions.tableContentAlignment property

Gets or sets a value that specifies how to align contents in tables
when exporting into the [SaveFormat.Markdown](../../../aspose.words/saveformat/#Markdown) format.
The default value is [TableContentAlignment.Auto](../../tablecontentalignment/#Auto).



```js
get tableContentAlignment(): Aspose.Words.Saving.TableContentAlignment
```

### Examples

Shows how to align contents in tables.

```js
let builder = new aw.DocumentBuilder();

builder.insertCell();
builder.paragraphFormat.alignment = aw.ParagraphAlignment.Right;
builder.write("Cell1");
builder.insertCell();
builder.paragraphFormat.alignment = aw.ParagraphAlignment.Center;
builder.write("Cell2");

let saveOptions = new aw.Saving.MarkdownSaveOptions { TableContentAlignment = tableContentAlignment };

builder.document.save(base.artifactsDir + "MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md", saveOptions);

let doc = new aw.Document(base.artifactsDir + "MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md");
let table = doc.firstSection.body.tables.at(0);

switch (tableContentAlignment)
{
  case aw.Saving.TableContentAlignment.Auto:
    expect(table.firstRow.cells.at(0).firstParagraph.paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Right);
    expect(table.firstRow.cells.at(1).firstParagraph.paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Center);
    break;
  case aw.Saving.TableContentAlignment.Left:
    expect(table.firstRow.cells.at(0).firstParagraph.paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Left);
    expect(table.firstRow.cells.at(1).firstParagraph.paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Left);
    break;
  case aw.Saving.TableContentAlignment.Center:
    expect(table.firstRow.cells.at(0).firstParagraph.paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Center);
    expect(table.firstRow.cells.at(1).firstParagraph.paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Center);
    break;
  case aw.Saving.TableContentAlignment.Right:
    expect(table.firstRow.cells.at(0).firstParagraph.paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Right);
    expect(table.firstRow.cells.at(1).firstParagraph.paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Right);
    break;
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [MarkdownSaveOptions](../)

