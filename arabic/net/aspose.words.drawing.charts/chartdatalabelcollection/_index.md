---
title: ChartDataLabelCollection
second_title: Aspose.Words لمراجع .NET API
description: يمثل مجموعة منChartDataLabel./chartdatalabel .
type: docs
weight: 640
url: /ar/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

يمثل مجموعة من[`ChartDataLabel`](../chartdatalabel) .

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count) { get; } | إرجاع عدد[`ChartDataLabel`](../chartdatalabel) في هذه المجموعة. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item) { get; } | عوائد[`ChartDataLabel`](../chartdatalabel) للفهرس المحدد. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat) { get; } | يحصل على ملف[`ChartNumberFormat`](../chartnumberformat) مثال يسمح بتعيين تنسيق رقم لتسميات البيانات لسلسلة بأكملها. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator) { get; set; } | الحصول على أو تعيين فاصل السلسلة المستخدم لتسميات البيانات للسلسلة بأكملها. الافتراضي هو الفاصلة ، باستثناء المخططات الدائرية التي تعرض اسم الفئة والنسبة المئوية فقط ، عند استخدام فاصل أسطر بدلاً من ذلك. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize) { get; set; } | يسمح بتحديد ما إذا كان سيتم عرض حجم الفقاعة لتسميات البيانات الخاصة بالسلسلة بأكملها. ينطبق فقط على المخططات الفقاعية. القيمة الافتراضية هي **خاطئة** . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname) { get; set; } | يسمح بتحديد ما إذا كان سيتم عرض اسم الفئة لتسميات البيانات الخاصة بالسلسلة بأكملها. القيمة الافتراضية هي **خاطئة** . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange) { get; set; } | يسمح بتحديد ما إذا كان سيتم عرض القيم من نطاق تسميات البيانات في تسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي **خاطئة** . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines) { get; set; } | يسمح بتحديد ما إذا كان يلزم إظهار خطوط البادئة لتسميات البيانات لتسميات البيانات الخاصة بالسلسلة بأكملها. القيمة الافتراضية هي **خاطئة** . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey) { get; set; } | يسمح بتحديد ما إذا كان سيتم عرض مفتاح وسيلة الإيضاح لتسميات البيانات الخاصة بالسلسلة بأكملها. القيمة الافتراضية هي **خاطئة** . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage) { get; set; } | يسمح بتحديد ما إذا كان سيتم عرض قيمة النسبة المئوية لتسميات البيانات الخاصة بالسلسلة بأكملها. القيمة الافتراضية هي **خاطئة** . ينطبق فقط على المخططات الدائرية. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname) { get; set; } | إرجاع أو تعيين قيمة منطقية للإشارة إلى سلوك عرض اسم السلسلة لتسميات البيانات الخاصة بالسلسلة بأكملها. **حقيقي**لإظهار اسم المسلسل. **خطأ شنيع** لإخفاء. بشكل افتراضي **خاطئة** . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue) { get; set; } | يسمح بتحديد ما إذا كان سيتم عرض القيم في تسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي **خاطئة** . |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat)() | مسح تنسيق الكل[`ChartDataLabel`](../chartdatalabel) في هذه المجموعة. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator)() | إرجاع كائن العداد . |

### أمثلة

يوضح كيفية تطبيق التسميات على نقاط البيانات في مخطط خطي.

```csharp
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

    // تغيير سلسلة الفاصل لكل تسمية بيانات في سلسلة.
    using (IEnumerator<ChartDataLabel> enumerator = chart.Series[0].DataLabels.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.AreEqual(", ", enumerator.Current.Separator);
            enumerator.Current.Separator = " & ";
        }
    }

    // للحصول على رسم بياني أنظف ، يمكننا إزالة ملصقات البيانات بشكل فردي.
    chart.Series[1].DataLabels[2].ClearFormat();

    // يمكننا أيضًا تجريد سلسلة كاملة من تسميات البيانات الخاصة بها مرة واحدة.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// تطبيق تسميات البيانات بتنسيق أرقام مخصص وفاصل على عدة نقاط بيانات في سلسلة.
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

* class [ChartDataLabel](../chartdatalabel)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
