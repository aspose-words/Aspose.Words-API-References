---
title: Class ChartDataPoint
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.Charts.ChartDataPoint فصل. يسمح بتحديد تنسيق نقطة بيانات واحدة على الرسم البياني.
type: docs
weight: 650
url: /ar/net/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class

يسمح بتحديد تنسيق نقطة بيانات واحدة على الرسم البياني.

```csharp
public class ChartDataPoint : IChartDataPoint
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartdatapoint/bubble3d/) { get; set; } |  |
| [Explosion](../../aspose.words.drawing.charts/chartdatapoint/explosion/) { get; set; } |  |
| [Format](../../aspose.words.drawing.charts/chartdatapoint/format/) { get; } | يوفر الوصول لتعبئة وتنسيق الخط لنقطة البيانات هذه. |
| [Index](../../aspose.words.drawing.charts/chartdatapoint/index/) { get; } | فهرس نقطة البيانات يطبق هذا الكائن التنسيق عليها. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartdatapoint/invertifnegative/) { get; set; } |  |
| [Marker](../../aspose.words.drawing.charts/chartdatapoint/marker/) { get; } |  |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapoint/clearformat/)() | يمسح تنسيق نقطة البيانات هذه. يتم تعيين الخصائص على القيم الافتراضية المحددة في السلسلة الأصلية. |

### ملاحظات

في سلسلة ، ملف`ChartDataPoint` الكائن عضو في[`ChartDataPointCollection`](../chartdatapointcollection/) . ملف[`ChartDataPointCollection`](../chartdatapointcollection/) يحتوي على`ChartDataPoint` كائن لكل نقطة.

### أمثلة

يوضح كيفية التعامل مع نقاط البيانات على مخطط خطي.

```csharp
[Test]
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

    // قم بتأكيد نقاط بيانات المخطط بجعلها تظهر كأشكال ماسية.
    foreach (ChartSeries series in chart.Series) 
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // قم بتمهيد الخط الذي يمثل سلسلة البيانات الأولى.
    chart.Series[0].Smooth = true;

    // تحقق من أن نقاط البيانات للسلسلة الأولى لن تعكس ألوانها إذا كانت القيمة سالبة.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    // للحصول على رسم بياني أكثر وضوحًا ، يمكننا مسح التنسيق بشكل فردي.
    chart.Series[1].DataPoints[2].ClearFormat();

    // يمكننا أيضًا تجريد سلسلة كاملة من نقاط البيانات مرة واحدة.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// يطبق عددًا من نقاط البيانات على سلسلة.
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

* interface [IChartDataPoint](../ichartdatapoint/)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)


