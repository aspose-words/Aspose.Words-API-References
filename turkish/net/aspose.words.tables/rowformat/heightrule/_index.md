---
title: RowFormat.HeightRule
second_title: Aspose.Words for .NET API Referansı
description: RowFormat mülk. Tablo satırının yüksekliğini belirlemek için kuralı alır veya ayarlar.
type: docs
weight: 50
url: /tr/net/aspose.words.tables/rowformat/heightrule/
---
## RowFormat.HeightRule property

Tablo satırının yüksekliğini belirlemek için kuralı alır veya ayarlar.

```csharp
public HeightRule HeightRule { get; set; }
```

### Örnekler

Satırların bir belge oluşturucuyla nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// İkinci bir satır başlatın ve ardından yüksekliğini yapılandırın. Oluşturucu bu ayarları aşağıdakilere uygulayacaktır:
// geçerli satırın yanı sıra daha sonra oluşturacağı yeni satırlar.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// İlk satır dolgunun yeniden yapılandırılmasından etkilenmedi ve hala varsayılan değerleri koruyor.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

DocumentBuilder kullanılarak biçimlendirilmiş bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
table.LeftIndent = 20;

// Metin ve tablo görünümü için bazı biçimlendirme seçeneklerini ayarlayın.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// Belge oluşturucudaki biçimlendirme seçeneklerini yapılandırmak bunları uygulayacaktır
// imlecin bulunduğu geçerli hücreye/satıra,
// ve ayrıca bu oluşturucu kullanılarak oluşturulan yeni hücreler ve satırlar.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// Oluşturucunun biçimlendirme nesnelerini, yapmak üzere olduğumuz yeni satırlar ve hücreler için yeniden yapılandırın.
// Oluşturucu bunları zaten oluşturulmuş olan ilk satıra uygulamayacaktır, böylece başlık satırı olarak öne çıkacaktır.
builder.CellFormat.Shading.BackgroundPatternColor = Color.White;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.RowFormat.Height = 30;
builder.RowFormat.HeightRule = HeightRule.Auto;
builder.InsertCell();
builder.Font.Size = 12;
builder.Font.Bold = false;

builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");
builder.InsertCell();
builder.Write("Row 1, Cell 3.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.InsertCell();
builder.Write("Row 2, Cell 3.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateFormattedTable.docx");
```

### Ayrıca bakınız

* enum [HeightRule](../../../aspose.words/heightrule/)
* class [RowFormat](../)
* ad alanı [Aspose.Words.Tables](../../rowformat/)
* toplantı [Aspose.Words](../../../)


