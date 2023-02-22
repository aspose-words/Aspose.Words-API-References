---
title: Class AxisBound
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.Charts.AxisBound sınıf. Eksen değerlerinin minimum veya maksimum sınırını temsil eder.
type: docs
weight: 500
url: /tr/net/aspose.words.drawing.charts/axisbound/
---
## AxisBound class

Eksen değerlerinin minimum veya maksimum sınırını temsil eder.

```csharp
public sealed class AxisBound
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [AxisBound](axisbound/#constructor)() | Eksen sınırının bir sözcük işleme uygulaması tarafından otomatik olarak belirlenmesi gerektiğini belirten yeni bir örnek oluşturur. |
| [AxisBound](axisbound/#constructor_2)(DateTime) | Tarih saat değeri olarak temsil edilen bir eksen sınırı oluşturur. |
| [AxisBound](axisbound/#constructor_1)(double) | Sayı olarak gösterilen bir eksen sınırı oluşturur. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [IsAuto](../../aspose.words.drawing.charts/axisbound/isauto/) { get; } | Eksen sınırının otomatik olarak belirlenmesi gerektiğini belirten bir bayrak döndürür. |
| [Value](../../aspose.words.drawing.charts/axisbound/value/) { get; } | Eksenin sayısal değerini döndürür. |
| [ValueAsDate](../../aspose.words.drawing.charts/axisbound/valueasdate/) { get; } | Tarih saat olarak temsil edilen eksen sınırının değerini döndürür. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/axisbound/equals/)(object) | Belirtilen nesnenin değer olarak geçerli nesneye eşit olup olmadığını belirler. |
| override [GetHashCode](../../aspose.words.drawing.charts/axisbound/gethashcode/)() | Bu tür için bir karma işlevi olarak hizmet eder. |
| override [ToString](../../aspose.words.drawing.charts/axisbound/tostring/)() | Bu nesnenin değerini görüntüleyen kullanıcı dostu bir dize döndürür. |

### Notlar

Sınır, sayısal, tarih saat veya özel bir "otomatik" değer olarak belirtilebilir.

Bu sınıfın örnekleri değişmezdir.

### Örnekler

Tarih/saat değerleriyle grafiğin nasıl ekleneceğini gösterir.

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

// X ekseni için alt ve üst sınırları ayarlayın.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// X ekseninin ana birimlerini bir haftaya ve küçük birimleri bir güne ayarlayın.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;

// Ondalık değerler için Y ekseni özelliklerini tanımlayın.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabelPosition = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)


