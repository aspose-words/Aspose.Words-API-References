---
title: ChartSeriesCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words لـ .NET
description: حسّن مخططاتك البيانية بسهولة باستخدام طريقة الإضافة ChartSeriesCollection. أضف سلاسل جديدة بسلاسة إلى المخططات الشريطية والعمودية والخطية والسطحية لعرض مرئي ديناميكي.
type: docs
weight: 30
url: /ar/net/aspose.words.drawing.charts/chartseriescollection/add/
---
## Add(*string, string[], double[]*) {#add_5}

يضيف جديد[`ChartSeries`](../../chartseries/) إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة إلى أي نوع من المخططات الشريطية والعمودية والخطية والسطحية.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values)
```

### قيمة الإرجاع

تمت إضافته مؤخرًا[`ChartSeries`](../../chartseries/) هدف.

## أمثلة

يوضح كيفية إنشاء مخطط باريتو.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج مخطط باريتو.
Shape shape = builder.InsertChart(ChartType.Pareto, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Best-Selling Car";

//حذف السلسلة المولدة افتراضيًا.
chart.Series.Clear();

//أضف سلسلة.
chart.Series.Add(
    "Best-Selling Car",
    new string[] { "Tesla Model Y", "Toyota Corolla", "Toyota RAV4", "Ford F-Series", "Honda CR-V" },
    new double[] { 1.43, 0.91, 1.17, 0.98, 0.85 });

doc.Save(ArtifactsDir + "Charts.Pareto.docx");
```

يوضح كيفية إنشاء مخطط قمعي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//إدراج مخطط قمعي.
Shape shape = builder.InsertChart(ChartType.Funnel, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Population by Age Group";

//حذف السلسلة المولدة افتراضيًا.
chart.Series.Clear();

//أضف سلسلة.
ChartSeries series = chart.Series.Add(
    "Population by Age Group",
    new string[] { "0-9", "10-19", "20-29", "30-39", "40-49", "50-59", "60-69", "70-79", "80-89", "90-" },
    new double[] { 0.121, 0.128, 0.132, 0.146, 0.124, 0.124, 0.111, 0.075, 0.032, 0.007 });

//إظهار تسميات البيانات.
series.HasDataLabels = true;
string decimalSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyDecimalSeparator;
series.DataLabels.NumberFormat.FormatCode = $"0{decimalSeparator}0%";

doc.Save(ArtifactsDir + "Charts.Funnel.docx");
```

يوضح كيفية إنشاء مخطط الصندوق والشارب.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل مخطط الصندوق والشارب.
Shape shape = builder.InsertChart(ChartType.BoxAndWhisker, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Points by Years";

//حذف السلسلة المولدة افتراضيًا.
chart.Series.Clear();

//أضف سلسلة.
ChartSeries series = chart.Series.Add(
    "Points by Years",
    new string[]
    {
        "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC",
        "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR",
        "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA"
    },
    new double[]
    {
        91, 80, 100, 77, 90, 104, 105, 118, 120, 101,
        114, 107, 110, 60, 79, 78, 77, 102, 101, 113,
        94, 93, 84, 71, 80, 103, 80, 94, 100, 101
    });

//إظهار تسميات البيانات.
series.HasDataLabels = true;

doc.Save(ArtifactsDir + "Charts.BoxAndWhisker.docx");
```

يوضح كيفية إنشاء نوع مناسب من سلسلة المخططات لنوع الرسم البياني.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // هناك عدة طرق لملء مجموعة السلاسل في الرسم البياني.
    // تم تصميم مخططات السلسلة المختلفة لأنواع مختلفة من المخططات.
    // 1 - مخطط عمودي يحتوي على أعمدة مجمعة ومقسمة على طول المحور X حسب الفئة:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // أدخل سلسلتين من القيم العشرية تحتويان على قيمة لكل فئة على حدة.
    // سيحتوي مخطط العمود هذا على ثلاث مجموعات، كل منها تحتوي على عمودين.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // يتم توزيع الفئات على طول المحور X، ويتم توزيع القيم على طول المحور Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - مخطط المنطقة مع التواريخ الموزعة على طول المحور X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // أدخل سلسلة بقيمة عشرية لكل تاريخ محدد.
    // سيتم توزيع التواريخ على طول المحور X الخطي،
    // والقيم المضافة إلى هذه السلسلة ستؤدي إلى إنشاء نقاط بيانات.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // رسم بياني تشتت ثلاثي الأبعاد:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // ستحتاج كل سلسلة إلى مصفوفتين عشريتين متساويتين في الطول.
    // تحتوي المصفوفة الأولى على قيم X، وتحتوي المصفوفة الثانية على قيم Y المقابلة
    // من نقاط البيانات على الرسم البياني.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - مخطط الفقاعات:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // ستحتاج كل سلسلة إلى ثلاث مصفوفات عشرية متساوية الطول.
    // تحتوي المصفوفة الأولى على قيم X، وتحتوي المصفوفة الثانية على قيم Y المقابلة،
    // والثالث يحتوي على أقطار لكل نقطة بيانات في الرسم البياني.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// قم بإدراج مخطط باستخدام منشئ المستندات لنوع مخطط معين وعرض وارتفاع، ثم قم بإزالة بياناته التجريبية.
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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)

