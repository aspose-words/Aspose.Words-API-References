---
title: Chart Class
linktitle: Chart
articleTitle: Chart
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.Drawing.Charts.Chart 类解锁强大的图表形状属性。通过动态可视化数据呈现增强您的文档。
type: docs
weight: 880
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
| [AxisX](../../aspose.words.drawing.charts/chart/axisx/) { get; } | 提供对图表主要 X 轴属性的访问。 |
| [AxisY](../../aspose.words.drawing.charts/chart/axisy/) { get; } | 提供对图表主 Y 轴属性的访问。 |
| [AxisZ](../../aspose.words.drawing.charts/chart/axisz/) { get; } | 提供对图表 Z 轴属性的访问。 |
| [DataTable](../../aspose.words.drawing.charts/chart/datatable/) { get; } | 提供对此图表数据表属性的访问。 可以使用[`Show`](../chartdatatable/show/)属性. |
| [Format](../../aspose.words.drawing.charts/chart/format/) { get; } | 提供对图表填充和线条格式的访问。 |
| [Legend](../../aspose.words.drawing.charts/chart/legend/) { get; } | 提供对图表图例属性的访问。 |
| [Series](../../aspose.words.drawing.charts/chart/series/) { get; } | 提供对系列收藏的访问。 |
| [SeriesGroups](../../aspose.words.drawing.charts/chart/seriesgroups/) { get; } | 提供对此图表的系列组集合的访问。 |
| [SourceFullName](../../aspose.words.drawing.charts/chart/sourcefullname/) { get; set; } | 获取此图表链接到的 xls/xlsx 文件的路径和名称。 |
| [Style](../../aspose.words.drawing.charts/chart/style/) { get; set; } | 获取或设置图表的样式。 |
| [Title](../../aspose.words.drawing.charts/chart/title/) { get; } | 提供对图表标题属性的访问。 |

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
