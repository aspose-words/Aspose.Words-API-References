---
title: ShapeLineStyle Enum
linktitle: ShapeLineStyle
articleTitle: ShapeLineStyle
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.ShapeLineStyle 枚举，使用可自定义的形状复合线条样式来增强文档设计。
type: docs
weight: 1660
url: /zh/net/aspose.words.drawing/shapelinestyle/
---
## ShapeLineStyle enumeration

指定复合线样式[`Shape`](../shape/).

```csharp
public enum ShapeLineStyle
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Single | `0` | 单行。 |
| Double | `1` | 等宽双线。 |
| ThickThin | `2` | 双线，一条粗，一条细。 |
| ThinThick | `3` | 双线，一细一粗。 |
| Triple | `4` | 三条线，细，粗，细。 |
| Default | `0` | 默认值为Single. |

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

* property [LineStyle](../stroke/linestyle/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
