---
title: ChartSeriesGroup.FirstSliceAngle
linktitle: FirstSliceAngle
articleTitle: FirstSliceAngle
second_title: Aspose.Words for .NET
description: 探索 ChartSeriesGroup FirstSliceAngle 属性，以度为单位自定义饼图的第一个切片角度，从而增强数据可视化。
type: docs
weight: 60
url: /zh/net/aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/
---
## ChartSeriesGroup.FirstSliceAngle property

获取或设置父饼图第一片的角度（以度为单位）。

```csharp
public int FirstSliceAngle { get; set; }
```

## 评论

适用于Pie，Pie3D 和Doughnut类型。

可接受值的范围是 0 到 360（含）。默认值为 0。

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
