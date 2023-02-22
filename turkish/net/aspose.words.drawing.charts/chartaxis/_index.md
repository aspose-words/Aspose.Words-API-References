---
title: Class ChartAxis
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.Charts.ChartAxis sınıf. Grafiğin eksen seçeneklerini temsil eder.
type: docs
weight: 610
url: /tr/net/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class

Grafiğin eksen seçeneklerini temsil eder.

```csharp
public class ChartAxis
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AxisBetweenCategories](../../aspose.words.drawing.charts/chartaxis/axisbetweencategories/) { get; set; } | Değer ekseninin kategoriler arasında kategori eksenini geçip geçmediğini gösteren bir bayrak alır veya ayarlar. |
| [BaseTimeUnit](../../aspose.words.drawing.charts/chartaxis/basetimeunit/) { get; set; } | Zaman kategorisi ekseninde temsil edilen en küçük zaman birimini döndürür veya ayarlar. |
| [CategoryType](../../aspose.words.drawing.charts/chartaxis/categorytype/) { get; set; } | Kategori ekseninin türünü alır veya ayarlar. |
| [Crosses](../../aspose.words.drawing.charts/chartaxis/crosses/) { get; set; } | Bu eksenin dikey ekseni nasıl geçtiğini belirtir. |
| [CrossesAt](../../aspose.words.drawing.charts/chartaxis/crossesat/) { get; set; } | Eksenin dikey eksende kesiştiği yeri belirtir. |
| [DisplayUnit](../../aspose.words.drawing.charts/chartaxis/displayunit/) { get; } | Değer ekseni için görüntüleme birimlerinin ölçekleme değerini belirtir. |
| [Document](../../aspose.words.drawing.charts/chartaxis/document/) { get; } | Başlık sahibinin ait olduğu Belgeyi döndürür. |
| [Hidden](../../aspose.words.drawing.charts/chartaxis/hidden/) { get; set; } | Bu eksenin gizli olup olmadığını gösteren bir bayrak alır veya ayarlar. |
| [MajorTickMark](../../aspose.words.drawing.charts/chartaxis/majortickmark/) { get; set; } | Ana onay işaretlerini döndürür veya ayarlar. |
| [MajorUnit](../../aspose.words.drawing.charts/chartaxis/majorunit/) { get; set; } | Ana onay işaretleri arasındaki mesafeyi döndürür veya ayarlar. |
| [MajorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/majorunitisauto/) { get; set; } | Ana onay işaretleri arasındaki varsayılan mesafenin kullanılıp kullanılmayacağını belirten bir bayrak alır veya ayarlar. |
| [MajorUnitScale](../../aspose.words.drawing.charts/chartaxis/majorunitscale/) { get; set; } | Zaman kategorisi eksenindeki ana onay işaretleri için ölçek değerini döndürür veya ayarlar. |
| [MinorTickMark](../../aspose.words.drawing.charts/chartaxis/minortickmark/) { get; set; } | Eksen için küçük onay işaretlerini döndürür veya ayarlar. |
| [MinorUnit](../../aspose.words.drawing.charts/chartaxis/minorunit/) { get; set; } | Küçük onay işaretleri arasındaki mesafeyi döndürür veya ayarlar. |
| [MinorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/minorunitisauto/) { get; set; } | Küçük onay işaretleri arasındaki varsayılan mesafenin kullanılıp kullanılmayacağını belirten bir bayrak alır veya ayarlar. |
| [MinorUnitScale](../../aspose.words.drawing.charts/chartaxis/minorunitscale/) { get; set; } | Zaman kategorisi eksenindeki küçük onay işaretleri için ölçek değerini döndürür veya ayarlar. |
| [NumberFormat](../../aspose.words.drawing.charts/chartaxis/numberformat/) { get; } | Bir döndürür[`ChartNumberFormat`](../chartnumberformat/) eksen için sayı biçimlerinin tanımlanmasına izin veren nesne. |
| [ReverseOrder](../../aspose.words.drawing.charts/chartaxis/reverseorder/) { get; set; } | Eksen değerlerinin ters sırada görüntülenip görüntülenmeyeceğini belirten bir bayrak döndürür veya ayarlar, yani maks'tan min'e. |
| [Scaling](../../aspose.words.drawing.charts/chartaxis/scaling/) { get; } | Eksenin ölçekleme seçeneklerine erişim sağlar. |
| [TickLabelAlignment](../../aspose.words.drawing.charts/chartaxis/ticklabelalignment/) { get; set; } | Eksen onay etiketlerinin metin hizalamasını alır veya ayarlar. |
| [TickLabelOffset](../../aspose.words.drawing.charts/chartaxis/ticklabeloffset/) { get; set; } | Etiketlerin eksenden uzaklığını alır veya ayarlar. |
| [TickLabelPosition](../../aspose.words.drawing.charts/chartaxis/ticklabelposition/) { get; set; } | Eksen üzerindeki onay etiketlerinin konumunu döndürür veya ayarlar. |
| [TickLabelSpacing](../../aspose.words.drawing.charts/chartaxis/ticklabelspacing/) { get; set; } | Onay etiketlerinin çizildiği aralığı alır veya ayarlar. |
| [TickLabelSpacingIsAuto](../../aspose.words.drawing.charts/chartaxis/ticklabelspacingisauto/) { get; set; } | Onay etiketlerinin otomatik çizim aralığının kullanılıp kullanılmayacağını belirten bir bayrak alır veya ayarlar. |
| [TickMarkSpacing](../../aspose.words.drawing.charts/chartaxis/tickmarkspacing/) { get; set; } | Onay işaretlerinin çizildiği aralığı alır veya ayarlar. |
| [Type](../../aspose.words.drawing.charts/chartaxis/type/) { get; } | Eksenin türünü döndürür. |

### Örnekler

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

// Grafik eksenleri, görünümlerini değiştirebilen çeşitli seçeneklere sahiptir,
// yönleri, majör/alt birim keneleri ve kene işaretleri gibi.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabelOffset = 50;
xAxis.TickLabelPosition = AxisTickLabelPosition.Low;
xAxis.TickLabelSpacingIsAuto = false;
xAxis.TickMarkSpacing = 1;

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabelPosition = AxisTickLabelPosition.NextToAxis;

// Sütun grafiklerinin Z ekseni yoktur.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)


