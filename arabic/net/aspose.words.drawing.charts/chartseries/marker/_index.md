---
title: ChartSeries.Marker
linktitle: Marker
articleTitle: Marker
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartSeries Marker لتخصيص علامات البيانات لمخططاتك بسهولة. حسّن التصور مع إنشاء العلامات تلقائيًا!
type: docs
weight: 100
url: /ar/net/aspose.words.drawing.charts/chartseries/marker/
---
## ChartSeries.Marker property

يحدد علامة بيانات. يتم إنشاء العلامة تلقائيًا عند الطلب.

```csharp
public ChartMarker Marker { get; }
```

## أمثلة

إظهار كيفية تعيين تنسيق العلامة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

//حذف السلسلة المولدة افتراضيًا.
chart.Series.Clear();
ChartSeries series = chart.Series.Add("AW Series 1", new[] { 0.7, 1.8, 2.6, 3.9 },
    new[] { 2.7, 3.2, 0.8, 1.7 });

// تعيين تنسيق العلامة.
series.Marker.Size = 40;
series.Marker.Symbol = MarkerSymbol.Square;
ChartDataPointCollection dataPoints = series.DataPoints;
dataPoints[0].Marker.Format.Fill.PresetTextured(PresetTexture.Denim);
dataPoints[0].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[0].Marker.Format.Stroke.BackColor = Color.Red;
dataPoints[1].Marker.Format.Fill.PresetTextured(PresetTexture.WaterDroplets);
dataPoints[1].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[1].Marker.Format.Stroke.Visible = false;
dataPoints[2].Marker.Format.Fill.PresetTextured(PresetTexture.GreenMarble);
dataPoints[2].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[3].Marker.Format.Fill.PresetTextured(PresetTexture.Oak);
dataPoints[3].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[3].Marker.Format.Stroke.Transparency = 0.5;

doc.Save(ArtifactsDir + "Charts.MarkerFormatting.docx");
```

### أنظر أيضا

* class [ChartMarker](../../chartmarker/)
* class [ChartSeries](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
