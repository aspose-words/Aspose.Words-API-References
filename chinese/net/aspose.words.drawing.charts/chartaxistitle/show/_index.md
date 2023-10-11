---
title: ChartAxisTitle.Show
second_title: Aspose.Words for .NET API 参考
description: ChartAxisTitle 财产. 确定是否应显示轴的标题 默认值为错误的.
type: docs
weight: 30
url: /zh/net/aspose.words.drawing.charts/chartaxistitle/show/
---
## ChartAxisTitle.Show property

确定是否应显示轴的标题。 默认值为`错误的`.

```csharp
public bool Show { get; set; }
```

### 例子

显示如何设置图表轴标题。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// 删除默认生成的系列。
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

// 设置轴标题。
chart.AxisX.Title.Text = "Categories";
chart.AxisX.Title.Show = true;
chart.AxisY.Title.Text = "Values";
chart.AxisY.Title.Show = true;
chart.AxisY.Title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### 也可以看看

* class [ChartAxisTitle](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../chartaxistitle/)
* 部件 [Aspose.Words](../../../)


