---
title: IChartDataPoint.Marker
linktitle: Marker
articleTitle: Marker
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية IChartDataPoint Marker، التي تُنشئ تلقائيًا علامات بيانات لتحسين التصور والتحليل. ارتقِ بتجربة رسمك البياني!
type: docs
weight: 40
url: /ar/net/aspose.words.drawing.charts/ichartdatapoint/marker/
---
## IChartDataPoint.Marker property

يحدد علامة بيانات. يتم إنشاء العلامة تلقائيًا عند الطلب.

```csharp
public ChartMarker Marker { get; }
```

## أمثلة

يوضح كيفية العمل مع نقاط البيانات على مخطط خطي.

```csharp
public void ChartDataPoint()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape shape = builder.InsertChart(ChartType.Line, 500, 350);
    Chart chart = shape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // قم بالتأكيد على نقاط بيانات الرسم البياني من خلال جعلها تظهر على شكل أشكال ماسية.
    foreach (ChartSeries series in chart.Series)
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // قم بتنعيم الخط الذي يمثل سلسلة البيانات الأولى.
    chart.Series[0].Smooth = true;

    // تأكد من أن نقاط البيانات الخاصة بالسلسلة الأولى لن تعكس ألوانها إذا كانت القيمة سلبية.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    ChartDataPoint dataPoint = chart.Series[1].DataPoints[2];
    dataPoint.Format.Fill.Color = Color.Red;

    // للحصول على رسم بياني يبدو أكثر نظافة، يمكننا مسح التنسيق بشكل فردي.
    dataPoint.ClearFormat();

    // يمكننا أيضًا تجريد سلسلة كاملة من نقاط البيانات مرة واحدة.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// تطبيق عدد من نقاط البيانات على سلسلة.
/// </summary>
private static void ApplyDataPoints(ChartSeries series, int dataPointsCount, MarkerSymbol markerSymbol, int dataPointSize)
{
    for (int i = 0; i < dataPointsCount; i++)
    {
        ChartDataPoint point = series.DataPoints[i];
        point.Marker.Symbol = markerSymbol;
        point.Marker.Size = dataPointSize;

        Assert.AreEqual(i, point.Index);
    }
}
```

### أنظر أيضا

* class [ChartMarker](../../chartmarker/)
* interface [IChartDataPoint](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
