---
title: Class ChartAxisCollection
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.Charts.ChartAxisCollection 班级. 表示图表轴的集合
type: docs
weight: 640
url: /zh/net/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class

表示图表轴的集合。

```csharp
public class ChartAxisCollection : IEnumerable<ChartAxis>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartaxiscollection/count/) { get; } | 获取此集合中的轴数。 |
| [Item](../../aspose.words.drawing.charts/chartaxiscollection/item/) { get; } | 获取指定索引处的轴。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartaxiscollection/getenumerator/)() | 返回一个枚举器对象。 |

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

* class [ChartAxis](../chartaxis/)
* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)


