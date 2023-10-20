---
title: AxisDisplayUnit.Unit
linktitle: Unit
articleTitle: Unit
second_title: 用于 .NET 的 Aspose.Words
description: AxisDisplayUnit Unit 财产. 获取或设置显示单位的缩放值作为预定义值之一 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.drawing.charts/axisdisplayunit/unit/
---
## AxisDisplayUnit.Unit property

获取或设置显示单位的缩放值作为预定义值之一。

```csharp
public AxisBuiltInUnit Unit { get; set; }
```

## 评论

默认值为None 。这Custom和 Percentage某些图表类型中不提供值；参见 [`AxisBuiltInUnit`](../../axisbuiltinunit/)了解更多信息。

## 例子

演示如何操作图表轴的刻度线和显示值。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// 将 Y 轴的小刻度线设置为远离绘图区域，
// 以及与轴交叉的主要刻度线。
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// 将 Y 轴设置为每 10 个单位显示一个主要刻度，每 1 个单位显示一个次要刻度。
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// 将 Y 轴界限设置为 -10 和 20。
// 此 Y 轴现在将显示 4 个主要刻度线和 27 个次要刻度线。
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// 对于 X 轴，每 10 个单位设置一次主要刻度线，
// 2.5 单位处的每个小刻度线。
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// 配置两种类型的刻度线以显示在图形绘图区域内。
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// 设置 X 轴边界，使 X 轴跨越 5 个主要刻度线和 12 个次要刻度线。
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabelAlignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabelSpacing);

// 设置刻度标签以显示其值（以百万为单位）。
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// 我们可以设置一个更具体的值，刻度标签将通过该值显示其值。
// 这个语句和上面的语句是等价的。
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### 也可以看看

* enum [AxisBuiltInUnit](../../axisbuiltinunit/)
* class [AxisDisplayUnit](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
