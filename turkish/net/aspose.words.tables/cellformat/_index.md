---
title: CellFormat
second_title: Aspose.Words for .NET API Referansı
description: Bir tablo hücresinin tüm biçimlendirmesini temsil eder.
type: docs
weight: 5960
url: /tr/net/aspose.words.tables/cellformat/
---
## CellFormat class

Bir tablo hücresinin tüm biçimlendirmesini temsil eder.

```csharp
public class CellFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Borders](../../aspose.words.tables/cellformat/borders) { get; } | Hücrenin kenarlıklarının koleksiyonunu alır. |
| [BottomPadding](../../aspose.words.tables/cellformat/bottompadding) { get; set; } | Hücre içeriğinin altına eklenecek boşluk miktarını (puan olarak) döndürür veya ayarlar. |
| [FitText](../../aspose.words.tables/cellformat/fittext) { get; set; } | Doğruysa, her paragrafı hücrenin genişliğine sıkıştırarak hücreye metin sığdırır. |
| [HorizontalMerge](../../aspose.words.tables/cellformat/horizontalmerge) { get; set; } | Hücrenin, satırdaki diğer hücrelerle yatay olarak nasıl birleştirileceğini belirtir. |
| [LeftPadding](../../aspose.words.tables/cellformat/leftpadding) { get; set; } | Hücre içeriğinin soluna eklenecek boşluk miktarını (puan olarak) döndürür veya ayarlar. |
| [Orientation](../../aspose.words.tables/cellformat/orientation) { get; set; } | Tablo hücresindeki metnin yönünü döndürür veya ayarlar. |
| [PreferredWidth](../../aspose.words.tables/cellformat/preferredwidth) { get; set; } | Hücrenin tercih edilen genişliğini döndürür veya ayarlar. |
| [RightPadding](../../aspose.words.tables/cellformat/rightpadding) { get; set; } | Hücre içeriğinin sağına eklenecek boşluk miktarını (puan olarak) döndürür veya ayarlar. |
| [Shading](../../aspose.words.tables/cellformat/shading) { get; } | Hücrenin gölgelendirme biçimlendirmesine başvuran bir Shading nesnesi döndürür. |
| [TopPadding](../../aspose.words.tables/cellformat/toppadding) { get; set; } | Hücre içeriğinin üzerine eklenecek boşluk miktarını (puan olarak) döndürür veya ayarlar. |
| [VerticalAlignment](../../aspose.words.tables/cellformat/verticalalignment) { get; set; } | Hücredeki metnin dikey hizalamasını döndürür veya ayarlar. |
| [VerticalMerge](../../aspose.words.tables/cellformat/verticalmerge) { get; set; } | Hücrenin diğer hücrelerle dikey olarak nasıl birleştirileceğini belirtir. |
| [Width](../../aspose.words.tables/cellformat/width) { get; set; } | Nokta olarak hücrenin genişliğini alır. |
| [WrapText](../../aspose.words.tables/cellformat/wraptext) { get; set; } | Doğruysa, hücre için metni kaydırın. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/cellformat/clearformatting)() | Varsayılan hücre biçimlendirmesine sıfırlar. Hücrenin genişliğini değiştirmez. |
| [SetPaddings](../../aspose.words.tables/cellformat/setpaddings)(double, double, double, double) | Hücre içeriğinin soluna/üstüne/sağına/altına eklenecek boşluk miktarını (puan olarak) ayarlar. |

### Örnekler

Bir tablo hücresinin biçimlendirmesinin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// Bir hücrenin görünümünü değiştiren biçimlendirmeyi ayarlamak için hücrenin "CellFormat" özelliğini kullanın.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
```

Tablodaki satırların ve hücrelerin biçiminin nasıl değiştirileceğini gösterir.

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
// bu satırdaki tüm hücrelerin içeriği.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Bu hücrenin içeriğinin biçimlendirmesini değiştirmek için son satırdaki ilk hücrenin "CellFormat" özelliğini kullanın.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
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

* ad alanı [Aspose.Words.Tables](../../aspose.words.tables)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
