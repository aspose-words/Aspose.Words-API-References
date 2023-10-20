---
title: ChartTitle.Overlay
linktitle: Overlay
articleTitle: Overlay
second_title: 用于 .NET 的 Aspose.Words
description: ChartTitle Overlay 财产. 确定是否允许其他图表元素重叠 title. 默认情况下覆盖为 false 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.charts/charttitle/overlay/
---
## ChartTitle.Overlay property

确定是否允许其他图表元素重叠 title. 默认情况下覆盖为 false。

```csharp
public bool Overlay { get; set; }
```

## 例子

显示如何插入图表和设置标题。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用文档构建器插入图表形状并获取其图表。
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// 使用“Title”属性给我们的图表一个标题，它出现在图表区域的顶部中心。
ChartTitle title = chart.Title;
title.Text = "My Chart";

 // 将“Show”属性设置为“true”以使标题可见。
title.Show = true;

// 将“Overlay”属性设置为“true”，允许其他图表元素与标题重叠，从而为它们提供更多空间
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### 也可以看看

* class [ChartTitle](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
