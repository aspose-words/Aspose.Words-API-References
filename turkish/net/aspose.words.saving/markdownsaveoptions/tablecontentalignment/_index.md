---
title: MarkdownSaveOptions.TableContentAlignment
linktitle: TableContentAlignment
articleTitle: TableContentAlignment
second_title: .NET için Aspose.Words
description: Sorunsuz Markdown dışa aktarımları için tablo içeriği hizalamasını özelleştirmek üzere MarkdownSaveOptions TableContentAlignment özelliğini keşfedin. Varsayılan Otomatik'tir.
type: docs
weight: 140
url: /tr/net/aspose.words.saving/markdownsaveoptions/tablecontentalignment/
---
## MarkdownSaveOptions.TableContentAlignment property

tables 'ye aktarırken içeriklerin nasıl hizalanacağını belirten bir değer alır veya ayarlar.Markdown format. Varsayılan değerAuto .

```csharp
public TableContentAlignment TableContentAlignment { get; set; }
```

## Örnekler

Tablolardaki içeriklerin nasıl hizalanacağını gösterir.

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

### Ayrıca bakınız

* enum [TableContentAlignment](../../tablecontentalignment/)
* class [MarkdownSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
