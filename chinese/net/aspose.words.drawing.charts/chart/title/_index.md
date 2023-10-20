---
title: Chart.Title
linktitle: Title
articleTitle: Title
second_title: 用于 .NET 的 Aspose.Words
description: Chart Title 财产. 提供对图表标题属性的访问 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words.drawing.charts/chart/title/
---
## Chart.Title property

提供对图表标题属性的访问。

```csharp
public ChartTitle Title { get; }
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

* class [ChartTitle](../../charttitle/)
* class [Chart](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