---

## Add(*string, double[], double[]*) {#add_2}

يضيف جديد[`ChartSeries`](../../chartseries/) إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة إلى أي نوع من مخططات التشتت.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues)
```

### قيمة الإرجاع

تمت إضافته مؤخرًا[`ChartSeries`](../../chartseries/) هدف.

## أمثلة

يوضح كيفية إنشاء نوع مناسب من سلسلة المخططات لنوع الرسم البياني.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // هناك عدة طرق لملء مجموعة السلاسل في الرسم البياني.
    // تم تصميم مخططات السلسلة المختلفة لأنواع مختلفة من المخططات.
    // 1 - مخطط عمودي يحتوي على أعمدة مجمعة ومقسمة على طول المحور X حسب الفئة:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // أدخل سلسلتين من القيم العشرية تحتويان على قيمة لكل فئة على حدة.
    // سيحتوي مخطط العمود هذا على ثلاث مجموعات، كل منها تحتوي على عمودين.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // يتم توزيع الفئات على طول المحور X، ويتم توزيع القيم على طول المحور Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - مخطط المنطقة مع التواريخ الموزعة على طول المحور X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // أدخل سلسلة بقيمة عشرية لكل تاريخ محدد.
    // سيتم توزيع التواريخ على طول المحور X الخطي،
    // والقيم المضافة إلى هذه السلسلة ستؤدي إلى إنشاء نقاط بيانات.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // رسم بياني تشتت ثلاثي الأبعاد:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // ستحتاج كل سلسلة إلى مصفوفتين عشريتين متساويتين في الطول.
    // تحتوي المصفوفة الأولى على قيم X، وتحتوي المصفوفة الثانية على قيم Y المقابلة
    // من نقاط البيانات على الرسم البياني.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - مخطط الفقاعات:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // ستحتاج كل سلسلة إلى ثلاث مصفوفات عشرية متساوية الطول.
    // تحتوي المصفوفة الأولى على قيم X، وتحتوي المصفوفة الثانية على قيم Y المقابلة،
    // والثالث يحتوي على أقطار لكل نقطة بيانات في الرسم البياني.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// قم بإدراج مخطط باستخدام منشئ المستندات لنوع مخطط معين وعرض وارتفاع، ثم قم بإزالة بياناته التجريبية.
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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)

---

## Add(*string, DateTime[], double[]*) {#add_4}

يضيف جديد[`ChartSeries`](../../chartseries/) إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة إلى أي نوع من المخططات المساحية والرادارية والأسهم.

```csharp
public ChartSeries Add(string seriesName, DateTime[] dates, double[] values)
```

## أمثلة

يوضح كيفية إنشاء نوع مناسب من سلسلة المخططات لنوع الرسم البياني.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // هناك عدة طرق لملء مجموعة السلاسل في الرسم البياني.
    // تم تصميم مخططات السلسلة المختلفة لأنواع مختلفة من المخططات.
    // 1 - مخطط عمودي يحتوي على أعمدة مجمعة ومقسمة على طول المحور X حسب الفئة:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // أدخل سلسلتين من القيم العشرية تحتويان على قيمة لكل فئة على حدة.
    // سيحتوي مخطط العمود هذا على ثلاث مجموعات، كل منها تحتوي على عمودين.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // يتم توزيع الفئات على طول المحور X، ويتم توزيع القيم على طول المحور Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - مخطط المنطقة مع التواريخ الموزعة على طول المحور X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // أدخل سلسلة بقيمة عشرية لكل تاريخ محدد.
    // سيتم توزيع التواريخ على طول المحور X الخطي،
    // والقيم المضافة إلى هذه السلسلة ستؤدي إلى إنشاء نقاط بيانات.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // رسم بياني تشتت ثلاثي الأبعاد:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // ستحتاج كل سلسلة إلى مصفوفتين عشريتين متساويتين في الطول.
    // تحتوي المصفوفة الأولى على قيم X، وتحتوي المصفوفة الثانية على قيم Y المقابلة
    // من نقاط البيانات على الرسم البياني.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - مخطط الفقاعات:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // ستحتاج كل سلسلة إلى ثلاث مصفوفات عشرية متساوية الطول.
    // تحتوي المصفوفة الأولى على قيم X، وتحتوي المصفوفة الثانية على قيم Y المقابلة،
    // والثالث يحتوي على أقطار لكل نقطة بيانات في الرسم البياني.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// قم بإدراج مخطط باستخدام منشئ المستندات لنوع مخطط معين وعرض وارتفاع، ثم قم بإزالة بياناته التجريبية.
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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)

---

## Add(*string, double[], double[], double[]*) {#add_3}

يضيف جديد[`ChartSeries`](../../chartseries/) إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة إلى أي نوع من مخططات الفقاعات.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)
```

