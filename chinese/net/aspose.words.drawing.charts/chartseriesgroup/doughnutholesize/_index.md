---
title: ChartSeriesGroup.DoughnutHoleSize
linktitle: DoughnutHoleSize
articleTitle: DoughnutHoleSize
second_title: Aspose.Words for .NET
description: 探索 ChartSeriesGroup DoughnutHoleSize 属性，轻松自定义圆环图的孔大小百分比，以增强数据可视化。
type: docs
weight: 50
url: /zh/net/aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/
---
## ChartSeriesGroup.DoughnutHoleSize property

获取或设置父级圆环图的孔径大小（以百分比表示）。

```csharp
public int DoughnutHoleSize { get; set; }
```

## 评论

仅适用于Doughnut类型。

可接受值的范围是 0 到 90（含）。默认值为 75。

## 例子

展示如何创建和格式化圆环图。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Doughnut, 400, 400);
Chart chart = shape.Chart;
// 删除默认生成的系列。
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
chart.Series.Add("Series 1", categories, new double[] { 4, 2, 5 });

// 格式化圆环图。
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.DoughnutHoleSize = 10;
seriesGroup.FirstSliceAngle = 270;

doc.Save(ArtifactsDir + "Charts.DoughnutChart.docx");
```

### 也可以看看

* class [ChartSeriesGroup](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
