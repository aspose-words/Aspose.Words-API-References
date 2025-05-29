---
title: ChartDataLabel.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words for .NET
description: 探索 ChartDataLabel 旋转属性，轻松自定义图表中的标签角度。精准控制，提升数据可视化效果！
type: docs
weight: 110
url: /zh/net/aspose.words.drawing.charts/chartdatalabel/rotation/
---
## ChartDataLabel.Rotation property

获取或设置标签的旋转角度（以度为单位）。

```csharp
public int Rotation { get; set; }
```

## 评论

可接受值的范围是 -180 到 180（含）。默认值为 0。

如果[`Orientation`](../orientation/)值是Horizontal，则 标签形状（如果存在）将随标签文本一起旋转。否则，仅标签文本旋转。

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

* class [ChartDataLabel](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
