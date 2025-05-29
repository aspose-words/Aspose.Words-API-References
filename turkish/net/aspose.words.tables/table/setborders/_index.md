---
title: Table.SetBorders
linktitle: SetBorders
articleTitle: SetBorders
second_title: .NET için Aspose.Words
description: SetBorders yöntemiyle tablolarınızı zahmetsizce özelleştirin; çizgi stilini, genişliğini ve rengini ayarlayarak cilalı, profesyonel bir görünüm elde edin.
type: docs
weight: 440
url: /tr/net/aspose.words.tables/table/setborders/
---
## Table.SetBorders method

Tüm tablo kenarlıklarını belirtilen çizgi stiline, genişliğe ve renge ayarlar.

```csharp
public void SetBorders(LineStyle lineStyle, double lineWidth, Color color)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| lineStyle | LineStyle | Uygulanacak çizgi stili. |
| lineWidth | Double | Ayarlanacak çizgi genişliği (puan cinsinden). |
| color | Color | Kenarlık için kullanılacak renk. |

## Örnekler

Bir tablonun tüm kenarlıklarının aynı anda nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Tablodaki tüm mevcut sınırları temizle.
table.ClearBorders();

// Bu tablonun her dış ve iç kenarlığını oluşturacak tek bir yeşil çizgi ayarlayın.
table.SetBorders(LineStyle.Single, 1.5, Color.Green);

doc.Save(ArtifactsDir + "Table.SetBorders.docx");
```

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

* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
