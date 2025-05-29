---
title: ChartLegend.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words for .NET
description: 轻松自定义 ChartLegend 字体设置！访问默认格式，轻松覆盖特定图例条目，打造更美观的外观。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.charts/chartlegend/font/
---
## ChartLegend.Font property

提供对图例条目默认字体格式的访问。要覆盖特定图例条目的字体格式，请使用[`Font`](../../chartlegendentry/font/)属性.

```csharp
public Font Font { get; }
```

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

* class [Font](../../../aspose.words/font/)
* class [ChartLegend](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
