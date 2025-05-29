---
title: ChartTitle Class
linktitle: ChartTitle
articleTitle: ChartTitle
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Charts.ChartTitle 类，轻松管理和自定义图表标题，以增强数据可视化。
type: docs
weight: 1140
url: /zh/net/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class

提供对图表标题属性的访问。

要了解更多信息，请访问[使用 图表](https://docs.aspose.com/words/net/working-with-charts/)文档文章。

```csharp
public class ChartTitle
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/charttitle/font/) { get; } | 提供对图表标题字体格式的访问。 |
| [Format](../../aspose.words.drawing.charts/charttitle/format/) { get; } | 提供对图表标题的填充和线条格式的访问。 |
| [Overlay](../../aspose.words.drawing.charts/charttitle/overlay/) { get; set; } | 确定是否允许其他图表元素覆盖标题。 默认情况下覆盖是`错误的`. |
| [Show](../../aspose.words.drawing.charts/charttitle/show/) { get; set; } | 确定是否显示此图表的标题。 默认值为`真的`. |
| [Text](../../aspose.words.drawing.charts/charttitle/text/) { get; set; } | 获取或设置图表标题的文本。 如果`无效的`或者指定空值，将显示自动生成的标题。 |

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

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
