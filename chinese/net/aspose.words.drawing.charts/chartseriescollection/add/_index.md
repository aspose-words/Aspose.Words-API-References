---
title: ChartSeriesCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: 使用 ChartSeriesCollection 的 Add 方法轻松增强您的图表。无缝添加新系列到条形图、柱形图、折线图和曲面图，打造动态视觉效果。
type: docs
weight: 30
url: /zh/net/aspose.words.drawing.charts/chartseriescollection/add/
---
## Add(*string, string[], double[]*) {#add_5}

添加新的[`ChartSeries`](../../chartseries/)到此集合。 使用此方法将系列添加到任何类型的条形图、柱形图、折线图和曲面图。

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values)
```

### 返回值

最近添加[`ChartSeries`](../../chartseries/)目的。

## 例子

显示如何创建帕累托图。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入帕累托图。
Shape shape = builder.InsertChart(ChartType.Pareto, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Best-Selling Car";

// 删除默认生成的系列。
chart.Series.Clear();

// 添加一个系列。
chart.Series.Add(
    "Best-Selling Car",
    new string[] { "Tesla Model Y", "Toyota Corolla", "Toyota RAV4", "Ford F-Series", "Honda CR-V" },
    new double[] { 1.43, 0.91, 1.17, 0.98, 0.85 });

doc.Save(ArtifactsDir + "Charts.Pareto.docx");
```

展示如何创建漏斗图。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入漏斗图。
Shape shape = builder.InsertChart(ChartType.Funnel, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Population by Age Group";

// 删除默认生成的系列。
chart.Series.Clear();

// 添加一个系列。
ChartSeries series = chart.Series.Add(
    "Population by Age Group",
    new string[] { "0-9", "10-19", "20-29", "30-39", "40-49", "50-59", "60-69", "70-79", "80-89", "90-" },
    new double[] { 0.121, 0.128, 0.132, 0.146, 0.124, 0.124, 0.111, 0.075, 0.032, 0.007 });

// 显示数据标签。
series.HasDataLabels = true;
string decimalSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyDecimalSeparator;
series.DataLabels.NumberFormat.FormatCode = $"0{decimalSeparator}0%";

doc.Save(ArtifactsDir + "Charts.Funnel.docx");
```

展示如何创建箱线图。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入箱线图。
Shape shape = builder.InsertChart(ChartType.BoxAndWhisker, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Points by Years";

// 删除默认生成的系列。
chart.Series.Clear();

// 添加一个系列。
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

// 显示数据标签。
series.HasDataLabels = true;

doc.Save(ArtifactsDir + "Charts.BoxAndWhisker.docx");
```

展示如何为图表类型创建适当类型的图表系列。

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 有几种方法可以填充图表的系列集合。
    // 不同的系列模式适用于不同的图表类型。
    // 1 - 柱状图，其中柱子按类别沿 X 轴分组并带状排列：
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // 插入两系列十进制值，每个系列包含一个相应类别的值。
    // 此柱状图将有三组，每组有两列。
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // 类别沿 X 轴分布，值沿 Y 轴分布。
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - 日期沿 X 轴分布的面积图：
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // 为每个相应的日期插入一个带有十进制值的系列。
    // 日期将沿线性 X 轴分布，
    // 并且添加到该系列的值将创建数据点。
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 二维散点图：
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // 每个系列需要两个等长的十进制数组。
    // 第一个数组包含 X 值，第二个数组包含相应的 Y 值
    // 图表图形上的数据点。
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - 气泡图：
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // 每个系列需要三个等长的十进制数组。
    // 第一个数组包含 X 值，第二个数组包含相应的 Y 值，
    // 第三个包含图形中每个数据点的直径。
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// 使用指定 ChartType、宽度和高度的文档构建器插入图表，并删除其演示数据。
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### 也可以看看

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)

---

## Add(*string, double[], double[]*) {#add_2}

添加新的[`ChartSeries`](../../chartseries/)到此集合。 使用此方法将系列添加到任何类型的散点图。

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues)
```

### 返回值

最近添加[`ChartSeries`](../../chartseries/)目的。

## 例子

展示如何为图表类型创建适当类型的图表系列。

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 有几种方法可以填充图表的系列集合。
    // 不同的系列模式适用于不同的图表类型。
    // 1 - 柱状图，其中柱子按类别沿 X 轴分组并带状排列：
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // 插入两系列十进制值，每个系列包含一个相应类别的值。
    // 此柱状图将有三组，每组有两列。
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // 类别沿 X 轴分布，值沿 Y 轴分布。
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - 日期沿 X 轴分布的面积图：
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // 为每个相应的日期插入一个带有十进制值的系列。
    // 日期将沿线性 X 轴分布，
    // 并且添加到该系列的值将创建数据点。
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 二维散点图：
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // 每个系列需要两个等长的十进制数组。
    // 第一个数组包含 X 值，第二个数组包含相应的 Y 值
    // 图表图形上的数据点。
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - 气泡图：
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // 每个系列需要三个等长的十进制数组。
    // 第一个数组包含 X 值，第二个数组包含相应的 Y 值，
    // 第三个包含图形中每个数据点的直径。
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// 使用指定 ChartType、宽度和高度的文档构建器插入图表，并删除其演示数据。
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### 也可以看看

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)

---

## Add(*string, DateTime[], double[]*) {#add_4}

添加新的[`ChartSeries`](../../chartseries/)到此集合。 使用此方法将系列添加到任何类型的区域、雷达和股票图表。

```csharp
public ChartSeries Add(string seriesName, DateTime[] dates, double[] values)
```

## 例子

展示如何为图表类型创建适当类型的图表系列。

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 有几种方法可以填充图表的系列集合。
    // 不同的系列模式适用于不同的图表类型。
    // 1 - 柱状图，其中柱子按类别沿 X 轴分组并带状排列：
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // 插入两系列十进制值，每个系列包含一个相应类别的值。
    // 此柱状图将有三组，每组有两列。
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // 类别沿 X 轴分布，值沿 Y 轴分布。
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - 日期沿 X 轴分布的面积图：
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // 为每个相应的日期插入一个带有十进制值的系列。
    // 日期将沿线性 X 轴分布，
    // 并且添加到该系列的值将创建数据点。
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 二维散点图：
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // 每个系列需要两个等长的十进制数组。
    // 第一个数组包含 X 值，第二个数组包含相应的 Y 值
    // 图表图形上的数据点。
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - 气泡图：
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // 每个系列需要三个等长的十进制数组。
    // 第一个数组包含 X 值，第二个数组包含相应的 Y 值，
    // 第三个包含图形中每个数据点的直径。
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// 使用指定 ChartType、宽度和高度的文档构建器插入图表，并删除其演示数据。
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### 也可以看看

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)

---

## Add(*string, double[], double[], double[]*) {#add_3}

添加新的[`ChartSeries`](../../chartseries/)到此集合。 使用此方法将系列添加到任何类型的气泡图。

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)
```

