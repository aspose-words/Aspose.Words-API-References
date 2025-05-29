---
title: ChartFormat Class
linktitle: ChartFormat
articleTitle: ChartFormat
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.ChartFormat 类，实现高级图表元素样式设置。使用专业、可定制的图表设计增强您的文档。
type: docs
weight: 1000
url: /zh/net/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class

表示图表元素的格式。

要了解更多信息，请访问[使用图表](https://docs.aspose.com/words/net/working-with-charts/)文档文章。

```csharp
public class ChartFormat
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Fill](../../aspose.words.drawing.charts/chartformat/fill/) { get; } | 获取父图表元素的填充格式。 |
| [IsDefined](../../aspose.words.drawing.charts/chartformat/isdefined/) { get; } | 获取一个标志，指示是否定义了任何格式。 |
| [ShapeType](../../aspose.words.drawing.charts/chartformat/shapetype/) { get; set; } | 获取或设置父图表元素的形状类型。 |
| [Stroke](../../aspose.words.drawing.charts/chartformat/stroke/) { get; } | 获取父图表元素的线条格式。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [SetDefaultFill](../../aspose.words.drawing.charts/chartformat/setdefaultfill/)() | 将图表元素的填充重置为默认值。 |

## 例子

展示如何使用图表格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// 删除默认生成的系列。
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// 格式化图表背景。
chart.Format.Fill.Solid(Color.DarkSlateGray);

// 隐藏轴刻度标签。
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// 格式化图表标题。
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// 格式化轴标题。
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// 格式化图例。
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
