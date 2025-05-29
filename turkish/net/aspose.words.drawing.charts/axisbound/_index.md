---
title: AxisBound Class
linktitle: AxisBound
articleTitle: AxisBound
second_title: .NET için Aspose.Words
description: Grafiklerde eksen değer sınırlarını tanımlayarak hassas veri görselleştirmesi için çözümünüz olan Aspose.Words.Drawing.Charts.AxisBound sınıfını keşfedin.
type: docs
weight: 750
url: /tr/net/aspose.words.drawing.charts/axisbound/
---
## AxisBound class

Eksen değerlerinin minimum veya maksimum sınırını temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafiklerle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) belgeleme makalesi.

```csharp
public sealed class AxisBound
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [AxisBound](axisbound/#constructor)() | Eksen sınırının bir kelime işleme uygulaması tarafından otomatik olarak belirlenmesi gerektiğini belirten yeni bir örnek oluşturur. |
| [AxisBound](axisbound/#constructor_2)(*DateTime*) | Tarih/saat değeri olarak temsil edilen bir eksen sınırı oluşturur. |
| [AxisBound](axisbound/#constructor_1)(*double*) | Bir sayı olarak temsil edilen bir eksen sınırı oluşturur. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [IsAuto](../../aspose.words.drawing.charts/axisbound/isauto/) { get; } | Eksen sınırının otomatik olarak belirlenmesi gerektiğini belirten bir bayrak döndürür. |
| [Value](../../aspose.words.drawing.charts/axisbound/value/) { get; } | Eksen sınırının sayısal değerini döndürür. |
| [ValueAsDate](../../aspose.words.drawing.charts/axisbound/valueasdate/) { get; } | Eksen sınırının datetime olarak temsil edilen değerini döndürür. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/axisbound/equals/)(*object*) | Belirtilen nesnenin geçerli nesneye eşit değerde olup olmadığını belirler. |
| override [GetHashCode](../../aspose.words.drawing.charts/axisbound/gethashcode/)() | Bu tür için bir karma işlevi görevi görür. |
| override [ToString](../../aspose.words.drawing.charts/axisbound/tostring/)() | Bu nesnenin değerini görüntüleyen kullanıcı dostu bir dize döndürür. |

## Notlar

Sınır, sayısal, tarih-saat veya özel bir "otomatik" değer olarak belirtilebilir.

Bu sınıfın örnekleri değiştirilemezdir.

## Örnekler

Tarih/saat değerleri içeren grafiğin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart.Series.Clear();

// X ekseni için tarih/saat değerlerini ve Y ekseni için ilgili ondalık değerleri içeren özel bir seri ekleyin.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// X ekseni için alt ve üst sınırları belirleyin.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// X ekseninin ana birimlerini haftaya, küçük birimlerini ise güne ayarlayın.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;
xAxis.HasMajorGridlines = true;
xAxis.HasMinorGridlines = true;

// Ondalık değerler için Y ekseni özelliklerini tanımlayın.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabels.Position = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);
yAxis.HasMajorGridlines = true;
yAxis.HasMinorGridlines = true;

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
