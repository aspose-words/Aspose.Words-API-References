---
title: Class ChartMarker
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.Charts.ChartMarker فصل. يمثل علامة بيانات الرسم البياني .
type: docs
weight: 710
url: /ar/net/aspose.words.drawing.charts/chartmarker/
---
## ChartMarker class

يمثل علامة بيانات الرسم البياني .

```csharp
public class ChartMarker
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Format](../../aspose.words.drawing.charts/chartmarker/format/) { get; } | يوفر الوصول لتعبئة وتنسيق خط هذه العلامة. |
| [Size](../../aspose.words.drawing.charts/chartmarker/size/) { get; set; } | الحصول على أو تعيين حجم علامة المخطط . القيمة الافتراضية هي 7. |
| [Symbol](../../aspose.words.drawing.charts/chartmarker/symbol/) { get; set; } | الحصول على أو تعيين رمز علامة المخطط . |

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

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)


