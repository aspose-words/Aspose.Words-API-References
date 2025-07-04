---
title: MarkdownSaveOptions.TableContentAlignment
linktitle: TableContentAlignment
articleTitle: TableContentAlignment
second_title: Aspose.Words for .NET
description: Discover the MarkdownSaveOptions TableContentAlignment property to customize table content alignment for seamless Markdown exports. Default is Auto.
type: docs
weight: 140
url: /net/aspose.words.saving/markdownsaveoptions/tablecontentalignment/
---
## MarkdownSaveOptions.TableContentAlignment property

Gets or sets a value that specifies how to align contents in tables when exporting into the Markdown format. The default value is Auto.

```csharp
public TableContentAlignment TableContentAlignment { get; set; }
```

## Examples

Shows how to align contents in tables.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;
builder.Write("Cell1");
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write("Cell2");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions { TableContentAlignment = tableContentAlignment };

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md", saveOptions);

Document doc = new Document(ArtifactsDir + "MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md");
Table table = doc.FirstSection.Body.Tables[0];

switch (tableContentAlignment)
{
    case TableContentAlignment.Auto:
        Assert.That(table.FirstRow.Cells[0].FirstParagraph.ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Right));
        Assert.That(table.FirstRow.Cells[1].FirstParagraph.ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Center));
        break;
    case TableContentAlignment.Left:
        Assert.That(table.FirstRow.Cells[0].FirstParagraph.ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Left));
        Assert.That(table.FirstRow.Cells[1].FirstParagraph.ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Left));
        break;
    case TableContentAlignment.Center:
        Assert.That(table.FirstRow.Cells[0].FirstParagraph.ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Center));
        Assert.That(table.FirstRow.Cells[1].FirstParagraph.ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Center));
        break;
    case TableContentAlignment.Right:
        Assert.That(table.FirstRow.Cells[0].FirstParagraph.ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Right));
        Assert.That(table.FirstRow.Cells[1].FirstParagraph.ParagraphFormat.Alignment, Is.EqualTo(ParagraphAlignment.Right));
        break;
}
```

### See Also

* enum [TableContentAlignment](../../tablecontentalignment/)
* class [MarkdownSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
