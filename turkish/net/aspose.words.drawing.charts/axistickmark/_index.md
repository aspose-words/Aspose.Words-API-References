---
title: Enum AxisTickMark
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.Charts.AxisTickMark Sıralama. Onay işaretleri için olası konumları belirtir.
type: docs
weight: 580
url: /tr/net/aspose.words.drawing.charts/axistickmark/
---
## AxisTickMark enumeration

Onay işaretleri için olası konumları belirtir.

```csharp
public enum AxisTickMark
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Cross | `0` | Onay işaretlerinin ekseni keseceğini belirtir. |
| Inside | `1` | Onay işaretlerinin çizim alanı içinde olacağını belirtir. |
| Outside | `2` | Onay işaretlerinin çizim alanının dışında olacağını belirtir. |
| None | `3` | Onay işareti olmayacağını belirtir. |

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


