---
title: AxisTickLabels Class
linktitle: AxisTickLabels
articleTitle: AxisTickLabels
second_title: .NET için Aspose.Words
description: Daha iyi veri görselleştirmesi için grafiğinizin eksen işaret etiketlerini özelleştirilebilir özelliklerle geliştirmek üzere tasarlanmış Aspose.Words.Drawing.Charts.AxisTickLabels sınıfını keşfedin.
type: docs
weight: 840
url: /tr/net/aspose.words.drawing.charts/axisticklabels/
---
## AxisTickLabels class

Eksen onay işareti etiketlerinin özelliklerini temsil eder.

```csharp
public class AxisTickLabels
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Alignment](../../aspose.words.drawing.charts/axisticklabels/alignment/) { get; set; } | Eksen işareti etiketlerinin metin hizalamasını alır veya ayarlar. |
| [Font](../../aspose.words.drawing.charts/axisticklabels/font/) { get; } | Tik etiketlerinin yazı tipi biçimlendirmesine erişim sağlar. |
| [IsAutoSpacing](../../aspose.words.drawing.charts/axisticklabels/isautospacing/) { get; set; } | Tik etiketlerini çizmek için otomatik aralık kullanılıp kullanılmayacağını belirten bir bayrak alır veya ayarlar. |
| [Offset](../../aspose.words.drawing.charts/axisticklabels/offset/) { get; set; } | Tik etiketlerinin eksenden uzaklığını alır veya ayarlar. |
| [Orientation](../../aspose.words.drawing.charts/axisticklabels/orientation/) { get; set; } | İşaret etiketi metninin yönünü alır veya ayarlar. |
| [Position](../../aspose.words.drawing.charts/axisticklabels/position/) { get; set; } | Eksen üzerindeki onay etiketlerinin konumunu alır veya ayarlar. |
| [Rotation](../../aspose.words.drawing.charts/axisticklabels/rotation/) { get; set; } | Tik etiketlerinin derece cinsinden dönüşünü alır veya ayarlar. |
| [Spacing](../../aspose.words.drawing.charts/axisticklabels/spacing/) { get; set; } | Tik etiketlerinin çizildiği aralığı alır veya ayarlar. |

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
