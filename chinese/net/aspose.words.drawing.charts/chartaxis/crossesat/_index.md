---
title: ChartAxis.CrossesAt
linktitle: CrossesAt
articleTitle: CrossesAt
second_title: 用于 .NET 的 Aspose.Words
description: ChartAxis CrossesAt 财产. 指定轴在垂直轴上相交的位置 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

指定轴在垂直轴上相交的位置。

```csharp
public double CrossesAt { get; set; }
```

## 评论

该属性仅在以下情况下才有效：[`Crosses`](../crosses/)被设置为Custom. MS Office 2016 新图表不支持它。

单位由轴的类型决定。当轴为数值轴时，property 的值为数值轴上的十进制数。当轴是时间类别轴时，该值定义为 相对于基准日期 (30/12/1899) 的整数天数。对于文本类别轴，该值是 一个整数类别编号，从 1 开始作为第一个类别。

## 例子

演示如何使图形轴在自定义位置交叉。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// 对于柱形图，Y 轴默认交叉于零，
// 这意味着所有低于零的值的列都向下表示负值。
// 我们可以为 Y 轴交叉设置不同的值。在本例中，我们将其设置为 3。
ChartAxis axis = chart.AxisX;
axis.Crosses = AxisCrosses.Custom;
axis.CrossesAt = 3;
axis.AxisBetweenCategories = true;

doc.Save(ArtifactsDir + "Charts.AxisCross.docx");
```

### 也可以看看

* class [ChartAxis](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
