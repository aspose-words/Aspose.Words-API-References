---
title: ChartTitle.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words for .NET
description: 使用可自定义的标题增强您的图表。轻松控制可见性 - 默认为 True。立即提升您的数据呈现效果！
type: docs
weight: 40
url: /zh/net/aspose.words.drawing.charts/charttitle/show/
---
## ChartTitle.Show property

确定是否显示此图表的标题。 默认值为`真的`.

```csharp
public bool Show { get; set; }
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

* class [ChartTitle](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
