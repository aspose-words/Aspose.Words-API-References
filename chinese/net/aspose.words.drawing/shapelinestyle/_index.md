---
title: ShapeLineStyle Enum
linktitle: ShapeLineStyle
articleTitle: ShapeLineStyle
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.ShapeLineStyle 枚举. 指定复合线样式Shape 在 C#.
type: docs
weight: 1270
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
| ThickThin | `2` | 双线，一粗一细。 |
| ThinThick | `3` | 双线，一根细，一根粗。 |
| Triple | `4` | 三行，细，粗，细。 |
| Default | `0` | 默认值为Single. |

## 例子

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

* property [LineStyle](../stroke/linestyle/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
