---
title: Stroke.LineStyle
second_title: Aspose.Words for .NET API 参考
description: Stroke 财产. 定义笔画的线条样式
type: docs
weight: 140
url: /zh/net/aspose.words.drawing/stroke/linestyle/
---
## Stroke.LineStyle property

定义笔画的线条样式。

```csharp
public ShapeLineStyle LineStyle { get; set; }
```

### 评论

默认值为Single。

### 例子

显示如何更改笔划属性。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// 基本形状，例如矩形，有两个可见部分。
// 1 - 填充，适用于形状轮廓内的区域：
shape.Fill.ForeColor = Color.White;

// 2 - 笔划，标记形状的轮廓：
// 修改该形状笔划的各种属性。
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

* enum [ShapeLineStyle](../../shapelinestyle/)
* class [Stroke](../)
* 命名空间 [Aspose.Words.Drawing](../../stroke/)
* 部件 [Aspose.Words](../../../)


