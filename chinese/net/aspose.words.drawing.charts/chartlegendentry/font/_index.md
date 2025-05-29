---
title: ChartLegendEntry.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words for .NET
description: 发现 ChartLegendEntry Font 属性，轻松访问可自定义的字体格式，增强图例条目以获得更好的视觉吸引力。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.charts/chartlegendentry/font/
---
## ChartLegendEntry.Font property

提供对此图例条目的字体格式的访问。

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
* class [ChartLegendEntry](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
