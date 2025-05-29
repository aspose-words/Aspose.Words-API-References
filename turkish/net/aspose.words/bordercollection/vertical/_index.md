---
title: BorderCollection.Vertical
linktitle: Vertical
articleTitle: Vertical
second_title: .NET için Aspose.Words
description: Kusursuz hücre sınırları için BorderCollection Vertical özelliğini keşfedin. Cilalı bir görünüm için tasarımınızı özelleştirilebilir dikey sınırlarla geliştirin!
type: docs
weight: 130
url: /tr/net/aspose.words/bordercollection/vertical/
---
## BorderCollection.Vertical property

Hücreler arasında kullanılan dikey kenarlığı alır.

```csharp
public Border Vertical { get; }
```

## Örnekler

Tablo satırının biçimine dikey kenarlık ayarlarının nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Kırmızı ve mavi iç kenarlıkları olan bir tablo oluşturun.
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

// Bir satır biçimi ve bir hücrenin iç paragrafı farklı kenarlık ayarları kullanır.
Border border = table.FirstRow.FirstCell.LastParagraph.ParagraphFormat.Borders.Vertical;

Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
Assert.AreEqual(0.0d, border.LineWidth);
Assert.AreEqual(LineStyle.None, border.LineStyle);

doc.Save(ArtifactsDir + "Border.VerticalBorders.docx");
```

### Ayrıca bakınız

* class [Border](../../border/)
* class [BorderCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
