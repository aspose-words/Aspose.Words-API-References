---
title: AxisTickLabelPosition Enum
linktitle: AxisTickLabelPosition
articleTitle: AxisTickLabelPosition
second_title: .NET için Aspose.Words
description: Gelişmiş grafik netliği ve sunumu için en uygun işaret etiketi yerleşimlerini tanımlayan Aspose.Words.Drawing.Charts.AxisTickLabelPosition enum'unu keşfedin.
type: docs
weight: 830
url: /tr/net/aspose.words.drawing.charts/axisticklabelposition/
---
## AxisTickLabelPosition enumeration

Tik etiketleri için olası konumları belirtir.

```csharp
public enum AxisTickLabelPosition
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| High | `0` | Eksen etiketlerinin dik eksenin en yüksek ucunda olacağını belirtir. |
| Low | `1` | Eksen etiketlerinin dik eksenin alt ucunda olacağını belirtir. |
| NextToAxis | `2` | Eksen etiketlerinin eksenin yanında olacağını belirtir. |
| None | `3` | Eksen etiketlerinin çizilmediğini belirtir. |
| Default | `2` | İşaret etiketleri konumunun varsayılan değerini belirtir. |

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
