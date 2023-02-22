---
title: ChartAxis.Type
second_title: Aspose.Words لمراجع .NET API
description: ChartAxis ملكية. إرجاع نوع المحور .
type: docs
weight: 260
url: /ar/net/aspose.words.drawing.charts/chartaxis/type/
---
## ChartAxis.Type property

إرجاع نوع المحور .

```csharp
public ChartAxisType Type { get; }
```

### أمثلة

يوضح كيفية إنشاء نوع مناسب من سلاسل المخططات لنوع رسم بياني.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // هناك عدة طرق لملء مجموعة سلاسل الرسم البياني.
    // مخططات السلاسل المختلفة مخصصة لأنواع المخططات المختلفة.
    // 1 - مخطط عمودي مع أعمدة مجمعة ومجمعة على طول المحور X حسب الفئة:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // أدخل سلسلتين من القيم العشرية تحتوي على قيمة لكل فئة على حدة.
    // سيحتوي مخطط العمود هذا على ثلاث مجموعات ، كل منها بعمودين.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // يتم توزيع الفئات على طول المحور السيني ، ويتم توزيع القيم على طول المحور ص.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - مخطط مساحي بتواريخ موزعة على طول المحور السيني:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // أدخل سلسلة بقيمة عشرية لكل تاريخ على حدة.
    // سيتم توزيع التواريخ على طول محور X خطي ،
    // والقيم المضافة إلى هذه السلسلة ستنشئ نقاط بيانات.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - مخطط مبعثر ثنائي الأبعاد:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // ستحتاج كل سلسلة مصفوفتين عشريتين متساويتين في الطول.
    // تحتوي المصفوفة الأولى على قيم X ، وتحتوي الثانية على قيم Y المقابلة
    // نقاط البيانات على الرسم البياني للرسم البياني.
    chart.Series.Add("Series 1", 
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 }, 
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2", 
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 }, 
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - مخطط فقاعي:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // ستحتاج كل سلسلة إلى ثلاث مصفوفات عشرية متساوية الطول.
    // تحتوي المصفوفة الأولى على قيم X ، والثانية تحتوي على قيم Y المقابلة ،
    // والثالث يحتوي على أقطار لكل نقطة من نقاط بيانات الرسم البياني.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// قم بإدراج مخطط باستخدام منشئ المستندات من نوع ChartType المحدد والعرض والارتفاع ، وقم بإزالة بيانات العرض التوضيحي الخاصة به.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### أنظر أيضا

* enum [ChartAxisType](../../chartaxistype/)
* class [ChartAxis](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chartaxis/)
* المجسم [Aspose.Words](../../../)


