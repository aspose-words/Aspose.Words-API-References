---
title: CellFormat Class
linktitle: CellFormat
articleTitle: CellFormat
second_title: .NET için Aspose.Words
description: Kapsamlı tablo hücresi biçimlendirmesi için Aspose.Words.Tables.CellFormat sınıfını keşfedin. Kullanımı kolay özelliklerle belge stilinizi geliştirin!
type: docs
weight: 7110
url: /tr/net/aspose.words.tables/cellformat/
---
## CellFormat class

Bir tablo hücresi için tüm biçimlendirmeyi temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Tablolarla Çalışma](https://docs.aspose.com/words/net/working-with-tables/) belgeleme makalesi.

```csharp
public class CellFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Borders](../../aspose.words.tables/cellformat/borders/) { get; } | Hücrenin kenarlıklarının koleksiyonunu alır. |
| [BottomPadding](../../aspose.words.tables/cellformat/bottompadding/) { get; set; } | Hücrenin içeriğinin altına eklenecek boşluk miktarını (nokta cinsinden) döndürür veya ayarlar. |
| [FitText](../../aspose.words.tables/cellformat/fittext/) { get; set; } | Eğer`doğru` , metni hücreye sığdırır ve her paragrafı hücrenin genişliğine sıkıştırır. |
| [HideMark](../../aspose.words.tables/cellformat/hidemark/) { get; set; } | Hücre işaretinin görünürlüğünü döndürür veya ayarlar. |
| [HorizontalMerge](../../aspose.words.tables/cellformat/horizontalmerge/) { get; set; } | Hücrenin satırdaki diğer hücrelerle yatay olarak nasıl birleştirileceğini belirtir. |
| [LeftPadding](../../aspose.words.tables/cellformat/leftpadding/) { get; set; } | Hücrenin içeriğinin soluna eklenecek boşluk miktarını (nokta cinsinden) döndürür veya ayarlar. |
| [Orientation](../../aspose.words.tables/cellformat/orientation/) { get; set; } | Bir tablo hücresindeki metnin yönünü döndürür veya ayarlar. |
| [PreferredWidth](../../aspose.words.tables/cellformat/preferredwidth/) { get; set; } | Hücrenin tercih edilen genişliğini döndürür veya ayarlar. |
| [RightPadding](../../aspose.words.tables/cellformat/rightpadding/) { get; set; } | Hücrenin içeriğinin sağına eklenecek boşluk miktarını (nokta cinsinden) döndürür veya ayarlar. |
| [Shading](../../aspose.words.tables/cellformat/shading/) { get; } | Bir[`Shading`](../../aspose.words/shading/) hücrenin gölgelendirme biçimlendirmesine başvuran nesne. |
| [TopPadding](../../aspose.words.tables/cellformat/toppadding/) { get; set; } | Hücrenin içeriğinin üstüne eklenecek boşluk miktarını (nokta cinsinden) döndürür veya ayarlar. |
| [VerticalAlignment](../../aspose.words.tables/cellformat/verticalalignment/) { get; set; } | Hücredeki metnin dikey hizalamasını döndürür veya ayarlar. |
| [VerticalMerge](../../aspose.words.tables/cellformat/verticalmerge/) { get; set; } | Hücrenin diğer hücrelerle dikey olarak nasıl birleştirileceğini belirtir. |
| [Width](../../aspose.words.tables/cellformat/width/) { get; set; } | Hücrenin genişliğini noktalar halinde alır. |
| [WrapText](../../aspose.words.tables/cellformat/wraptext/) { get; set; } | Eğer`doğru` , hücre için metni kaydır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/cellformat/clearformatting/)() | Varsayılan hücre biçimlendirmesine sıfırlar. Hücrenin genişliğini değiştirmez. |
| [SetPaddings](../../aspose.words.tables/cellformat/setpaddings/)(*double, double, double, double*) | Hücrenin içeriğinin soluna/üstüne/sağına/altına eklenecek boşluk miktarını (nokta cinsinden) ayarlar. |

## Örnekler

Bir tablo hücresinin biçimlendirmesinin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// Bir hücrenin görünümünü değiştiren biçimlendirmeyi ayarlamak için o hücrenin "CellFormat" özelliğini kullanın.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
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
