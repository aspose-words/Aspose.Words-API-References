---
title: ChartAxis.AxisBetweenCategories
linktitle: AxisBetweenCategories
articleTitle: AxisBetweenCategories
second_title: Aspose.Words for .NET
description: 探索 ChartAxis 的 AxisBetweenCategories 属性——控制值轴的位置，增强图表中的类别可视化效果。优化您的数据呈现！
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.charts/chartaxis/axisbetweencategories/
---
## ChartAxis.AxisBetweenCategories property

获取或设置一个标志，指示数值轴是否与类别之间的类别轴相交。

```csharp
public bool AxisBetweenCategories { get; set; }
```

## 评论

此属性仅适用于数值轴。MS Office 2016 新图表不支持此属性。

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
