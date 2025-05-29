---
title: ChartSeries Class
linktitle: ChartSeries
articleTitle: ChartSeries
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Charts.ChartSeries، وهي مفتاحك لتحسين خصائص سلسلة المخططات لإنشاء المستندات وتصورها بشكل ديناميكي.
type: docs
weight: 1070
url: /ar/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

يمثل خصائص سلسلة الرسم البياني.

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class ChartSeries : IChartDataPoint
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } | يحدد ما إذا كان يجب تطبيق تأثير ثلاثي الأبعاد على الفقاعات الموجودة في مخطط الفقاعات. |
| [BubbleSizes](../../aspose.words.drawing.charts/chartseries/bubblesizes/) { get; } | يحصل على مجموعة من أحجام الفقاعات لسلسلة المخططات هذه. |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | يحدد إعدادات تسميات البيانات للسلسلة بأكملها. |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | يعيد مجموعة من كائنات التنسيق لجميع نقاط البيانات في هذه السلسلة. |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } | يحدد مقدار نقل نقطة البيانات من مركز الفطيرة. يمكن أن يكون سلبيًا، ويعني السلبي أن الخاصية غير مضبوطة ولا ينبغي تطبيق أي انفجار. ينطبق فقط على المخططات الدائرية. |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | يوفر إمكانية الوصول إلى تنسيق التعبئة والخطوط للسلسلة. |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | يحصل على علم أو يعينه للإشارة إلى ما إذا كان سيتم عرض تسميات البيانات للسلسلة. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } | يحدد ما إذا كان العنصر الرئيسي سيعكس ألوانه إذا كانت القيمة سلبية. |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | يحصل على إدخال أسطورة لسلسلة الرسم البياني هذه. |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } | يحدد علامة بيانات. يتم إنشاء العلامة تلقائيًا عند الطلب. |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | يحصل على اسم السلسلة أو يعينه، إذا لم يتم تعيين الاسم صراحةً، فسيتم إنشاؤه باستخدام الفهرس. بشكل افتراضي، يتم إرجاع السلسلة بالإضافة إلى فهرس واحد بناءً على ذلك. |
| [SeriesType](../../aspose.words.drawing.charts/chartseries/seriestype/) { get; } | يحصل على نوع سلسلة الرسم البياني هذه. |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | يسمح بتحديد ما إذا كان الخط الذي يربط النقاط على الرسم البياني سيتم تنعيمه باستخدام خطوط Catmull-Rom. |
| [XValues](../../aspose.words.drawing.charts/chartseries/xvalues/) { get; } | يحصل على مجموعة من قيم X لسلسلة الرسم البياني هذه. |
| [YValues](../../aspose.words.drawing.charts/chartseries/yvalues/) { get; } | يحصل على مجموعة من قيم Y لسلسلة الرسم البياني هذه. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add)(*[ChartXValue](../chartxvalue/)*) | يُضيف قيمة X المحددة إلى سلسلة المخططات. إذا كانت السلسلة تدعم قيم Y وأحجام الفقاعات، فستكون فارغة لقيمة X. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_1)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | يضيف قيم X وY المحددة إلى سلسلة الرسم البياني. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_2)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | يضيف قيمة X وقيمة Y وحجم الفقاعة المحددة إلى سلسلة الرسم البياني. |
| [Clear](../../aspose.words.drawing.charts/chartseries/clear/)() | يزيل جميع قيم البيانات من سلسلة المخططات. يُمسح تنسيق جميع نقاط البيانات الفردية وعلامات البيانات. |
| [ClearValues](../../aspose.words.drawing.charts/chartseries/clearvalues/)() | يزيل جميع قيم البيانات من سلسلة الرسم البياني مع الحفاظ على تنسيق نقاط البيانات وعلامات البيانات. |
| [CopyFormatFrom](../../aspose.words.drawing.charts/chartseries/copyformatfrom/)(*int*) | نسخ تنسيق نقطة البيانات الافتراضية من نقطة البيانات ذات الفهرس المحدد. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert)(*int, [ChartXValue](../chartxvalue/)*) | يُدرج قيمة X المحددة في سلسلة المخططات عند الفهرس المحدد. إذا كانت السلسلة تدعم قيم Y وأحجام الفقاعات، فستكون فارغة لقيمة X. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_1)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | يقوم بإدراج قيم X وY المحددة في سلسلة الرسم البياني عند الفهرس المحدد. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_2)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | يقوم بإدراج قيمة X وقيمة Y وحجم الفقاعة المحددة في سلسلة الرسم البياني عند الفهرس المحدد. |
| [Remove](../../aspose.words.drawing.charts/chartseries/remove/)(*int*) | يزيل قيمة X وقيمة Y وحجم الفقاعة، إذا كان مدعومًا، من سلسلة الرسم البياني عند الفهرس المحدد. تتم أيضًا إزالة نقطة البيانات المقابلة وعلامة البيانات. |

## أمثلة

يوضح كيفية تطبيق العلامات على نقاط البيانات في مخطط خطي.

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

    // تطبيق تسميات البيانات على كل سلسلة في الرسم البياني.
    // ستظهر هذه العلامات بجوار كل نقطة بيانات في الرسم البياني وتعرض قيمتها.
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.AreEqual(4, series.DataLabels.Count);
    }

    // قم بتغيير سلسلة الفاصل لكل تسمية بيانات في السلسلة.
    using (IEnumerator<ChartDataLabel> enumerator = chart.Series[0].DataLabels.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.AreEqual(", ", enumerator.Current.Separator);
            enumerator.Current.Separator = " & ";
        }
    }

    ChartDataLabel dataLabel = chart.Series[1].DataLabels[2];
    dataLabel.Format.Fill.Color = Color.Red;

    // للحصول على رسم بياني يبدو أكثر نظافة، يمكننا إزالة تسميات البيانات بشكل فردي.
    dataLabel.ClearFormat();

    // يمكننا أيضًا تجريد سلسلة كاملة من تسميات البيانات الخاصة بها مرة واحدة.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// قم بتطبيق تسميات البيانات بتنسيق رقم مخصص وفاصل لعدة نقاط بيانات في سلسلة.
/// </summary>
private static void ApplyDataLabels(ChartSeries series, int labelsCount, string numberFormat, string separator)
{
    series.HasDataLabels = true;
    series.Explosion = 40;

    for (int i = 0; i < labelsCount; i++)
    {
        Assert.False(series.DataLabels[i].IsVisible);

        series.DataLabels[i].ShowCategoryName = true;
        series.DataLabels[i].ShowSeriesName = true;
        series.DataLabels[i].ShowValue = true;
        series.DataLabels[i].ShowLeaderLines = true;
        series.DataLabels[i].ShowLegendKey = true;
        series.DataLabels[i].ShowPercentage = false;
        Assert.False(series.DataLabels[i].IsHidden);
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
