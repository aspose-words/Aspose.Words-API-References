---
title: Class ChartSeries
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.Charts.ChartSeries فصل. يمثل خصائص سلسلة المخططات.
type: docs
weight: 780
url: /ar/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

يمثل خصائص سلسلة المخططات.

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class ChartSeries : IChartDataPoint
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } | يحدد ما إذا كان يجب أن يكون للفقاعات الموجودة في المخطط الفقاعي تأثير ثلاثي الأبعاد مطبق عليها. |
| [BubbleSizes](../../aspose.words.drawing.charts/chartseries/bubblesizes/) { get; } | الحصول على مجموعة من أحجام الفقاعات لسلسلة المخططات هذه. |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | يحدد إعدادات تسميات البيانات للسلسلة بأكملها. |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | إرجاع مجموعة من كائنات التنسيق لجميع نقاط البيانات في هذه السلسلة. |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } | يحدد مقدار نقل نقطة البيانات من مركز الدائرة. يمكن أن يكون سالبًا، ويعني السالب أنه لم يتم تعيين الخاصية ولا ينبغي تطبيق أي انفجار. ينطبق فقط على المخططات الدائرية. |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | يوفر الوصول إلى التعبئة وتنسيق الخط للسلسلة. |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | الحصول على أو تعيين علامة تشير إلى ما إذا كانت تسميات البيانات معروضة للسلسلة. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } | يحدد ما إذا كان العنصر الأصلي يجب أن يعكس ألوانه إذا كانت القيمة سالبة. |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | الحصول على إدخال وسيلة إيضاح لسلسلة المخططات هذه. |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } | يحدد علامة البيانات. يتم إنشاء العلامة تلقائيًا عند الطلب. |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | الحصول على اسم السلسلة أو تعيينه، إذا لم يتم تعيين الاسم بشكل صريح، فسيتم إنشاؤه باستخدام الفهرس. بشكل افتراضي يتم إرجاع السلسلة بالإضافة إلى فهرس واحد. |
| [SeriesType](../../aspose.words.drawing.charts/chartseries/seriestype/) { get; } | الحصول على نوع سلسلة المخططات هذه. |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | يسمح بتحديد ما إذا كان الخط الذي يربط النقاط على الرسم البياني سيتم تنعيمه باستخدام خطوط Catmull-Rom. |
| [XValues](../../aspose.words.drawing.charts/chartseries/xvalues/) { get; } | الحصول على مجموعة من قيم X لسلسلة المخططات هذه. |
| [YValues](../../aspose.words.drawing.charts/chartseries/yvalues/) { get; } | الحصول على مجموعة من قيم Y لسلسلة المخططات هذه. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add)(ChartXValue) | إضافة قيمة X المحددة إلى سلسلة المخططات. إذا كانت السلسلة تدعم قيم Y وأحجام الفقاعات، فستكون فارغة للقيمة X. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_1)(ChartXValue, ChartYValue) | إضافة قيم X وY المحددة إلى سلسلة المخططات. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_2)(ChartXValue, ChartYValue, double) | إضافة قيمة X وقيمة Y وحجم الفقاعة المحددة إلى سلسلة المخطط. |
| [Clear](../../aspose.words.drawing.charts/chartseries/clear/)() | إزالة كافة قيم البيانات من سلسلة المخططات. تم مسح تنسيق جميع نقاط البيانات الفردية وتسميات البيانات. |
| [ClearValues](../../aspose.words.drawing.charts/chartseries/clearvalues/)() | إزالة كافة قيم البيانات من سلسلة المخططات مع الحفاظ على تنسيق نقاط البيانات وتسميات البيانات. |
| [CopyFormatFrom](../../aspose.words.drawing.charts/chartseries/copyformatfrom/)(int) |  |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert)(int, ChartXValue) | يقوم بإدراج قيمة X المحددة في سلسلة المخططات في الفهرس المحدد. إذا كانت السلسلة تدعم قيم Y وأحجام الفقاعات، فستكون فارغة بالنسبة لقيمة X. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_1)(int, ChartXValue, ChartYValue) | يقوم بإدراج قيم X وY المحددة في سلسلة المخططات في الفهرس المحدد. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_2)(int, ChartXValue, ChartYValue, double) | يقوم بإدراج قيمة X المحددة وقيمة Y وحجم الفقاعة في سلسلة المخططات في الفهرس المحدد. |
| [Remove](../../aspose.words.drawing.charts/chartseries/remove/)(int) | إزالة القيمة X والقيمة Y وحجم الفقاعة، إذا كانت مدعومة، من سلسلة المخططات في الفهرس المحدد. تتم أيضًا إزالة نقطة البيانات المقابلة وتسمية البيانات. |

### أمثلة

يوضح كيفية تطبيق التسميات على نقاط البيانات في مخطط خطي.

```csharp
public void DataLabels()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape chartShape = builder.InsertChart(ChartType.Line, 400, 300);
    Chart chart = chartShape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // قم بتطبيق تسميات البيانات على كل سلسلة في المخطط.
    // ستظهر هذه التسميات بجوار كل نقطة بيانات في الرسم البياني وستعرض قيمتها.
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.AreEqual(4, series.DataLabels.Count);
    }

    // قم بتغيير السلسلة الفاصلة لكل تسمية بيانات في السلسلة.
    using (IEnumerator<ChartDataLabel> enumerator = chart.Series[0].DataLabels.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.AreEqual(", ", enumerator.Current.Separator);
            enumerator.Current.Separator = " & ";
        }
    }

    // للحصول على رسم بياني أكثر وضوحًا، يمكننا إزالة تسميات البيانات بشكل فردي.
    chart.Series[1].DataLabels[2].ClearFormat();

    // يمكننا أيضًا تجريد سلسلة كاملة من تسميات البيانات الخاصة بها مرة واحدة.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// قم بتطبيق تسميات البيانات بتنسيق أرقام مخصص وفاصل على عدة نقاط بيانات في سلسلة.
/// </summary>
private static void ApplyDataLabels(ChartSeries series, int labelsCount, string numberFormat, string separator)
{
    for (int i = 0; i < labelsCount; i++)
    {
        series.HasDataLabels = true;

        Assert.False(series.DataLabels[i].IsVisible);

        series.DataLabels[i].ShowCategoryName = true;
        series.DataLabels[i].ShowSeriesName = true;
        series.DataLabels[i].ShowValue = true;
        series.DataLabels[i].ShowLeaderLines = true;
        series.DataLabels[i].ShowLegendKey = true;
        series.DataLabels[i].ShowPercentage = false;
        series.DataLabels[i].IsHidden = false;
        Assert.False(series.DataLabels[i].ShowDataLabelsRange);

        series.DataLabels[i].NumberFormat.FormatCode = numberFormat;
        series.DataLabels[i].Separator = separator;

        Assert.False(series.DataLabels[i].ShowDataLabelsRange);
        Assert.True(series.DataLabels[i].IsVisible);
        Assert.False(series.DataLabels[i].IsHidden);
    }
}
```

### أنظر أيضا

* interface [IChartDataPoint](../ichartdatapoint/)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)


