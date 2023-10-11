---
title: Class Chart
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.Charts.Chart 班级. 提供对图表形状属性的访问
type: docs
weight: 620
url: /zh/net/aspose.words.drawing.charts/chart/
---
## Chart class

提供对图表形状属性的访问。

要了解更多信息，请访问[使用图表](https://docs.aspose.com/words/net/working-with-charts/)文档文章。

```csharp
public class Chart
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Axes](../../aspose.words.drawing.charts/chart/axes/) { get; } | 获取此图表所有轴的集合。 |
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | 提供对图表 X 轴属性的访问。 |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | 提供对图表 Y 轴属性的访问。 |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | 提供对图表 Z 轴属性的访问。 |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | 提供对图表图例属性的访问。 |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | 提供对系列集合的访问。 |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | 获取此图表链接到的 xls/xlsx 文件的路径和名称。 |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | 提供对图表标题属性的访问。 |

### 例子

演示如何插入图表并设置标题。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用文档生成器插入图表形状并获取其图表。
Shape chartShape = builder.InsertChart(ChartType.Bar, 400, 300);
Chart chart = chartShape.Chart;

// 使用“Title”属性为图表指定标题，该标题显示在图表区域的顶部中心。
ChartTitle title = chart.Title;
title.Text = "My Chart";

 // 将“Show”属性设置为“true”以使标题可见。
title.Show = true;

// 将“Overlay”属性设置为“true”，允许其他图表元素与标题重叠，从而为它们提供更多空间
title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartTitle.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)


