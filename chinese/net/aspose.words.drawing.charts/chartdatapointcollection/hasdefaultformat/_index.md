---
title: ChartDataPointCollection.HasDefaultFormat
linktitle: HasDefaultFormat
articleTitle: HasDefaultFormat
second_title: Aspose.Words for .NET
description: 了解 ChartDataPointCollection 中特定索引处的数据点是否使用默认格式。立即增强您的数据可视化！
type: docs
weight: 60
url: /zh/net/aspose.words.drawing.charts/chartdatapointcollection/hasdefaultformat/
---
## ChartDataPointCollection.HasDefaultFormat method

获取一个标志，指示指定索引处的数据点是否具有默认格式。

```csharp
public bool HasDefaultFormat(int dataPointIndex)
```

## 例子

显示如何复制数据点格式。

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

// 获取图表和系列以更新格式。
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPointCollection dataPoints = series.DataPoints;

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsFalse(dataPoints.HasDefaultFormat(1));

// 将索引 1 的数据点的格式复制到索引 2 的数据点
// 这样数据点 2 看起来就与数据点 1 相同。
dataPoints.CopyFormat(0, 1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

// 将索引 0 的数据点格式复制到系列默认值，以便所有数据点
// 在具有默认格式的系列中看起来与数据点 0 相同。
series.CopyFormatFrom(1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

doc.Save(ArtifactsDir + "Charts.CopyDataPointFormat.docx");
```

### 也可以看看

* class [ChartDataPointCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
