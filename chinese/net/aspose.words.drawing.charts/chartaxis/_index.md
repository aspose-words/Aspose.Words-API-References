---
title: ChartAxis Class
linktitle: ChartAxis
articleTitle: ChartAxis
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Charts.ChartAxis 类，获取可自定义的图表轴选项。轻松增强您的数据可视化！
type: docs
weight: 890
url: /zh/net/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class

表示图表的轴选项。

要了解更多信息，请访问[使用图表](https://docs.aspose.com/words/net/working-with-charts/)文档文章。

```csharp
public class ChartAxis
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AxisBetweenCategories](../../aspose.words.drawing.charts/chartaxis/axisbetweencategories/) { get; set; } | 获取或设置一个标志，指示数值轴是否与类别之间的类别轴相交。 |
| [BaseTimeUnit](../../aspose.words.drawing.charts/chartaxis/basetimeunit/) { get; set; } | 返回或设置时间类别轴上表示的最小时间单位。 |
| [CategoryType](../../aspose.words.drawing.charts/chartaxis/categorytype/) { get; set; } | 获取或设置分类轴的类型。 |
| [Crosses](../../aspose.words.drawing.charts/chartaxis/crosses/) { get; set; } | 指定此轴如何与垂直轴相交。 |
| [CrossesAt](../../aspose.words.drawing.charts/chartaxis/crossesat/) { get; set; } | 指定轴在垂直轴上的交叉位置。 |
| [DisplayUnit](../../aspose.words.drawing.charts/chartaxis/displayunit/) { get; } | 指定数值轴显示单位的缩放值。 |
| [Document](../../aspose.words.drawing.charts/chartaxis/document/) { get; } | 返回包含父图表的文档。 |
| [Format](../../aspose.words.drawing.charts/chartaxis/format/) { get; } | 提供对轴的线条格式和刻度标签的填充的访问。 |
| [HasMajorGridlines](../../aspose.words.drawing.charts/chartaxis/hasmajorgridlines/) { get; set; } | 获取或设置指示轴是否有主网格线的标志。 |
| [HasMinorGridlines](../../aspose.words.drawing.charts/chartaxis/hasminorgridlines/) { get; set; } | 获取或设置指示轴是否有次要网格线的标志。 |
| [Hidden](../../aspose.words.drawing.charts/chartaxis/hidden/) { get; set; } | 获取或设置一个标志，指示该轴是否隐藏。 |
| [MajorTickMark](../../aspose.words.drawing.charts/chartaxis/majortickmark/) { get; set; } | 返回或设置主刻度线。 |
| [MajorUnit](../../aspose.words.drawing.charts/chartaxis/majorunit/) { get; set; } | 返回或设置主刻度线之间的距离。 |
| [MajorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/majorunitisauto/) { get; set; } | 获取或设置一个标志，指示是否应使用主刻度线之间的默认距离。 |
| [MajorUnitScale](../../aspose.words.drawing.charts/chartaxis/majorunitscale/) { get; set; } | 返回或设置时间类别轴上主要刻度线的刻度值。 |
| [MinorTickMark](../../aspose.words.drawing.charts/chartaxis/minortickmark/) { get; set; } | 返回或设置轴的次要刻度标记。 |
| [MinorUnit](../../aspose.words.drawing.charts/chartaxis/minorunit/) { get; set; } | 返回或设置小刻度线之间的距离。 |
| [MinorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/minorunitisauto/) { get; set; } | 获取或设置一个标志，指示是否应使用小刻度线之间的默认距离。 |
| [MinorUnitScale](../../aspose.words.drawing.charts/chartaxis/minorunitscale/) { get; set; } | 返回或设置时间类别轴上小刻度线的刻度值。 |
| [NumberFormat](../../aspose.words.drawing.charts/chartaxis/numberformat/) { get; } | 返回[`ChartNumberFormat`](../chartnumberformat/)允许定义轴的数字格式的对象。 |
| [ReverseOrder](../../aspose.words.drawing.charts/chartaxis/reverseorder/) { get; set; } | 返回或设置一个标志，指示是否应以相反的顺序显示轴的值，即 从最大值到最小值。 |
| [Scaling](../../aspose.words.drawing.charts/chartaxis/scaling/) { get; } | 提供对轴的缩放选项的访问。 |
| [TickLabels](../../aspose.words.drawing.charts/chartaxis/ticklabels/) { get; } | 提供对轴刻度标签属性的访问。 |
| [TickMarkSpacing](../../aspose.words.drawing.charts/chartaxis/tickmarkspacing/) { get; set; } | 获取或设置绘制刻度线的间隔。 |
| [Title](../../aspose.words.drawing.charts/chartaxis/title/) { get; } | 提供对轴标题属性的访问。 |
| [Type](../../aspose.words.drawing.charts/chartaxis/type/) { get; } | 返回轴的类型。 |

## 例子

展示如何插入图表并修改其轴的外观。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// 清除图表的演示数据系列以从干净的图表开始。
chart.Series.Clear();

// 插入一个图表系列，其中 X 轴为类别，Y 轴为相应的数值。
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// 图表轴有各种可以改变其外观的选项，
// 例如它们的方向、主/次单位刻度和刻度标记。
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabels.Offset = 50;
xAxis.TickLabels.Position = AxisTickLabelPosition.Low;
xAxis.TickLabels.IsAutoSpacing = false;
xAxis.TickMarkSpacing = 1;

Assert.AreEqual(doc, xAxis.Document);

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabels.Position = AxisTickLabelPosition.NextToAxis;
yAxis.TickLabels.Alignment = ParagraphAlignment.Center;
yAxis.TickLabels.Font.Color = Color.Red;
yAxis.TickLabels.Spacing = 1;

// 柱状图没有 Z 轴。
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
