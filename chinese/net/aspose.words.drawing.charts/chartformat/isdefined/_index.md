---
title: ChartFormat.IsDefined
linktitle: IsDefined
articleTitle: IsDefined
second_title: Aspose.Words for .NET
description: 使用 ChartFormat IsDefined 属性检查格式是否已定义。立即解锁图表的无缝格式控制！
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.charts/chartformat/isdefined/
---
## ChartFormat.IsDefined property

获取一个标志，指示是否定义了任何格式。

```csharp
public bool IsDefined { get; }
```

## 例子

显示如何将填充重置为系列中定义的默认值。

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPoint dataPoint = series.DataPoints[1];

Assert.IsTrue(dataPoint.Format.IsDefined);

dataPoint.Format.SetDefaultFill();

doc.Save(ArtifactsDir + "Charts.ResetDataPointFill.docx");
```

### 也可以看看

* class [ChartFormat](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
