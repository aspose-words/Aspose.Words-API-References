---
title: Enum ChartType
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.Charts.ChartType 枚举. 指定图表的类型
type: docs
weight: 760
url: /zh/net/aspose.words.drawing.charts/charttype/
---
## ChartType enumeration

指定图表的类型。

```csharp
public enum ChartType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Area | `0` | 面积图。 |
| AreaStacked | `1` | 堆积面积图。 |
| AreaPercentStacked | `2` | 100% 堆积面积图。 |
| Area3D | `3` | 3D 面积图。 |
| Area3DStacked | `4` | 3D 堆积面积图。 |
| Area3DPercentStacked | `5` | 3D 100% 堆积面积图。 |
| Bar | `6` | 条形图. |
| BarStacked | `7` | 堆积条形图。 |
| BarPercentStacked | `8` | 100% 堆积条形图。 |
| Bar3D | `9` | 3D 条形图。 |
| Bar3DStacked | `10` | 3D 堆积条形图。 |
| Bar3DPercentStacked | `11` | 3D 100% 堆积条形图。 |
| Bubble | `12` | 气泡图. |
| Bubble3D | `13` | 3D 气泡图。 |
| Column | `14` | 柱形图. |
| ColumnStacked | `15` | 堆积柱形图。 |
| ColumnPercentStacked | `16` | 100% 堆积柱形图。 |
| Column3D | `17` | 3D 柱形图。 |
| Column3DStacked | `18` | 3D 堆积柱形图。 |
| Column3DPercentStacked | `19` | 3D 100% 堆积柱形图。 |
| Column3DClustered | `20` | 3D 聚集柱形图。 |
| Doughnut | `21` | 圆环图。 |
| Line | `22` | 折线图。 |
| LineStacked | `23` | 堆积折线图。 |
| LinePercentStacked | `24` | 100% 堆积折线图。 |
| Line3D | `25` | 3D 折线图。 |
| Pie | `26` | 饼图。 |
| Pie3D | `27` | 3D 饼图。 |
| PieOfBar | `28` | 条形图饼图。 |
| PieOfPie | `29` | 饼图。 |
| Radar | `30` | 雷达图。 |
| Scatter | `31` | 散点图. |
| Stock | `32` | 股票图表. |
| Surface | `33` | 曲面图. |
| Surface3D | `34` | 3D 曲面图。 |

### 例子

展示如何为图表类型创建适当类型的图表系列。

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 有几种方法可以填充图表的系列集合。
    // 不同的系列模式适用于不同的图表类型。
    // 1 - 柱形图，柱形图按类别沿 X 轴分组和带状：
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // 插入两个系列的十进制值，其中包含每个相应类别的值。
    // 这个柱形图将有三组，每组有两列。
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

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

    // 为每个日期插入一个带有十进制值的系列。
    // 日期将沿线性 X 轴分布，
    // 添加到这个系列的值将创建数据点。
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - 2D 散点图：
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // 每个系列都需要两个长度相等的十进制数组。
    // 第一个数组包含 X 值，第二个包含对应的 Y 值
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

    // 每个系列都需要三个等长的十进制数组。
    // 第一个数组包含 X 值，第二个包含对应的 Y 值，
    // 第三个包含每个图形数据点的直径。
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

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

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)


