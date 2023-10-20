---
title: ChartAxisType Enum
linktitle: ChartAxisType
articleTitle: ChartAxisType
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.Charts.ChartAxisType تعداد. يحدد نوع محور المخطط في C#.
type: docs
weight: 660
url: /ar/net/aspose.words.drawing.charts/chartaxistype/
---
## ChartAxisType enumeration

يحدد نوع محور المخطط.

```csharp
public enum ChartAxisType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Category | `0` | محور الفئة في المخطط. |
| Series | `1` | محور السلسلة للمخطط. |
| Value | `2` | محور القيمة للمخطط. |

## أمثلة

يوضح كيفية إنشاء نوع مناسب من سلسلة المخططات لنوع الرسم البياني.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // هناك عدة طرق لملء مجموعة سلاسل المخطط.
    // مخططات السلاسل المختلفة مخصصة لأنواع مختلفة من المخططات.
    // 1 - مخطط عمودي يحتوي على أعمدة مجمعة ومحددة على طول المحور السيني حسب الفئة:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // أدخل سلسلتين من القيم العشرية التي تحتوي على قيمة لكل فئة.
    // سيحتوي هذا المخطط العمودي على ثلاث مجموعات، تحتوي كل منها على عمودين.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // يتم توزيع الفئات على طول المحور X، ويتم توزيع القيم على طول المحور Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - مخطط مساحي مع تواريخ موزعة على طول المحور السيني:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // أدخل سلسلة ذات قيمة عشرية لكل تاريخ.
    // سيتم توزيع التواريخ على طول المحور السيني الخطي،
    // والقيم المضافة إلى هذه السلسلة ستنشئ نقاط بيانات.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - مخطط مبعثر ثنائي الأبعاد:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // ستحتاج كل سلسلة إلى صفيفين عشريين متساويين في الطول.
    // يحتوي المصفوفة الأولى على قيم X، والثانية تحتوي على قيم Y المقابلة
    // نقاط البيانات على الرسم البياني للمخطط.
    chart.Series.Add("Series 1", 
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 }, 
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2", 
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 }, 
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - المخطط الفقاعي:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // ستحتاج كل سلسلة إلى ثلاث صفائف عشرية متساوية الطول.
    // يحتوي المصفوفة الأولى على قيم X، والثانية تحتوي على قيم Y المقابلة،
    // والثالث يحتوي على أقطار لكل نقطة من نقاط بيانات الرسم البياني.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// قم بإدراج مخطط باستخدام أداة إنشاء المستندات ذات نوع المخطط المحدد وعرضه وارتفاعه، ثم قم بإزالة بيانات العرض التوضيحي الخاصة به.
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

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
