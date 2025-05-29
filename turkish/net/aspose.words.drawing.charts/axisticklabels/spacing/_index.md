---
title: AxisTickLabels.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: .NET için Aspose.Words
description: AxisTickLabels aralıklarını zahmetsizce kontrol edin! Veri görselleştirmenizi geliştirmek ve grafik netliğini artırmak için işaret etiketleri için aralıklar ayarlayın.
type: docs
weight: 80
url: /tr/net/aspose.words.drawing.charts/axisticklabels/spacing/
---
## AxisTickLabels.Spacing property

Tik etiketlerinin çizildiği aralığı alır veya ayarlar.

```csharp
public int Spacing { get; set; }
```

## Notlar

Özellik, metin kategorisi ve seri eksenleri için etkilidir. MS Office 2016 yeni grafikleri tarafından desteklenmez. Bir değerin geçerli aralığı 1'den büyük veya ona eşittir.

Bu özelliğin ayarlanması,[`IsAutoSpacing`](../isautospacing/) mülk`YANLIŞ`.

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

* class [AxisTickLabels](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