### 返回值

最近添加[`ChartSeries`](../../chartseries/)目的。

## 例子

展示如何为图表类型创建适当类型的图表系列。

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 有几种方法可以填充图表的系列集合。
    // 不同的系列模式适用于不同的图表类型。
    // 1 - 柱状图，其中柱子按类别沿 X 轴分组并带状排列：
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // 插入两系列十进制值，每个系列包含一个相应类别的值。
    // 此柱状图将有三组，每组有两列。
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // 类别沿 X 轴分布，值沿 Y 轴分布。
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - 日期沿 X 轴分布的面积图：
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // 为每个相应的日期插入一个带有十进制值的系列。
    // 日期将沿线性 X 轴分布，
    // 并且添加到该系列的值将创建数据点。
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 二维散点图：
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // 每个系列需要两个等长的十进制数组。
    // 第一个数组包含 X 值，第二个数组包含相应的 Y 值
    // 图表图形上的数据点。
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - 气泡图：
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // 每个系列需要三个等长的十进制数组。
    // 第一个数组包含 X 值，第二个数组包含相应的 Y 值，
    // 第三个包含图形中每个数据点的直径。
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// 使用指定 ChartType、宽度和高度的文档构建器插入图表，并删除其演示数据。
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### 也可以看看

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)

---

## Add(*string, ChartMultilevelValue[], double[]*) {#add}

添加新的[`ChartSeries`](../../chartseries/)到此集合。 使用此方法添加具有多级数据类别的系列。

```csharp
public ChartSeries Add(string seriesName, ChartMultilevelValue[] categories, double[] values)
```

### 返回值

最近添加[`ChartSeries`](../../chartseries/)目的。

## 例子

展示如何创建旭日图。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入旭日图。
Shape shape = builder.InsertChart(ChartType.Sunburst, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Sales";

// 删除默认生成的系列。
chart.Series.Clear();

// 添加一个系列。
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

// 显示数据标签。
series.HasDataLabels = true;
series.DataLabels.ShowValue = false;
series.DataLabels.ShowCategoryName = true;

doc.Save(ArtifactsDir + "Charts.Sunburst.docx");
```

展示如何创建树状图。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入树状图。
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

// 删除默认生成的系列。
chart.Series.Clear();

// 添加一个系列。
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

// 显示数据标签。
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### 也可以看看

* class [ChartSeries](../../chartseries/)
* class [ChartMultilevelValue](../../chartmultilevelvalue/)
* class [ChartSeriesCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)

---

## Add(*string, double[]*) {#add_1}

添加新的[`ChartSeries`](../../chartseries/)到此集合。 使用此方法将系列添加到直方图。

```csharp
public ChartSeries Add(string seriesName, double[] xValues)
```

### 返回值

最近添加[`ChartSeries`](../../chartseries/)目的。

## 评论

对于直方图以外的图表类型，此方法添加具有空 Y 值的系列。

## 例子

展示如何创建直方图。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入直方图。
Shape shape = builder.InsertChart(ChartType.Histogram, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Avg Temperature since 1991";

// 删除默认生成的系列。
chart.Series.Clear();

// 添加一个系列。
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

### 也可以看看

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)

---

## Add(*string, string[], double[], bool[]*) {#add_6}

添加新的[`ChartSeries`](../../chartseries/)到此集合。 使用此方法将系列添加到瀑布图。

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values, bool[] isSubtotal)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| seriesName | String | 要添加的系列的名称。 |
| categories | String[] | X 轴的类别名称。 |
| values | Double[] | Y 轴值。 |
| isSubtotal | Boolean[] | 指示相应 Y 值是否为小计的值。 |

### 返回值

最近添加[`ChartSeries`](../../chartseries/)目的。

## 评论

对于瀑布图以外的图表类型，*isSubtotal*值被忽略。

## 例子

展示如何创建瀑布图。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入瀑布图。
Shape shape = builder.InsertChart(ChartType.Waterfall, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "New Zealand GDP";

// 删除默认生成的系列。
chart.Series.Clear();

// 添加一个系列。
ChartSeries series = chart.Series.Add(
    "New Zealand GDP",
    new string[] { "2018", "2019 growth", "2020 growth", "2020", "2021 growth", "2022 growth", "2022" },
    new double[] { 100, 0.57, -0.25, 100.32, 20.22, -2.92, 117.62 },
    new bool[] { true, false, false, true, false, false, true });

// 显示数据标签。
series.HasDataLabels = true;

doc.Save(ArtifactsDir + "Charts.Waterfall.docx");
```

### 也可以看看

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
