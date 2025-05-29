---
title: AxisTickLabels Class
linktitle: AxisTickLabels
articleTitle: AxisTickLabels
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Charts.AxisTickLabels 类，旨在通过可自定义的属性增强图表的轴刻度标签，以实现更好的数据可视化。
type: docs
weight: 840
url: /zh/net/aspose.words.drawing.charts/axisticklabels/
---
## AxisTickLabels class

表示轴刻度标签的属性。

```csharp
public class AxisTickLabels
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Alignment](../../aspose.words.drawing.charts/axisticklabels/alignment/) { get; set; } | 获取或设置轴刻度标签的文本对齐方式。 |
| [Font](../../aspose.words.drawing.charts/axisticklabels/font/) { get; } | 提供对刻度标签字体格式的访问。 |
| [IsAutoSpacing](../../aspose.words.drawing.charts/axisticklabels/isautospacing/) { get; set; } | 获取或设置一个标志，指示是否使用自动间隔来绘制刻度标签。 |
| [Offset](../../aspose.words.drawing.charts/axisticklabels/offset/) { get; set; } | 获取或设置刻度标签与轴的距离。 |
| [Orientation](../../aspose.words.drawing.charts/axisticklabels/orientation/) { get; set; } | 获取或设置刻度标签文本的方向。 |
| [Position](../../aspose.words.drawing.charts/axisticklabels/position/) { get; set; } | 获取或设置轴上刻度标签的位置。 |
| [Rotation](../../aspose.words.drawing.charts/axisticklabels/rotation/) { get; set; } | 获取或设置刻度标签的旋转角度（以度为单位）。 |
| [Spacing](../../aspose.words.drawing.charts/axisticklabels/spacing/) { get; set; } | 获取或设置绘制刻度标签的间隔。 |

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
