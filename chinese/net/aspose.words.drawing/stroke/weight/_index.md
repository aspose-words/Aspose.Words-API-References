---
title: Stroke.Weight
linktitle: Weight
articleTitle: Weight
second_title: 用于 .NET 的 Aspose.Words
description: Stroke Weight 财产. 以点为单位定义描边形状路径的画笔厚度 在 C#.
type: docs
weight: 210
url: /zh/net/aspose.words.drawing/stroke/weight/
---
## Stroke.Weight property

以点为单位定义描边形状路径的画笔厚度。

```csharp
public double Weight { get; set; }
```

## 评论

的默认值[`Shape`](../../shape/)为 0.75。

## 例子

显示如何更改笔触属性。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// 基本形状，例如矩形，有两个可见部分。
// 1 - 填充，应用于形状轮廓内的区域：
shape.Fill.ForeColor = Color.White;

// 2 - 描边，标记形状的轮廓：
// 修改这个形状的笔画的各种属性。
Stroke stroke = shape.Stroke;
stroke.On = true;
stroke.Weight = 5;
stroke.Color = Color.Red;
stroke.DashStyle = DashStyle.ShortDashDotDot;
stroke.JoinStyle = JoinStyle.Miter;
stroke.EndCap = EndCap.Square;
stroke.LineStyle = ShapeLineStyle.Triple;

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### 也可以看看

* class [Stroke](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
