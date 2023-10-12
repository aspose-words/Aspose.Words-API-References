---
title: Table.SetBorders
second_title: Aspose.Words for .NET API Referansı
description: Table yöntem. Tüm tablo kenarlıklarını belirtilen çizgi stiline genişliğine ve rengine ayarlar.
type: docs
weight: 440
url: /tr/net/aspose.words.tables/table/setborders/
---
## Table.SetBorders method

Tüm tablo kenarlıklarını belirtilen çizgi stiline, genişliğine ve rengine ayarlar.

```csharp
public void SetBorders(LineStyle lineStyle, double lineWidth, Color color)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| lineStyle | LineStyle | Uygulanacak çizgi stili. |
| lineWidth | Double | Ayarlanacak çizgi genişliği (nokta cinsinden). |
| color | Color | Kenarlık için kullanılacak renk. |

### Örnekler

Bir tablonun tüm kenarlarının aynı anda nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

//Tablodaki mevcut tüm sınırları temizleyin.
table.ClearBorders();

// Bu tablonun her dış ve iç kenarlığı olarak hizmet edecek tek bir yeşil çizgi ayarlayın.
table.SetBorders(LineStyle.Single, 1.5, Color.Green);

doc.Save(ArtifactsDir + "Table.SetBorders.docx");
```

Tablo oluştururken kenarlık ve gölgeleme renginin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir tablo başlatın ve kenarlıkları için varsayılan rengi/kalınlığı ayarlayın.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Farklı arka plan renklerine sahip iki hücreden oluşan bir satır oluşturun.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Arka plan renklerini devre dışı bırakmak için hücre biçimlendirmesini sıfırlayın
// oluşturucu tarafından oluşturulan tüm yeni hücreler için özel bir kenar kalınlığı ayarlayın,
// sonra ikinci satırı oluşturalım.
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

* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../table/)
* toplantı [Aspose.Words](../../../)


