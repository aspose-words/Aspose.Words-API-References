---
title: ChartDataLabelCollection.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words for .NET
description: 调整 ChartDataLabelCollection 的旋转角度，以获得最佳可视性。自定义数据标签角度，增强图表的可读性和影响力。
type: docs
weight: 80
url: /zh/net/aspose.words.drawing.charts/chartdatalabelcollection/rotation/
---
## ChartDataLabelCollection.Rotation property

获取或设置整个系列的数据标签的旋转角度（以度为单位）。

```csharp
public int Rotation { get; set; }
```

## 评论

可接受值的范围是 -180 到 180（含）。默认值为 0。

如果[`Orientation`](../orientation/)值是Horizontal、标签形状、 （如果存在）将随标签文本一起旋转。否则，仅标签文本旋转。

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

* class [ChartDataLabelCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