### قيمة الإرجاع

تمت إضافته مؤخرًا[`ChartSeries`](../../chartseries/) هدف.

## أمثلة

يوضح كيفية إنشاء نوع مناسب من سلسلة المخططات لنوع الرسم البياني.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // هناك عدة طرق لملء مجموعة السلاسل في الرسم البياني.
    // تم تصميم مخططات السلسلة المختلفة لأنواع مختلفة من المخططات.
    // 1 - مخطط عمودي يحتوي على أعمدة مجمعة ومقسمة على طول المحور X حسب الفئة:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // أدخل سلسلتين من القيم العشرية تحتويان على قيمة لكل فئة على حدة.
    // سيحتوي مخطط العمود هذا على ثلاث مجموعات، كل منها تحتوي على عمودين.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // يتم توزيع الفئات على طول المحور X، ويتم توزيع القيم على طول المحور Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - مخطط المنطقة مع التواريخ الموزعة على طول المحور X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // أدخل سلسلة بقيمة عشرية لكل تاريخ محدد.
    // سيتم توزيع التواريخ على طول المحور X الخطي،
    // والقيم المضافة إلى هذه السلسلة ستؤدي إلى إنشاء نقاط بيانات.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // رسم بياني تشتت ثلاثي الأبعاد:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // ستحتاج كل سلسلة إلى مصفوفتين عشريتين متساويتين في الطول.
    // تحتوي المصفوفة الأولى على قيم X، وتحتوي المصفوفة الثانية على قيم Y المقابلة
    // من نقاط البيانات على الرسم البياني.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - مخطط الفقاعات:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // ستحتاج كل سلسلة إلى ثلاث مصفوفات عشرية متساوية الطول.
    // تحتوي المصفوفة الأولى على قيم X، وتحتوي المصفوفة الثانية على قيم Y المقابلة،
    // والثالث يحتوي على أقطار لكل نقطة بيانات في الرسم البياني.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// قم بإدراج مخطط باستخدام منشئ المستندات لنوع مخطط معين وعرض وارتفاع، ثم قم بإزالة بياناته التجريبية.
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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)

