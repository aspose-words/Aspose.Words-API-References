---
title: Table.LeftIndent
second_title: Aspose.Words for .NET API Referansı
description: Table mülk. Tablonun sol girintisini temsil eden değeri alır veya ayarlar.
type: docs
weight: 190
url: /tr/net/aspose.words.tables/table/leftindent/
---
## Table.LeftIndent property

Tablonun sol girintisini temsil eden değeri alır veya ayarlar.

```csharp
public double LeftIndent { get; set; }
```

### Örnekler

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

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../table/)
* toplantı [Aspose.Words](../../../)


