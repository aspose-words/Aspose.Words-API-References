---
title: Cell.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words for .NET
description: Cell LastParagraph mülk. Hemen alt öğeler arasındaki son paragrafı alır C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words.tables/cell/lastparagraph/
---
## Cell.LastParagraph property

Hemen alt öğeler arasındaki son paragrafı alır.

```csharp
public Paragraph LastParagraph { get; }
```

## Örnekler

Ayarların dikey kenarlıklara bir tablo satırı biçimine nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Kırmızı ve mavi iç kenarlıklara sahip bir tablo oluşturun.
Table table = builder.StartTable();

for (int i = 0; i < 3; i++)
{
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 1");
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 2");

    Row row = builder.EndRow();
    BorderCollection borders = row.RowFormat.Borders;

    // Satırlar arasında görünecek kenarlıkların görünümünü ayarlayın.
    borders.Horizontal.Color = Color.Red;
    borders.Horizontal.LineStyle = LineStyle.Dot;
    borders.Horizontal.LineWidth = 2.0d;

    // Hücreler arasında görünecek kenarlıkların görünümünü ayarlayın.
    borders.Vertical.Color = Color.Blue;
    borders.Vertical.LineStyle = LineStyle.Dot;
    borders.Vertical.LineWidth = 2.0d;
}

// Bir satır biçimi ve hücrenin iç paragrafı farklı kenarlık ayarları kullanır.
Border border = table.FirstRow.FirstCell.LastParagraph.ParagraphFormat.Borders.Vertical;

Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
Assert.AreEqual(0.0d, border.LineWidth);
Assert.AreEqual(LineStyle.None, border.LineStyle);

doc.Save(ArtifactsDir + "Border.VerticalBorders.docx");
```

### Ayrıca bakınız

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Cell](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
