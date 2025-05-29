---
title: ChartSeries.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words for .NET
description: 探索 ChartSeries 格式属性，轻松访问可自定义的填充和线条样式，增强您的数据可视化体验。
type: docs
weight: 60
url: /zh/net/aspose.words.drawing.charts/chartseries/format/
---
## ChartSeries.Format property

提供对系列填充和线条格式的访问。

```csharp
public ChartFormat Format { get; }
```

## 例子

播种如何设置系列颜色。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// 删除默认生成的系列。
seriesColl.Clear();

// 创建类别名称数组。
string[] categories = new[] { "Category 1", "Category 2" };

// 添加新系列。值和类别数组的大小必须相同。
ChartSeries series1 = seriesColl.Add("Series 1", categories, new double[] { 1, 2 });
ChartSeries series2 = seriesColl.Add("Series 2", categories, new double[] { 3, 4 });
ChartSeries series3 = seriesColl.Add("Series 3", categories, new double[] { 5, 6 });

// 设置系列颜色。
series1.Format.Fill.ForeColor = Color.Red;
series2.Format.Fill.ForeColor = Color.Yellow;
series3.Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.SeriesColor.docx");
```

### 也可以看看

* class [ChartFormat](../../chartformat/)
* class [ChartSeries](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
