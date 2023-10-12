---
title: ChartDataLabel.ShowDataLabelsRange
second_title: Aspose.Words لمراجع .NET API
description: ChartDataLabel ملكية. يسمح بتحديد ما إذا كانت القيم من تسميات البيانات سيتم عرضها في تسميات البيانات. القيمة الافتراضية هيخطأ شنيع .
type: docs
weight: 100
url: /ar/net/aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/
---
## ChartDataLabel.ShowDataLabelsRange property

يسمح بتحديد ما إذا كانت القيم من تسميات البيانات سيتم عرضها في تسميات البيانات. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ShowDataLabelsRange { get; set; }
```

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

* class [ChartDataLabel](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chartdatalabel/)
* المجسم [Aspose.Words](../../../)


