---
title: ChartAxis.CrossesAt
linktitle: CrossesAt
articleTitle: CrossesAt
second_title: Aspose.Words for .NET
description: 探索 ChartAxis CrossesAt 属性，轻松定义图表垂直轴上的交叉点，以增强数据可视化。
type: docs
weight: 50
url: /zh/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

指定轴在垂直轴上的交叉位置。

```csharp
public double CrossesAt { get; set; }
```

## 评论

仅当该属性有效时[`Crosses`](../crosses/)设置为Custom. 它不受 MS Office 2016 新图表支持。

单位由轴的类型决定。当轴为数值轴时，属性 的值为数值轴上的小数。当轴为时间类别轴时，该值定义为 （相对于基准日期 (1899/12/30) 的整数天数）。对于文本类别轴，该值为 （整数类别编号，从 1 开始作为第一个类别）。

## 例子

展示如何让图形轴在自定义位置交叉。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// 对于柱形图，Y 轴默认与零点相交，
// 这意味着所有低于零的值的列都指向下方以表示负值。
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
