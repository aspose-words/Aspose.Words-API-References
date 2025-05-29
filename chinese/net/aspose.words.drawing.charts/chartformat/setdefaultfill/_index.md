---
title: ChartFormat.SetDefaultFill
linktitle: SetDefaultFill
articleTitle: SetDefaultFill
second_title: Aspose.Words for .NET
description: 了解如何使用 ChartFormat SetDefaultFill 方法轻松地将图表元素的填充恢复为其原始默认值。
type: docs
weight: 50
url: /zh/net/aspose.words.drawing.charts/chartformat/setdefaultfill/
---
## ChartFormat.SetDefaultFill method

将图表元素的填充重置为默认值。

```csharp
public void SetDefaultFill()
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
