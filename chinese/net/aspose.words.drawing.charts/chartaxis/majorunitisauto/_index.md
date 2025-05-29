---
title: ChartAxis.MajorUnitIsAuto
linktitle: MajorUnitIsAuto
articleTitle: MajorUnitIsAuto
second_title: Aspose.Words for .NET
description: 探索 ChartAxis MajorUnitIsAuto 属性，轻松控制主要刻度线间距，以增强数据可视化中的图表清晰度和精确度。
type: docs
weight: 140
url: /zh/net/aspose.words.drawing.charts/chartaxis/majorunitisauto/
---
## ChartAxis.MajorUnitIsAuto property

获取或设置一个标志，指示是否应使用主刻度线之间的默认距离。

```csharp
public bool MajorUnitIsAuto { get; set; }
```

## 评论

该属性对时间类别和值轴有效。

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

* class [ChartAxis](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
