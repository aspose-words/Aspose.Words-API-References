---
title: TableContentAlignment enumeration
linktitle: TableContentAlignment enumeration
articleTitle: TableContentAlignment enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.TableContentAlignment enumeration. Allows to specify the alignment of the content of the table to be used when exporting into Markdown format."
type: docs
weight: 810
url: /nodejs-net/aspose.words.saving/tablecontentalignment/
---

## TableContentAlignment enumeration

Allows to specify the alignment of the content of the table to be used when exporting into Markdown format.


### Members

| Name | Description |
| --- | --- |
| Auto | The alignment will be taken from the first paragraph in corresponding table column. |
| Left | The content of tables will be aligned to the Left. |
| Center | The content of tables will be aligned to the Center. |
| Right | The content of tables will be aligned to the Right. |

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

* module [Aspose.Words.Saving](../)

