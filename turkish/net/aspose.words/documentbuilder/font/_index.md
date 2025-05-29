---
title: DocumentBuilder.Font
linktitle: Font
articleTitle: Font
second_title: .NET için Aspose.Words
description: Mevcut yazı tipi biçimlendirmenize zahmetsizce erişmek ve özelleştirmek için DocumentBuilder Font özelliğini keşfedin. Belgenizin stilini bugün geliştirin!
type: docs
weight: 100
url: /tr/net/aspose.words/documentbuilder/font/
---
## DocumentBuilder.Font property

Geçerli yazı tipi biçimlendirme özelliklerini temsil eden bir nesne döndürür.

```csharp
public Font Font { get; }
```

## Notlar

Kullanmak`Font` yazı tipi biçimlendirme özelliklerine erişmek ve bunları değiştirmek için.

Metni eklemeden önce yazı tipi biçimlendirmesini belirtin.

## Örnekler

Bir belgeye kenarlıkla çevrili bir dizenin nasıl ekleneceğini gösterir.

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

// Metin ve tablo görünümü için bazı biçimlendirme seçenekleri ayarlayın.
builder.RowFormat.Height = 40;
builder.RowFormat.HeightRule = HeightRule.AtLeast;
builder.CellFormat.Shading.BackgroundPatternColor = Color.FromArgb(198, 217, 241);

builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Font.Size = 16;
builder.Font.Name = "Arial";
builder.Font.Bold = true;

// Bir belge oluşturucuda biçimlendirme seçeneklerinin yapılandırılması bunları uygular
// imlecin bulunduğu geçerli hücreye/satıra,
// ve bu oluşturucu kullanılarak oluşturulan tüm yeni hücreler ve satırlar.
builder.Write("Header Row,\n Cell 1");
builder.InsertCell();
builder.Write("Header Row,\n Cell 2");
builder.InsertCell();
builder.Write("Header Row,\n Cell 3");
builder.EndRow();

// Oluşturmak üzere olduğumuz yeni satırlar ve hücreler için oluşturucunun biçimlendirme nesnelerini yeniden yapılandırın.
// Oluşturucu bunları daha önceden oluşturulmuş ilk satıra uygulamayacak, böylece bu satır başlık satırı olarak öne çıkacaktır.
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
