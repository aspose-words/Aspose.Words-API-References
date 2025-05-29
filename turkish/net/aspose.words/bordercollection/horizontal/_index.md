---
title: BorderCollection.Horizontal
linktitle: Horizontal
articleTitle: Horizontal
second_title: .NET için Aspose.Words
description: Sorunsuz hücre ve paragraf kenarlıkları için BorderCollection Yatay özelliğini keşfedin. Mükemmel hizalama ve stil ile düzeninizi geliştirin!
type: docs
weight: 50
url: /tr/net/aspose.words/bordercollection/horizontal/
---
## BorderCollection.Horizontal property

Hücreler veya uyumlu paragraflar arasında kullanılan yatay kenarlığı alır.

```csharp
public Border Horizontal { get; }
```

## Örnekler

Bir paragrafın biçimine yatay kenarlık ayarlarının nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Paragraf için kırmızı yatay bir kenarlık oluştur. Daha sonra oluşturulan tüm paragraflar bu kenarlık ayarlarını devralacaktır.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
borders.Horizontal.Color = Color.Red;
borders.Horizontal.LineStyle = LineStyle.DashSmallGap;
borders.Horizontal.LineWidth = 3;

// Sonrasında yeni bir paragraf oluşturmadan belgeye metin yaz.
// Altında paragraf olmadığı için yatay kenarlık görünmeyecektir.
builder.Write("Paragraph above horizontal border.");

// İkinci paragrafı eklediğimizde ilk paragrafın sınırı görünür hale gelecektir.
builder.InsertParagraph();
builder.Write("Paragraph below horizontal border.");

doc.Save(ArtifactsDir + "Border.HorizontalBorders.docx");
```

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
