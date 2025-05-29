---
title: ChartDataLabelCollection.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words for .NET
description: 探索 ChartDataLabelCollection Orientation 属性，轻松自定义数据标签的文本方向，增强图表的清晰度和影响力。
type: docs
weight: 60
url: /zh/net/aspose.words.drawing.charts/chartdatalabelcollection/orientation/
---
## ChartDataLabelCollection.Orientation property

获取或设置整个系列的数据标签的文本方向。

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## 评论

默认值为Horizontal.

## 例子

展示如何更改数据标签的方向和旋转。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
ChartSeries series = shape.Chart.Series[0];
ChartDataLabelCollection dataLabels = series.DataLabels;

// 显示数据标签。
series.HasDataLabels = true;
dataLabels.ShowValue = true;
dataLabels.ShowCategoryName = true;

// 定义数据标签形状。
dataLabels.Format.ShapeType = ChartShapeType.UpArrow;
dataLabels.Format.Stroke.Fill.Solid(Color.DarkBlue);

// 为整个系列设置数据标签方向和旋转。
dataLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
dataLabels.Rotation = -45;

// 改变第一个数据标签的方向和旋转。
dataLabels[0].Orientation = ShapeTextOrientation.Horizontal;
dataLabels[0].Rotation = 45;

doc.Save(ArtifactsDir + "Charts.LabelOrientationRotation.docx");
```

### 也可以看看

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [ChartDataLabelCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
