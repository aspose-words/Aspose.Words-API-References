---
title: Class ChartDataLabelCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.Charts.ChartDataLabelCollection فصل. يمثل مجموعة منChartDataLabel .
type: docs
weight: 680
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

يمثل مجموعة من[`ChartDataLabel`](../chartdatalabel/) .

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count/) { get; } | إرجاع عدد[`ChartDataLabel`](../chartdatalabel/) في هذه المجموعة. |
| [Font](../../aspose.words.drawing.charts/chartdatalabelcollection/font/) { get; } | يوفر الوصول إلى تنسيق الخط الخاص بتسميات البيانات الخاصة بالسلسلة بأكملها. |
| [Format](../../aspose.words.drawing.charts/chartdatalabelcollection/format/) { get; } | يوفر إمكانية الوصول إلى تعبئة وتنسيق سطر تسميات البيانات. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item/) { get; } | إرجاع[`ChartDataLabel`](../chartdatalabel/) للفهرس المحدد. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat/) { get; } | يحصل على[`ChartNumberFormat`](../chartnumberformat/) مثيل يسمح بتعيين تنسيق الأرقام لتسميات البيانات الخاصة بسلسلة بأكملها. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator/) { get; set; } | الحصول على أو تعيين فاصل السلسلة المستخدم لتسميات البيانات الخاصة بالسلسلة بأكملها. الإعداد الافتراضي هو فاصلة، باستثناء المخططات الدائرية التي تعرض اسم الفئة والنسبة المئوية فقط، عند استخدام فاصل الأسطر بدلاً من ذلك. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/) { get; set; } | يسمح بتحديد ما إذا كان سيتم عرض حجم الفقاعة لتسميات البيانات الخاصة بالسلسلة بأكملها. ينطبق فقط على المخططات الفقاعية. القيمة الافتراضية هي`خطأ شنيع` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/) { get; set; } | يسمح بتحديد ما إذا كان سيتم عرض اسم الفئة لتسميات البيانات الخاصة بالسلسلة بأكملها. القيمة الافتراضية هي`خطأ شنيع` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange/) { get; set; } | يسمح بتحديد ما إذا كانت القيم من تسميات البيانات سيتم عرضها في تسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي`خطأ شنيع` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/) { get; set; } | يسمح بتحديد ما إذا كان من الضروري إظهار الخطوط الرئيسية لتسمية البيانات لتسميات البيانات الخاصة بالسلسلة بأكملها. القيمة الافتراضية هي`خطأ شنيع` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/) { get; set; } | يسمح بتحديد ما إذا كان سيتم عرض مفتاح وسيلة الإيضاح لتسميات البيانات الخاصة بالسلسلة بأكملها. القيمة الافتراضية هي`خطأ شنيع` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/) { get; set; } | يسمح بتحديد ما إذا كان سيتم عرض قيمة النسبة المئوية لتسميات البيانات الخاصة بالسلسلة بأكملها. القيمة الافتراضية هي`خطأ شنيع` . ينطبق فقط على المخططات الدائرية. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/) { get; set; } | إرجاع قيمة منطقية أو تعيينها للإشارة إلى سلوك عرض اسم السلسلة لتسميات البيانات الخاصة بالسلسلة بأكملها. `حقيقي` لإظهار اسم المسلسل؛`خطأ شنيع` لإخفاء. بشكل افتراضي`خطأ شنيع` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue/) { get; set; } | يسمح بتحديد ما إذا كان سيتم عرض القيم في تسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي`خطأ شنيع` . |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat/)() | مسح التنسيق للجميع[`ChartDataLabel`](../chartdatalabel/) في هذه المجموعة. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator/)() | يُرجع كائن العداد. |

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

* class [ChartDataLabel](../chartdatalabel/)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)


