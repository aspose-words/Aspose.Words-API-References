---
title: BorderCollection.Bottom
second_title: Aspose.Words for .NET API Referansı
description: BorderCollection mülk. Alt kenarlığı alır.
type: docs
weight: 10
url: /tr/net/aspose.words/bordercollection/bottom/
---
## BorderCollection.Bottom property

Alt kenarlığı alır.

```csharp
public Border Bottom { get; }
```

### Örnekler

Tablo oluştururken kenarlık ve gölgelendirme renginin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir tablo başlatın ve sınırları için varsayılan bir renk/kalınlık ayarlayın.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Farklı arka plan renklerine sahip iki hücreli bir satır oluşturun.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Arka plan renklerini devre dışı bırakmak için hücre biçimlendirmesini sıfırlayın
// oluşturucu tarafından oluşturulan tüm yeni hücreler için özel bir kenarlık kalınlığı ayarlayın,
// sonra ikinci bir satır oluşturun.
builder.CellFormat.ClearFormatting();
builder.CellFormat.Borders.Left.LineWidth = 4.0;
builder.CellFormat.Borders.Right.LineWidth = 4.0;
builder.CellFormat.Borders.Top.LineWidth = 4.0;
builder.CellFormat.Borders.Bottom.LineWidth = 4.0;

builder.InsertCell();
builder.Writeln("Row 2, Cell 1.");
builder.InsertCell();
builder.Writeln("Row 2, Cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### Ayrıca bakınız

* class [Border](../../border/)
* class [BorderCollection](../)
* ad alanı [Aspose.Words](../../bordercollection/)
* toplantı [Aspose.Words](../../../)


