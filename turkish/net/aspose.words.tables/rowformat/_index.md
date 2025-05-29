---
title: RowFormat Class
linktitle: RowFormat
articleTitle: RowFormat
second_title: .NET için Aspose.Words
description: Kapsamlı tablo satır biçimlendirmesi için Aspose.Words.Tables.RowFormat sınıfını keşfedin. Belge tasarımınızı güçlü, esnek özellikler ile geliştirin.
type: docs
weight: 7180
url: /tr/net/aspose.words.tables/rowformat/
---
## RowFormat class

Bir tablo satırı için tüm biçimlendirmeyi temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Tablolarla Çalışma](https://docs.aspose.com/words/net/working-with-tables/) belgeleme makalesi.

```csharp
public class RowFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AllowBreakAcrossPages](../../aspose.words.tables/rowformat/allowbreakacrosspages/) { get; set; } | Bir tablo satırındaki metnin sayfa sonu boyunca bölünmesine izin veriliyorsa doğrudur. |
| [Borders](../../aspose.words.tables/rowformat/borders/) { get; } | Satır için varsayılan hücre kenarlıklarının koleksiyonunu alır. |
| [HeadingFormat](../../aspose.words.tables/rowformat/headingformat/) { get; set; } | Tablo birden fazla sayfaya yayıldığında satır her sayfada tablo başlığı olarak tekrarlanıyorsa doğrudur. |
| [Height](../../aspose.words.tables/rowformat/height/) { get; set; } | Tablo satırının yüksekliğini noktalar halinde alır veya ayarlar. |
| [HeightRule](../../aspose.words.tables/rowformat/heightrule/) { get; set; } | Tablo satırının yüksekliğini belirleme kuralını alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/rowformat/clearformatting/)() | Varsayılan satır biçimlendirmesine sıfırlar. |

## Örnekler

Bir tablo satırının biçimlendirmesinin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Tüm satırın görünümünü değiştiren biçimlendirmeyi ayarlamak için ilk satırın "RowFormat" özelliğini kullanın.
Row firstRow = table.FirstRow;
firstRow.RowFormat.Borders.LineStyle = LineStyle.None;
firstRow.RowFormat.HeightRule = HeightRule.Auto;
firstRow.RowFormat.AllowBreakAcrossPages = true;

doc.Save(ArtifactsDir + "Table.RowFormat.docx");
```

Bir tablodaki satır ve hücrelerin biçiminin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("City");
builder.InsertCell();
builder.Write("Country");
builder.EndRow();
builder.InsertCell();
builder.Write("London");
builder.InsertCell();
builder.Write("U.K.");
builder.EndTable();

// Biçimlendirmeyi değiştirmek için ilk satırın "RowFormat" özelliğini kullanın
// Bu satırdaki tüm hücrelerin içerikleri.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Son satırdaki ilk hücrenin "CellFormat" özelliğini kullanarak o hücrenin içeriğinin biçimlendirmesini değiştirin.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

Özel kenarlıkları olan bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Bir belge oluşturucu için tablo biçimlendirme seçeneklerini ayarlama
// bunları eklediğimiz her satıra ve hücreye uygulayacaktır.
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

// Biçimlendirmeyi değiştirmek, bunu geçerli hücreye uygulayacaktır.
// ve sonrasında builder ile oluşturduğumuz yeni hücreler.
// Bu daha önce eklediğimiz hücreleri etkilemeyecektir.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Dikey metne uyacak şekilde satır yüksekliğini artırın.
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

* ad alanı [Aspose.Words.Tables](../../aspose.words.tables/)
* toplantı [Aspose.Words](../../)
