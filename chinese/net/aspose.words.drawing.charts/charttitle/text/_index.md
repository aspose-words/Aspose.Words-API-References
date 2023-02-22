---
title: ChartTitle.Text
second_title: Aspose.Words for .NET API 参考
description: ChartTitle 财产. 获取或设置图表标题的文本 如果指定null或空值将显示自动生成的标题
type: docs
weight: 30
url: /zh/net/aspose.words.drawing.charts/charttitle/text/
---
## ChartTitle.Text property

获取或设置图表标题的文本。 如果指定null或空值，将显示自动生成的标题。

```csharp
public string Text { get; set; }
```

### 评论

利用[`Show`](../show/)如果您需要隐藏标题，请选择此选项。

### 例子

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
* 命名空间 [Aspose.Words.Drawing.Charts](../../charttitle/)
* 部件 [Aspose.Words](../../../)


