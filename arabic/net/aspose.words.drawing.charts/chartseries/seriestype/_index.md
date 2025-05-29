---
title: ChartSeries.SeriesType
linktitle: SeriesType
articleTitle: SeriesType
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartSeries SeriesType لتحديد نوع سلسلة مخططاتك بسهولة وتحسين تصور بياناتك. احصل على رؤى قيّمة اليوم!
type: docs
weight: 120
url: /ar/net/aspose.words.drawing.charts/chartseries/seriestype/
---
## ChartSeries.SeriesType property

يحصل على نوع سلسلة الرسم البياني هذه.

```csharp
public ChartSeriesType SeriesType { get; }
```

## أمثلة

يوضح كيفية إزالة سلسلة مخطط محددة.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// قم بإزالة كافة سلاسل نوع العمود.
for (int i = chart.Series.Count - 1; i >= 0; i--)
{
    if (chart.Series[i].SeriesType == ChartSeriesType.Column)
        chart.Series.RemoveAt(i);
}

chart.Series.Add(
    "Aspose Series",
    new string[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 5.6, 7.1, 2.9, 8.9 });

doc.Save(ArtifactsDir + "Charts.RemoveSpecificChartSeries.docx");
```

### أنظر أيضا

* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeries](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
