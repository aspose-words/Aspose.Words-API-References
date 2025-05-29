---
title: Stroke.Fill
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words for .NET
description: 探索“描边填充”属性，增强设计中的填充格式。立即通过精准的描边自定义功能，提升您的项目质量！
type: docs
weight: 120
url: /zh/net/aspose.words.drawing/stroke/fill/
---
## Stroke.Fill property

获取填充格式[`Stroke`](../).

```csharp
public Fill Fill { get; }
```

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

* class [Fill](../../fill/)
* class [Stroke](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
