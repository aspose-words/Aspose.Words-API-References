---
title: TableContentAlignment Enum
linktitle: TableContentAlignment
articleTitle: TableContentAlignment
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Saving.TableContentAlignment-enum för exakt justering av tabellinnehåll i Markdown-exporter. Förbättra din dokumentformatering utan ansträngning!
type: docs
weight: 6420
url: /sv/net/aspose.words.saving/tablecontentalignment/
---
## TableContentAlignment enumeration

Gör det möjligt att ange justeringen av innehållet i tabellen som ska användas vid export till Markdown-format.

```csharp
public enum TableContentAlignment
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Auto | `0` | Justeringen kommer att hämtas från det första stycket i motsvarande tabellkolumn. |
| Left | `1` | Innehållet i tabellerna kommer att justeras till vänster. |
| Center | `2` | Innehållet i tabellerna kommer att justeras mot mitten. |
| Right | `3` | Innehållet i tabellerna kommer att justeras till höger. |

## Exempel

Visar hur man justerar innehåll i tabeller.

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
        Assert.AreEqual(ParagraphAlignment.Right,
            table.FirstRow.Cells[0].FirstParagraph.ParagraphFormat.Alignment);
        Assert.AreEqual(ParagraphAlignment.Center,
            table.FirstRow.Cells[1].FirstParagraph.ParagraphFormat.Alignment);
        break;
    case TableContentAlignment.Left:
        Assert.AreEqual(ParagraphAlignment.Left,
            table.FirstRow.Cells[0].FirstParagraph.ParagraphFormat.Alignment);
        Assert.AreEqual(ParagraphAlignment.Left,
            table.FirstRow.Cells[1].FirstParagraph.ParagraphFormat.Alignment);
        break;
    case TableContentAlignment.Center:
        Assert.AreEqual(ParagraphAlignment.Center,
            table.FirstRow.Cells[0].FirstParagraph.ParagraphFormat.Alignment);
        Assert.AreEqual(ParagraphAlignment.Center,
            table.FirstRow.Cells[1].FirstParagraph.ParagraphFormat.Alignment);
        break;
    case TableContentAlignment.Right:
        Assert.AreEqual(ParagraphAlignment.Right,
            table.FirstRow.Cells[0].FirstParagraph.ParagraphFormat.Alignment);
        Assert.AreEqual(ParagraphAlignment.Right,
            table.FirstRow.Cells[1].FirstParagraph.ParagraphFormat.Alignment);
        break;
}
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