---

## Add(*string, ChartMultilevelValue[], double[]*) {#add}

يضيف جديد[`ChartSeries`](../../chartseries/)إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة تحتوي على فئات بيانات متعددة المستويات.

```csharp
public ChartSeries Add(string seriesName, ChartMultilevelValue[] categories, double[] values)
```

### قيمة الإرجاع

تمت إضافته مؤخرًا[`ChartSeries`](../../chartseries/) هدف.

## أمثلة

يوضح كيفية إنشاء مخطط أشعة الشمس.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج مخطط Sunburst.
Shape shape = builder.InsertChart(ChartType.Sunburst, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Sales";

//حذف السلسلة المولدة افتراضيًا.
chart.Series.Clear();

//أضف سلسلة.
ChartSeries series = chart.Series.Add(
    "Sales",
    new ChartMultilevelValue[]
    {
        new ChartMultilevelValue("Sales - Europe", "UK", "London Dep."),
        new ChartMultilevelValue("Sales - Europe", "UK", "Liverpool Dep."),
        new ChartMultilevelValue("Sales - Europe", "UK", "Manchester Dep."),
        new ChartMultilevelValue("Sales - Europe", "France", "Paris Dep."),
        new ChartMultilevelValue("Sales - Europe", "France", "Lyon Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Denver Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Seattle Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Detroit Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Houston Dep."),
        new ChartMultilevelValue("Sales - NA", "Canada", "Toronto Dep."),
        new ChartMultilevelValue("Sales - NA", "Canada", "Montreal Dep."),
        new ChartMultilevelValue("Sales - Oceania", "Australia", "Sydney Dep."),
        new ChartMultilevelValue("Sales - Oceania", "New Zealand", "Auckland Dep.")
    },
    new double[] { 1236, 851, 536, 468, 179, 527, 799, 1148, 921, 457, 482, 761, 694 });

//إظهار تسميات البيانات.
series.HasDataLabels = true;
series.DataLabels.ShowValue = false;
series.DataLabels.ShowCategoryName = true;

doc.Save(ArtifactsDir + "Charts.Sunburst.docx");
```

يوضح كيفية إنشاء مخطط شجرة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//إدراج مخطط شجرة.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

//حذف السلسلة المولدة افتراضيًا.
chart.Series.Clear();

//أضف سلسلة.
ChartSeries series = chart.Series.Add(
    "Population by Region",
    new ChartMultilevelValue[]
    {
        new ChartMultilevelValue("Asia", "China"),
        new ChartMultilevelValue("Asia", "India"),
        new ChartMultilevelValue("Asia", "Indonesia"),
        new ChartMultilevelValue("Asia", "Pakistan"),
        new ChartMultilevelValue("Asia", "Bangladesh"),
        new ChartMultilevelValue("Asia", "Japan"),
        new ChartMultilevelValue("Asia", "Philippines"),
        new ChartMultilevelValue("Asia", "Other"),
        new ChartMultilevelValue("Africa", "Nigeria"),
        new ChartMultilevelValue("Africa", "Ethiopia"),
        new ChartMultilevelValue("Africa", "Egypt"),
        new ChartMultilevelValue("Africa", "Other"),
        new ChartMultilevelValue("Europe", "Russia"),
        new ChartMultilevelValue("Europe", "Germany"),
        new ChartMultilevelValue("Europe", "Other"),
        new ChartMultilevelValue("Latin America", "Brazil"),
        new ChartMultilevelValue("Latin America", "Mexico"),
        new ChartMultilevelValue("Latin America", "Other"),
        new ChartMultilevelValue("Northern America", "United States", "Other"),
        new ChartMultilevelValue("Northern America", "Other"),
        new ChartMultilevelValue("Oceania")
    },
    new double[]
    {
        1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000,
        223800000, 107334000, 105914499, 903000000,
        146150789, 84607016, 516000000,
        203080756, 129713690, 310000000,
        335893238, 35000000,
        42000000
    });

//إظهار تسميات البيانات.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### أنظر أيضا

* class [ChartSeries](../../chartseries/)
* class [ChartMultilevelValue](../../chartmultilevelvalue/)
* class [ChartSeriesCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)

---

## Add(*string, double[]*) {#add_1}

يضيف جديد[`ChartSeries`](../../chartseries/) إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة إلى مخططات الهيستوغرام.

```csharp
public ChartSeries Add(string seriesName, double[] xValues)
```

### قيمة الإرجاع

تمت إضافته مؤخرًا[`ChartSeries`](../../chartseries/) هدف.

## ملاحظات

بالنسبة لأنواع المخططات الأخرى غير الهيستوجرام، تضيف هذه الطريقة سلسلة تحتوي على قيم Y فارغة.

## أمثلة

يوضح كيفية إنشاء مخطط الهيستوجرام.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//إدراج مخطط الهيستوجرام.
Shape shape = builder.InsertChart(ChartType.Histogram, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Avg Temperature since 1991";

//حذف السلسلة المولدة افتراضيًا.
chart.Series.Clear();

//أضف سلسلة.
chart.Series.Add(
    "Avg Temperature",
    new double[]
    {
        51.8, 53.6, 50.3, 54.7, 53.9, 54.3, 53.4, 52.9, 53.3, 53.7, 53.8, 52.0, 55.0, 52.1, 53.4,
        53.8, 53.8, 51.9, 52.1, 52.7, 51.8, 56.6, 53.3, 55.6, 56.3, 56.2, 56.1, 56.2, 53.6, 55.7,
        56.3, 55.9, 55.6
    });

doc.Save(ArtifactsDir + "Charts.Histogram.docx");
```

### أنظر أيضا

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)

