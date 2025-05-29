---
title: AxisDisplayUnit.Unit
linktitle: Unit
articleTitle: Unit
second_title: Aspose.Words for .NET
description: 探索 AxisDisplayUnit 属性，使用预定义值轻松自定义显示单位缩放，从而增强数据可视化。
type: docs
weight: 40
url: /zh/net/aspose.words.drawing.charts/axisdisplayunit/unit/
---
## AxisDisplayUnit.Unit property

获取或设置显示单位的缩放值为预定义值之一。

```csharp
public AxisBuiltInUnit Unit { get; set; }
```

## 评论

默认值为None 。 这Customand Percentage某些图表类型中没有值；see [`AxisBuiltInUnit`](../../axisbuiltinunit/)了解更多信息。

## 例子

展示如何操作图表轴的刻度线和显示值。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// 将 Y 轴的次要刻度线设置为指向远离绘图区域的方向，
// 以及穿过轴的主要刻度标记。
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// 设置 Y 轴每 10 个单位显示一个主刻度，每 1 个单位显示一个小刻度。
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// 将 Y 轴边界设置为 -10 和 20。
// 此 Y 轴现在将显示 4 个主刻度线和 27 个次刻度线。
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// 对于 X 轴，每 10 个单位设置一个主刻度线，
// 每个小刻度线为 2.5 个单位。
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// 配置两种类型的刻度标记以出现在图形绘图区域内。
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// 设置 X 轴边界，使 X 轴跨越 5 个主刻度线和 12 个次刻度线。
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabels.Alignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabels.Spacing);
Assert.AreEqual(doc, axis.DisplayUnit.Document);

// 设置刻度标签以百万为单位显示其值。
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// 我们可以设置一个更具体的值，刻度标签将通过该值显示其值。
// 该语句与上面的语句等效。
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### 也可以看看

* enum [AxisBuiltInUnit](../../axisbuiltinunit/)
* class [AxisDisplayUnit](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
