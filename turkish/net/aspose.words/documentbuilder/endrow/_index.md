---
title: EndRow
second_title: Aspose.Words for .NET API Referansı
description: Belgedeki bir tablo satırını sonlandırır.
type: docs
weight: 220
url: /tr/net/aspose.words/documentbuilder/endrow/
---
## DocumentBuilder.EndRow method

Belgedeki bir tablo satırını sonlandırır.

```csharp
public Row EndRow()
```

### Geri dönüş değeri

Yeni biten satır düğümü.

### Notlar

Telefon etmek **EndRow** bir tablo satırını bitirmek için. eğer ararsan[`InsertCell`](../insertcell) hemen sonra tablo yeni bir satırda devam eder.

Kullan[`RowFormat`](../rowformat) satır biçimlendirmesini belirtmek için özellik.

### Örnekler

Tablo hücrelerinin dikey olarak nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İlk satırın ilk sütununa bir hücre ekleyin.
// Bu hücre, dikey olarak birleştirilmiş hücre aralığındaki ilk hücre olacaktır.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// İlk satırın ikinci sütununa bir hücre ekleyin, ardından satırı bitirin.
// Ayrıca, oluşturucuyu oluşturulan hücrelerde dikey birleştirmeyi devre dışı bırakacak şekilde yapılandırın.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

// İkinci satırın ilk sütununa bir hücre ekleyin. 
// Metin içeriği eklemek yerine, bu hücreyi doğrudan yukarıda eklediğimiz ilk hücreyle birleştireceğiz.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// İkinci satırın ikinci sütununa başka bir bağımsız hücre ekle.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.VerticalMerge.docx");
```

Biçimlendirilmiş bir 2x2 tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// Tabloyu oluştururken, belge oluşturucu mevcut RowFormat/CellFormat özellik değerlerini uygulayacaktır
// imlecinin içinde bulunduğu geçerli satıra/hücreye ve bunları oluştururken yeni satırlara/hücrelere.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Önceden eklenen satırlar ve hücreler, oluşturucunun biçimlendirmesindeki değişikliklerden geriye dönük olarak etkilenmez.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

Özel kenarlıklı bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Bir belge oluşturucu için tablo biçimlendirme seçeneklerini ayarlama
// onları eklediğimiz her satıra ve hücreye uygulayacak.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// Biçimlendirmeyi değiştirmek, onu geçerli hücreye uygular,
// ve daha sonra oluşturucu ile oluşturduğumuz yeni hücreler.
// Bu daha önce eklediğimiz hücreleri etkilemeyecektir.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Dikey metne sığdırmak için satır yüksekliğini artırın.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### Ayrıca bakınız

* class [Row](../../../aspose.words.tables/row)
* class [DocumentBuilder](../../documentbuilder)
* ad alanı [Aspose.Words](../../documentbuilder)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
