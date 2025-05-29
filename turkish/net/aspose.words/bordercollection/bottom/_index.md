---
title: BorderCollection.Bottom
linktitle: Bottom
articleTitle: Bottom
second_title: .NET için Aspose.Words
description: Gelişmiş tasarım esnekliği ve stili için alt kenarlığınıza kolayca erişmek ve onu özelleştirmek amacıyla BorderCollection Bottom özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words/bordercollection/bottom/
---
## BorderCollection.Bottom property

Alt sınırı alır.

```csharp
public Border Bottom { get; }
```

## Örnekler

Bir tablo oluştururken kenarlık ve gölgelendirme renginin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir tablo başlatın ve kenarlıkları için varsayılan bir renk/kalınlık ayarlayın.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Farklı arka plan renklerine sahip iki hücreden oluşan bir satır oluştur.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Arka plan renklerini devre dışı bırakmak için hücre biçimlendirmesini sıfırlayın
// Oluşturucu tarafından oluşturulan tüm yeni hücreler için özel bir kenarlık kalınlığı ayarlayın,
// daha sonra ikinci bir satır oluştur.
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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
