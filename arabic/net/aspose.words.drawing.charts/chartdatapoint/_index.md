---
title: ChartDataPoint Class
linktitle: ChartDataPoint
articleTitle: ChartDataPoint
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.Charts.ChartDataPoint فصل. يسمح بتحديد تنسيق نقطة بيانات واحدة على المخطط في C#.
type: docs
weight: 690
url: /ar/net/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class

يسمح بتحديد تنسيق نقطة بيانات واحدة على المخطط.

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class ChartDataPoint : IChartDataPoint
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartdatapoint/bubble3d/) { get; set; } | يحدد ما إذا كان يجب أن يكون للفقاعات الموجودة في المخطط الفقاعي تأثير ثلاثي الأبعاد مطبق عليها. |
| [Explosion](../../aspose.words.drawing.charts/chartdatapoint/explosion/) { get; set; } | يحدد مقدار نقل نقطة البيانات من مركز الدائرة. يمكن أن يكون سالبًا، ويعني السالب أنه لم يتم تعيين الخاصية ولا ينبغي تطبيق أي انفجار. ينطبق فقط على المخططات الدائرية. |
| [Format](../../aspose.words.drawing.charts/chartdatapoint/format/) { get; } | يوفر الوصول إلى التعبئة وتنسيق الخط لنقطة البيانات هذه. |
| [Index](../../aspose.words.drawing.charts/chartdatapoint/index/) { get; } | فهرس نقطة البيانات التي يطبق هذا الكائن التنسيق عليها. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartdatapoint/invertifnegative/) { get; set; } | يحدد ما إذا كان العنصر الأصلي يجب أن يعكس ألوانه إذا كانت القيمة سالبة. |
| [Marker](../../aspose.words.drawing.charts/chartdatapoint/marker/) { get; } | يحدد علامة بيانات المخطط. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapoint/clearformat/)() | مسح تنسيق نقطة البيانات هذه. يتم تعيين الخصائص على القيم الافتراضية المحددة في السلسلة الأصلية. |

## ملاحظات

في مسلسل`ChartDataPoint` الكائن هو عضو في[`ChartDataPointCollection`](../chartdatapointcollection/) . ال[`ChartDataPointCollection`](../chartdatapointcollection/) يحتوي على`ChartDataPoint` كائن لكل نقطة.

## أمثلة

يوضح كيفية التعامل مع نقاط البيانات على مخطط خطي.

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

    // قم بتأكيد نقاط بيانات المخطط من خلال جعلها تظهر كأشكال ماسية.
    foreach (ChartSeries series in chart.Series) 
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // قم بتسوية الخط الذي يمثل سلسلة البيانات الأولى.
    chart.Series[0].Smooth = true;

    // تحقق من أن نقاط البيانات الخاصة بالسلسلة الأولى لن تعكس ألوانها إذا كانت القيمة سالبة.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    // للحصول على رسم بياني أكثر وضوحًا، يمكننا مسح التنسيق بشكل فردي.
    chart.Series[1].DataPoints[2].ClearFormat();

    // يمكننا أيضًا تجريد سلسلة كاملة من نقاط البيانات مرة واحدة.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// يطبق عددًا من نقاط البيانات على السلسلة.
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
