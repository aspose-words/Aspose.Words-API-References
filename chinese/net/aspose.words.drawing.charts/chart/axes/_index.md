---
title: Chart.Axes
second_title: Aspose.Words for .NET API 参考
description: Chart 财产. 获取此图表所有轴的集合
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.charts/chart/axes/
---
## Chart.Axes property

获取此图表所有轴的集合。

```csharp
public ChartAxisCollection Axes { get; }
```

### 例子

展示如何使用轴集合。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;            

// 隐藏主要和次要 Y 轴上的主要网格线。
foreach (ChartAxis axis in chart.Axes)
{
    if (axis.Type == ChartAxisType.Value)
        axis.HasMajorGridlines = false;
}

doc.Save(ArtifactsDir + "Charts.AxisCollection.docx");
```

### 也可以看看

* class [ChartAxisCollection](../../chartaxiscollection/)
* class [Chart](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../chart/)
* 部件 [Aspose.Words](../../../)