---

## Add(*string, string[], double[], bool[]*) {#add_6}

يضيف جديد[`ChartSeries`](../../chartseries/) إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلسلة إلى مخططات الشلال.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values, bool[] isSubtotal)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| seriesName | String | اسم السلسلة المراد إضافتها. |
| categories | String[] | أسماء الفئات لمحور X. |
| values | Double[] | قيم المحور Y. |
| isSubtotal | Boolean[] | القيم التي تشير إلى ما إذا كانت قيمة Y المقابلة عبارة عن مجموع فرعي. |

### قيمة الإرجاع

تمت إضافته مؤخرًا[`ChartSeries`](../../chartseries/) هدف.

## ملاحظات

لأنواع المخططات الأخرى غير الشلال،*isSubtotal* يتم تجاهل القيم.

## أمثلة

يوضح كيفية إنشاء مخطط الشلال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//إدراج مخطط الشلال.
Shape shape = builder.InsertChart(ChartType.Waterfall, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "New Zealand GDP";

//حذف السلسلة المولدة افتراضيًا.
chart.Series.Clear();

//أضف سلسلة.
ChartSeries series = chart.Series.Add(
    "New Zealand GDP",
    new string[] { "2018", "2019 growth", "2020 growth", "2020", "2021 growth", "2022 growth", "2022" },
    new double[] { 100, 0.57, -0.25, 100.32, 20.22, -2.92, 117.62 },
    new bool[] { true, false, false, true, false, false, true });

//إظهار تسميات البيانات.
series.HasDataLabels = true;

doc.Save(ArtifactsDir + "Charts.Waterfall.docx");
```

### أنظر أيضا

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
