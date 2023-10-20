---
title: ChartAxisTitle.Text
linktitle: Text
articleTitle: Text
second_title: 用于 .NET 的 Aspose.Words
description: ChartAxisTitle Text 财产. 获取或设置轴标题的文本 如果无效的或指定空值将显示自动生成的标题 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.drawing.charts/chartaxistitle/text/
---
## ChartAxisTitle.Text property

获取或设置轴标题的文本。 如果`无效的`或指定空值，将显示自动生成的标题。

```csharp
public string Text { get; set; }
```

## 评论

使用[`Show`](../show/)如果您需要显示标题，请选择。

## 例子

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
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
