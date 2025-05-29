---
title: ChartAxis Class
linktitle: ChartAxis
articleTitle: ChartAxis
second_title: .NET için Aspose.Words
description: Özelleştirilebilir grafik ekseni seçenekleri için Aspose.Words.Drawing.Charts.ChartAxis sınıfını keşfedin. Veri görselleştirmenizi zahmetsizce geliştirin!
type: docs
weight: 890
url: /tr/net/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class

Grafiğin eksen seçeneklerini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafiklerle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) belgeleme makalesi.

```csharp
public class ChartAxis
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AxisBetweenCategories](../../aspose.words.drawing.charts/chartaxis/axisbetweencategories/) { get; set; } | Kategoriler arasında değer ekseninin kategori eksenini geçip geçmediğini belirten bir bayrak alır veya ayarlar. |
| [BaseTimeUnit](../../aspose.words.drawing.charts/chartaxis/basetimeunit/) { get; set; } | Zaman kategorisi ekseninde gösterilen en küçük zaman birimini döndürür veya ayarlar. |
| [CategoryType](../../aspose.words.drawing.charts/chartaxis/categorytype/) { get; set; } | Kategori ekseninin türünü alır veya ayarlar. |
| [Crosses](../../aspose.words.drawing.charts/chartaxis/crosses/) { get; set; } | Bu eksenin dik ekseni nasıl kestiğini belirtir. |
| [CrossesAt](../../aspose.words.drawing.charts/chartaxis/crossesat/) { get; set; } | Eksenin dik eksende nerede kesiştiğini belirtir. |
| [DisplayUnit](../../aspose.words.drawing.charts/chartaxis/displayunit/) { get; } | Değer ekseni için görüntüleme birimlerinin ölçekleme değerini belirtir. |
| [Document](../../aspose.words.drawing.charts/chartaxis/document/) { get; } | Üst grafiği içeren belgeyi döndürür. |
| [Format](../../aspose.words.drawing.charts/chartaxis/format/) { get; } | Eksen çizgi biçimlendirmesine ve işaret etiketlerinin doldurulmasına erişim sağlar. |
| [HasMajorGridlines](../../aspose.words.drawing.charts/chartaxis/hasmajorgridlines/) { get; set; } | Eksenin ana ızgara çizgilerine sahip olup olmadığını belirten bir bayrak alır veya ayarlar. |
| [HasMinorGridlines](../../aspose.words.drawing.charts/chartaxis/hasminorgridlines/) { get; set; } | Eksenin küçük ızgara çizgilerine sahip olup olmadığını belirten bir bayrak alır veya ayarlar. |
| [Hidden](../../aspose.words.drawing.charts/chartaxis/hidden/) { get; set; } | Bu eksenin gizli olup olmadığını belirten bir bayrak alır veya ayarlar. |
| [MajorTickMark](../../aspose.words.drawing.charts/chartaxis/majortickmark/) { get; set; } | Ana onay işaretlerini döndürür veya ayarlar. |
| [MajorUnit](../../aspose.words.drawing.charts/chartaxis/majorunit/) { get; set; } | Ana işaretler arasındaki mesafeyi döndürür veya ayarlar. |
| [MajorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/majorunitisauto/) { get; set; } | Ana işaretler arasındaki varsayılan mesafenin kullanılıp kullanılmayacağını belirten bir bayrak alır veya ayarlar. |
| [MajorUnitScale](../../aspose.words.drawing.charts/chartaxis/majorunitscale/) { get; set; } | Zaman kategorisi eksenindeki ana işaretler için ölçek değerini döndürür veya ayarlar. |
| [MinorTickMark](../../aspose.words.drawing.charts/chartaxis/minortickmark/) { get; set; } | Eksen için küçük işaret çizgilerini döndürür veya ayarlar. |
| [MinorUnit](../../aspose.words.drawing.charts/chartaxis/minorunit/) { get; set; } | Küçük işaretler arasındaki mesafeyi döndürür veya ayarlar. |
| [MinorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/minorunitisauto/) { get; set; } | Küçük işaretler arasındaki varsayılan mesafenin kullanılıp kullanılmayacağını belirten bir bayrak alır veya ayarlar. |
| [MinorUnitScale](../../aspose.words.drawing.charts/chartaxis/minorunitscale/) { get; set; } | Zaman kategorisi eksenindeki küçük işaretler için ölçek değerini döndürür veya ayarlar. |
| [NumberFormat](../../aspose.words.drawing.charts/chartaxis/numberformat/) { get; } | Bir[`ChartNumberFormat`](../chartnumberformat/) eksen için sayı biçimlerinin tanımlanmasına izin veren nesne. |
| [ReverseOrder](../../aspose.words.drawing.charts/chartaxis/reverseorder/) { get; set; } | Eksen değerlerinin ters sırada, yani maksimumdan minimuma doğru görüntülenip görüntülenmeyeceğini belirten bir bayrak döndürür veya ayarlar. |
| [Scaling](../../aspose.words.drawing.charts/chartaxis/scaling/) { get; } | Eksenin ölçekleme seçeneklerine erişim sağlar. |
| [TickLabels](../../aspose.words.drawing.charts/chartaxis/ticklabels/) { get; } | Eksen onay işareti etiketlerinin özelliklerine erişim sağlar. |
| [TickMarkSpacing](../../aspose.words.drawing.charts/chartaxis/tickmarkspacing/) { get; set; } | İşaretlerin çizildiği aralığı alır veya ayarlar. |
| [Title](../../aspose.words.drawing.charts/chartaxis/title/) { get; } | Eksen başlığı özelliklerine erişim sağlar. |
| [Type](../../aspose.words.drawing.charts/chartaxis/type/) { get; } | Eksenin türünü döndürür. |

## Örnekler

Bir grafiğin nasıl ekleneceğini ve eksenlerinin görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// X ekseni için kategoriler ve Y ekseni için ilgili sayısal değerler içeren bir grafik serisi ekleyin.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Grafik eksenlerinin görünümünü değiştirebilen çeşitli seçenekleri vardır,
// yönleri, majör/minör birim tikleri ve tik işaretleri gibi.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabels.Offset = 50;
xAxis.TickLabels.Position = AxisTickLabelPosition.Low;
xAxis.TickLabels.IsAutoSpacing = false;
xAxis.TickMarkSpacing = 1;

Assert.AreEqual(doc, xAxis.Document);

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabels.Position = AxisTickLabelPosition.NextToAxis;
yAxis.TickLabels.Alignment = ParagraphAlignment.Center;
yAxis.TickLabels.Font.Color = Color.Red;
yAxis.TickLabels.Spacing = 1;

// Sütun grafiklerin Z ekseni yoktur.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
