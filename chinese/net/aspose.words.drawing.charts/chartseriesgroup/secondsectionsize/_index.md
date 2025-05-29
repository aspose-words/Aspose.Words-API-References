---
title: ChartSeriesGroup.SecondSectionSize
linktitle: SecondSectionSize
articleTitle: SecondSectionSize
second_title: Aspose.Words for .NET
description: 了解如何调整 ChartSeriesGroup 中的 SecondSectionSize 属性以有效地自定义饼图的次要部分大小。
type: docs
weight: 90
url: /zh/net/aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/
---
## ChartSeriesGroup.SecondSectionSize property

获取或设置饼图次要部分的大小（以百分比表示）。

```csharp
public int SecondSectionSize { get; set; }
```

## 评论

适用于PieOfPieand PieOfBar类型。

可接受值的范围是 5 到 200（含）。默认值为 75。

## 例子

展示如何创建和格式化饼图。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.PieOfPie, 440, 300);
Chart chart = shape.Chart;
// 删除默认生成的系列。
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3", "Category 4" };
chart.Series.Add("Series 1", categories, new double[] { 11, 8, 4, 3 });

// 格式化饼图中的饼图。
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.GapWidth = 10;
seriesGroup.SecondSectionSize = 77;

doc.Save(ArtifactsDir + "Charts.PieOfPieChart.docx");
```

### 也可以看看

* class [ChartSeriesGroup](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
