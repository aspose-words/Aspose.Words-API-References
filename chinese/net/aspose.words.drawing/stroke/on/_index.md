---
title: Stroke.On
linktitle: On
articleTitle: On
second_title: Aspose.Words for .NET
description: 使用“描边”属性控制路径样式。通过定义路径的描边方式来增强您的设计，打造精致专业的视觉效果。
type: docs
weight: 190
url: /zh/net/aspose.words.drawing/stroke/on/
---
## Stroke.On property

定义路径是否将被描边。

```csharp
public bool On { get; set; }
```

## 评论

默认值为[`Shape`](../../shape/)是`真的`。

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
