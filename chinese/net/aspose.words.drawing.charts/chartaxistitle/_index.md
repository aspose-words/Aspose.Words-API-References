---
title: ChartAxisTitle Class
linktitle: ChartAxisTitle
articleTitle: ChartAxisTitle
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.ChartAxisTitle 类以轻松管理轴标题属性并增强文档的视觉效果。
type: docs
weight: 910
url: /zh/net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

提供对轴标题属性的访问。

要了解更多信息，请访问[使用 图表](https://docs.aspose.com/words/net/working-with-charts/)文档文章。

```csharp
public class ChartAxisTitle
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartaxistitle/font/) { get; } | 提供对轴标题字体格式的访问。 |
| [Format](../../aspose.words.drawing.charts/chartaxistitle/format/) { get; } | 提供对轴标题的填充和线条格式的访问。 |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | 确定是否允许其他图表元素与标题重叠。 默认值为`错误的`. |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | 确定是否显示轴的标题。 默认值为`错误的`. |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | 获取或设置轴标题的文本。 如果`无效的`或者指定空值，将显示自动生成的标题。 |

## 例子

显示如何设置图表轴标题。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// 删除默认生成的系列。
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

ChartAxisTitle chartAxisXTitle = chart.AxisX.Title;
chartAxisXTitle.Text = "Categories";
chartAxisXTitle.Show = true;
ChartAxisTitle chartAxisYTitle = chart.AxisY.Title;
chartAxisYTitle.Text = "Values";
chartAxisYTitle.Show = true;
chartAxisYTitle.Overlay = true;
chartAxisYTitle.Font.Size = 12;
chartAxisYTitle.Font.Color = Color.Blue;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
