---
title: Enum ChartType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.Charts.ChartType تعداد. يحدد نوع المخطط.
type: docs
weight: 830
url: /ar/net/aspose.words.drawing.charts/charttype/
---
## ChartType enumeration

يحدد نوع المخطط.

```csharp
public enum ChartType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Area | `0` | مخطط مساحي. |
| AreaStacked | `1` | مخطط مساحي مكدس. |
| AreaPercentStacked | `2` | مخطط مساحي مكدس بنسبة 100%. |
| Area3D | `3` | مخطط مساحي ثلاثي الأبعاد. |
| Area3DStacked | `4` | مخطط مساحي مكدس ثلاثي الأبعاد. |
| Area3DPercentStacked | `5` | مخطط مساحي مكدس بنسبة 100% ثلاثي الأبعاد. |
| Bar | `6` | مخطط شريطي. |
| BarStacked | `7` | مخطط شريطي مكدس. |
| BarPercentStacked | `8` | مخطط شريطي مكدس بنسبة 100%. |
| Bar3D | `9` | مخطط شريطي ثلاثي الأبعاد. |
| Bar3DStacked | `10` | مخطط شريطي مكدس ثلاثي الأبعاد. |
| Bar3DPercentStacked | `11` | مخطط شريطي مكدس بنسبة 100% ثلاثي الأبعاد. |
| Bubble | `12` | المخطط الفقاعي. |
| Bubble3D | `13` | مخطط فقاعي ثلاثي الأبعاد. |
| Column | `14` | مخطط عمودي. |
| ColumnStacked | `15` | مخطط عمودي مكدس. |
| ColumnPercentStacked | `16` | مخطط عمودي مكدس بنسبة 100%. |
| Column3D | `17` | مخطط عمودي ثلاثي الأبعاد. |
| Column3DStacked | `18` | مخطط عمودي مكدس ثلاثي الأبعاد. |
| Column3DPercentStacked | `19` | مخطط عمودي مكدس بنسبة 100% ثلاثي الأبعاد. |
| Column3DClustered | `20` | مخطط عمودي متفاوت المسافات ثلاثي الأبعاد. |
| Doughnut | `21` | المخطط الدائري المجوف. |
| Line | `22` | مخطط خطي. |
| LineStacked | `23` | مخطط خطي مكدس. |
| LinePercentStacked | `24` | مخطط خطي مكدس بنسبة 100%. |
| Line3D | `25` | مخطط خطي ثلاثي الأبعاد. |
| Pie | `26` | مخطط دائري. |
| Pie3D | `27` | مخطط دائري ثلاثي الأبعاد. |
| PieOfBar | `28` | مخطط دائري للمخطط الشريطي. |
| PieOfPie | `29` | مخطط دائري. |
| Radar | `30` | مخطط راداري. |
| Scatter | `31` | المخطط المبعثر. |
| Stock | `32` | مخطط الأسهم. |
| Surface | `33` | مخطط سطحي. |
| Surface3D | `34` | مخطط سطحي ثلاثي الأبعاد. |

### أمثلة

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


