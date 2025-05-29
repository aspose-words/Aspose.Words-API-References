---
title: ChartLegendEntry Class
linktitle: ChartLegendEntry
articleTitle: ChartLegendEntry
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.ChartLegendEntry 类，用于创建动态图表图例。通过无缝集成和自定义功能，增强您的数据可视化效果。
type: docs
weight: 1020
url: /zh/net/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class

表示图表图例条目。

要了解更多信息，请访问[使用图表](https://docs.aspose.com/words/net/working-with-charts/)文档文章。

```csharp
public class ChartLegendEntry
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegendentry/font/) { get; } | 提供对此图例条目的字体格式的访问。 |
| [IsHidden](../../aspose.words.drawing.charts/chartlegendentry/ishidden/) { get; set; } | 获取或设置一个值，指示此条目是否隐藏在图表图例中。 默认值为**错误的**. |

## 评论

图例条目对应于特定的图表系列或趋势线。

条目的文本是系列或趋势线的名称。文本无法更改。

## 例子

展示如何使用图例字体。

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

ChartLegend chartLegend = chart.Legend;
// 设置所有图例条目的默认字体大小。
chartLegend.Font.Size = 14;
// 更改特定图例条目的字体。
chartLegend.LegendEntries[1].Font.Italic = true;
chartLegend.LegendEntries[1].Font.Size = 12;
// 获取图表系列的图例条目。
ChartLegendEntry legendEntry = chart.Series[0].LegendEntry;

doc.Save(ArtifactsDir + "Charts.LegendFont.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
