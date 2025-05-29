---
title: TableContentAlignment Enum
linktitle: TableContentAlignment
articleTitle: TableContentAlignment
second_title: .NET için Aspose.Words
description: Markdown dışa aktarımlarında hassas tablo içeriği hizalaması için Aspose.Words.Saving.TableContentAlignment enum'unu keşfedin. Belge biçimlendirmenizi zahmetsizce geliştirin!
type: docs
weight: 6420
url: /tr/net/aspose.words.saving/tablecontentalignment/
---
## TableContentAlignment enumeration

Markdown formatına aktarılırken kullanılacak tablonun içeriğinin hizalamasını belirtmeye olanak tanır.

```csharp
public enum TableContentAlignment
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Auto | `0` | Hizalama, ilgili tablo sütunundaki ilk paragraftan alınacaktır. |
| Left | `1` | Tabloların içeriği Sola hizalanacaktır. |
| Center | `2` | Tabloların içerikleri Ortaya hizalanacaktır. |
| Right | `3` | Tabloların içeriği Sağa hizalanacaktır. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
