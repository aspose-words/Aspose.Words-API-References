---
title: ShapeTextOrientation Enum
linktitle: ShapeTextOrientation
articleTitle: ShapeTextOrientation
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.ShapeTextOrientation 枚举，轻松控制形状中的文本方向，增强文档设计和可读性。
type: docs
weight: 1680
url: /zh/net/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enumeration

指定形状中文本的方向。

```csharp
public enum ShapeTextOrientation
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Horizontal | `0` | 文本水平排列 (lr-tb)。 |
| Downward | `1` | 文本向右旋转 90 度，从上到下显示 (tb-rl)。 |
| Upward | `2` | 文本向左旋转 90 度，从下到上显示 (bt-lr)。 |
| VerticalFarEast | `3` | 远东字符垂直显示，其他文本向右旋转 90 度 从上到下显示（tb-rl-v）。 |
| VerticalRotatedFarEast | `4` | 远东字符垂直显示，其他文本向右旋转 90 度 ，从上到下垂直显示，然后从左到右水平显示（tb-lr-v）。 |
| WordArtVertical | `5` | 文本是垂直的，一个字母位于另一个字母之上。 |
| WordArtVerticalRightToLeft | `6` | 文本是垂直的，一个字母在另一个字母上面，然后从右到左水平排列。 |

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

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
