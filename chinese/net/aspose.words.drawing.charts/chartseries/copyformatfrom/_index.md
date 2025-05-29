---
title: ChartSeries.CopyFormatFrom
linktitle: CopyFormatFrom
articleTitle: CopyFormatFrom
second_title: Aspose.Words for .NET
description: 探索 ChartSeries CopyFormatFrom 方法，通过索引轻松复制数据点格式，提高图表效率和一致性。
type: docs
weight: 190
url: /zh/net/aspose.words.drawing.charts/chartseries/copyformatfrom/
---
## ChartSeries.CopyFormatFrom method

从具有指定索引的数据点复制默认数据点格式。

```csharp
public void CopyFormatFrom(int dataPointIndex)
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

* class [ChartSeries](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
