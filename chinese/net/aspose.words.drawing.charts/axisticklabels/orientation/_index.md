---
title: AxisTickLabels.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words for .NET
description: 自定义 AxisTickLabels 方向，获得最佳可读性。轻松调整刻度标签文本方向，提升数据可视化效果！
type: docs
weight: 50
url: /zh/net/aspose.words.drawing.charts/axisticklabels/orientation/
---
## AxisTickLabels.Orientation property

获取或设置刻度标签文本的方向。

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## 评论

默认值为Horizontal。

请注意，一些[`ShapeTextOrientation`](../../../aspose.words.drawing/shapetextorientation/)值不会影响数值轴上刻度标签 text 的方向。

## 例子

展示如何更改轴刻度标签的方向和旋转。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入柱形图。
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
AxisTickLabels xTickLabels = shape.Chart.AxisX.TickLabels;
AxisTickLabels yTickLabels = shape.Chart.AxisY.TickLabels;

// 设置轴刻度标签的方向和旋转。
xTickLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
xTickLabels.Rotation = -30;
yTickLabels.Orientation = ShapeTextOrientation.Horizontal;
yTickLabels.Rotation = 45;

doc.Save(ArtifactsDir + "Charts.TickLabelsOrientationRotation.docx");
```

### 也可以看看

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [AxisTickLabels](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
