---
title: AxisTickLabels.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words for .NET
description: 调整 AxisTickLabels 旋转以获得最佳可读性。自定义刻度标签角度（以度为单位），以增强图表的清晰度和视觉吸引力。
type: docs
weight: 70
url: /zh/net/aspose.words.drawing.charts/axisticklabels/rotation/
---
## AxisTickLabels.Rotation property

获取或设置刻度标签的旋转角度（以度为单位）。

```csharp
public int Rotation { get; set; }
```

## 评论

可接受值的范围是 -180 到 180（含）。默认值为 0。

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

* class [AxisTickLabels](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
