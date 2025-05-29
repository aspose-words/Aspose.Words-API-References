---
title: ChartDataLabel.ShowDataLabelsRange
linktitle: ShowDataLabelsRange
articleTitle: ShowDataLabelsRange
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "عرض نطاق علامات البيانات" (ShowDataLabelsRange) لتحسين مخططاتك البيانية من خلال عرض قيم علامات البيانات. حسّن الوضوح مع هذه الميزة السهلة!
type: docs
weight: 150
url: /ar/net/aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/
---
## ChartDataLabel.ShowDataLabelsRange property

يسمح بتحديد ما إذا كانت القيم من نطاق تسميات البيانات سيتم عرضها في تسميات البيانات. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool ShowDataLabelsRange { get; set; }
```

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

* class [ChartDataLabel](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
