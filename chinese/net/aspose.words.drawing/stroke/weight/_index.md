---
title: Stroke.Weight
linktitle: Weight
articleTitle: Weight
second_title: Aspose.Words for .NET
description: 探索“描边粗细”属性，自定义形状的画笔粗细。使用点数精准的路径描边，提升您的设计效果！
type: docs
weight: 260
url: /zh/net/aspose.words.drawing/stroke/weight/
---
## Stroke.Weight property

定义描边形状路径的画笔粗细（以点为单位）。

```csharp
public double Weight { get; set; }
```

## 评论

默认值为[`Shape`](../../shape/)为0.75。

## 例子

显示如何改变笔触属性。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// 基本形状，例如矩形，有两个可见部分。
// 1 - 填充，适用于形状轮廓内的区域：
shape.Fill.ForeColor = Color.White;

// 2 - 笔触，标记形状的轮廓：
// 修改此形状的笔触的各种属性。
Stroke stroke = shape.Stroke;
stroke.On = true;
stroke.Weight = 5;
stroke.Color = Color.Red;
stroke.DashStyle = DashStyle.ShortDashDotDot;
stroke.JoinStyle = JoinStyle.Miter;
stroke.EndCap = EndCap.Square;
stroke.LineStyle = ShapeLineStyle.Triple;
stroke.Fill.TwoColorGradient(Color.Red, Color.Blue, GradientStyle.Vertical, GradientVariant.Variant1);

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### 也可以看看

* class [Stroke](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
