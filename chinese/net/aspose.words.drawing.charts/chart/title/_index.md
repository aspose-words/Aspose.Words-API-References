---
title: Chart.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words for .NET
description: 探索图表标题属性，轻松自定义并增强视觉效果。利用用户友好的功能，充分释放图表的潜力！
type: docs
weight: 120
url: /zh/net/aspose.words.drawing.charts/chart/title/
---
## Chart.Title property

提供对图表标题属性的访问。

```csharp
public ChartTitle Title { get; }
```

## 例子

展示如何插入图表和设置标题。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用文档生成器插入图表形状并获取其图表。
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// 使用“Title”属性为我们的图表添加标题，该标题显示在图表区域的顶部中心。
ChartTitle title = chart.Title;
title.Text = "My Chart";
title.Font.Size = 15;
title.Font.Color = Color.Blue;

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
