---
title: ChartDataLabel
second_title: Aspose.Words لمراجع .NET API
description: يمثل تسمية البيانات على نقطة مخطط أو خط اتجاه.
type: docs
weight: 630
url: /ar/net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

يمثل تسمية البيانات على نقطة مخطط أو خط اتجاه.

```csharp
public class ChartDataLabel
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index/) { get; } | تحديد فهرس العنصر المحتوي. سيحدد هذا الفهرس أي مجموعة من العناصر الأبناء ينطبق عليها هذا العنصر. القيمة الافتراضية هي 0. |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden/) { get; set; } | يحصل / يحدد علامة تشير إلى ما إذا كانت هذه التسمية مخفية. القيمة الافتراضية هي **خاطئة** . |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible/) { get; } | إرجاع صحيح إذا كانت تسمية البيانات هذه بها شيء لعرضه . |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat/) { get; } | إرجاع تنسيق الأرقام للعنصر الأصل. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator/) { get; set; } | الحصول على أو تعيين فاصل السلسلة المستخدم لتسميات البيانات على الرسم البياني. الافتراضي هو الفاصلة ، باستثناء المخططات الدائرية التي تعرض اسم الفئة والنسبة المئوية فقط ، عند استخدام فاصل أسطر بدلاً من ذلك. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize/) { get; set; } | يسمح بتحديد ما إذا كان سيتم عرض حجم الفقاعة لتسميات البيانات على الرسم البياني. ينطبق فقط على المخططات الفقاعية. القيمة الافتراضية خاطئة . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname/) { get; set; } | يسمح بتحديد ما إذا كان سيتم عرض اسم الفئة لتسميات البيانات على الرسم البياني. القيمة الافتراضية خاطئة . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/) { get; set; } | يسمح بتحديد ما إذا كانت القيم من نطاق تسميات البيانات سيتم عرضها في تسميات البيانات. القيمة الافتراضية خاطئة . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines/) { get; set; } | يسمح بتحديد ما إذا كانت هناك حاجة لإظهار الخطوط البادئة لتسمية البيانات. القيمة الافتراضية خاطئة . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey/) { get; set; } | يسمح بتحديد ما إذا كان سيتم عرض مفتاح وسيلة الإيضاح لتسميات البيانات على الرسم البياني. القيمة الافتراضية خاطئة . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage/) { get; set; } | يسمح بتحديد ما إذا كان سيتم عرض قيمة النسبة المئوية لتسميات البيانات على الرسم البياني. القيمة الافتراضية خاطئة . |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname/) { get; set; } | إرجاع أو تعيين قيمة منطقية للإشارة إلى سلوك عرض اسم السلسلة لتسميات البيانات على مخطط. صحيح لإظهار اسم السلسلة. خطأ للاختباء. افتراضيا false . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue/) { get; set; } | يسمح بتحديد ما إذا كان سيتم عرض القيم في تسميات البيانات. القيمة الافتراضية خاطئة . |

## طُرق

| اسم | وصف |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat/)() | مسح تنسيق تسمية البيانات هذه. يتم تعيين الخصائص على القيم الافتراضية المحددة في البيانات الأصلية data label collection. |

### ملاحظات

في سلسلة ، ملف[`ChartDataLabel`](./chartdatalabel/) الكائن عضو في[`ChartDataLabelCollection`](../chartdatalabelcollection/) . ملف[`ChartDataLabelCollection`](../chartdatalabelcollection/) يحتوي على[`ChartDataLabel`](./chartdatalabel/) كائن لكل نقطة.

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

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
