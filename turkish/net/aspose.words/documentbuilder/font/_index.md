---
title: DocumentBuilder.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words for .NET
description: DocumentBuilder Font mülk. Geçerli yazı tipi biçimlendirme özelliklerini temsil eden bir nesneyi döndürür C#'da.
type: docs
weight: 100
url: /tr/net/aspose.words/documentbuilder/font/
---
## DocumentBuilder.Font property

Geçerli yazı tipi biçimlendirme özelliklerini temsil eden bir nesneyi döndürür.

```csharp
public Font Font { get; }
```

## Notlar

Kullanmak`Font` yazı tipi biçimlendirme özelliklerine erişmek ve bunları değiştirmek için.

Metin eklemeden önce yazı tipi formatını belirtin.

## Örnekler

Kenarlıkla çevrelenmiş bir dizenin belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
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

* class [Font](../../font/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
