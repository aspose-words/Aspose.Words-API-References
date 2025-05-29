---
title: ChartSeriesGroupCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: 发现 ChartSeriesGroupCollection 的 Count 属性，它揭示了增强数据可视化的系列组的总数。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.charts/chartseriesgroupcollection/count/
---
## ChartSeriesGroupCollection.Count property

返回此集合中的系列组数。

```csharp
public int Count { get; }
```

## 例子

展示如何删除次轴。

```csharp
Document doc = new Document(MyDir + "Combo chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;
ChartSeriesGroupCollection seriesGroups = chart.SeriesGroups;

// 找到次轴并从集合中删除。
for (int i = 0; i < seriesGroups.Count; i++)
    if (seriesGroups[i].AxisGroup == AxisGroup.Secondary)
        seriesGroups.RemoveAt(i);
```

### 也可以看看

* class [ChartSeriesGroupCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
