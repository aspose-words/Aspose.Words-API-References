---
title: Chart.Series
second_title: Aspose.Words for .NET API 参考
description: Chart 财产. 提供对系列集合的访问
type: docs
weight: 60
url: /zh/net/aspose.words.drawing.charts/chart/series/
---
## Chart.Series property

提供对系列集合的访问。

```csharp
public ChartSeriesCollection Series { get; }
```

### 例子

展示如何为图形类型创建适当类型的图表系列。

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 有多种方法可以填充图表的系列集合。
    // 不同的系列模式适用于不同的图表类型。
    // 1 - 柱形图，其中的柱按类别沿 X 轴分组和排列：
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // 插入两个系列的十进制值，其中包含每个相应类别的值。
    // 此柱形图将包含三组，每组有两列。
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // 类别沿X轴分布，值沿Y轴分布。
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

    // 为每个相应日期插入一个带有十进制值的系列。
    // 日期将沿线性 X 轴分布，
    // 添加到该系列的值将创建数据点。
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D 散点图：
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // 每个系列都需要两个长度相等的十进制数组。
    // 第一个数组包含 X 值，第二个数组包含相应的 Y 值
    // 图表上的数据点。
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

    // 每个系列需要三个长度相等的十进制数组。
    // 第一个数组包含 X 值，第二个数组包含相应的 Y 值，
    // 第三个包含图表每个数据点的直径。
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// 使用指定图表类型、宽度和高度的文档生成器插入图表，并删除其演示数据。
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

* class [ChartSeriesCollection](../../chartseriescollection/)
* class [Chart](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../chart/)
* 部件 [Aspose.Words](../../../)


