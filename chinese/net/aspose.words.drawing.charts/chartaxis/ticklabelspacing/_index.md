---
title: ChartAxis.TickLabelSpacing
linktitle: TickLabelSpacing
articleTitle: TickLabelSpacing
second_title: 用于 .NET 的 Aspose.Words
description: ChartAxis TickLabelSpacing 财产. 获取或设置绘制刻度标签的时间间隔 在 C#.
type: docs
weight: 250
url: /zh/net/aspose.words.drawing.charts/chartaxis/ticklabelspacing/
---
## ChartAxis.TickLabelSpacing property

获取或设置绘制刻度标签的时间间隔。

```csharp
public int TickLabelSpacing { get; set; }
```

## 评论

该属性对文本类别和系列轴有效。 MS Office 2016 新图表不支持它。值的有效范围大于或等于 1。

设置此属性会设置[`TickLabelSpacingIsAuto`](../ticklabelspacingisauto/)财产**错误的**.

## 例子

显示如何操作刻度线和图表轴的显示值。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// 将 Y 轴的小刻度线设置为远离绘图区域，
// 和跨轴的主要刻度线。
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// 将它们的 Y 轴设置为每 10 个单位显示一个主要刻度，每 1 个单位显示一个次要刻度。
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// 将 Y 轴范围设置为 -10 和 20。
// 这个 Y 轴现在将显示 4 个主要刻度线和 27 个次要刻度线。
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// 对于 X 轴，每 10 个单位设置一次主刻度线，
// 2.5 个单位的每个次要刻度线。
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// 将两种类型的刻度线配置为出现在图形绘图区域内。
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// 设置 X 轴边界，使 X 轴跨越 5 个主要刻度线和 12 个次要刻度线。
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabelAlignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabelSpacing);

// 将刻度标签设置为以百万为单位显示它们的值。
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// 我们可以设置一个更具体的值，刻度标签将通过该值显示它们的值。
// 这个语句和上面那个是等价的。
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### 也可以看看

* class [ChartAxis](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
