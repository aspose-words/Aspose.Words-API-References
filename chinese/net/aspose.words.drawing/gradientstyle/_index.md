---
title: GradientStyle Enum
linktitle: GradientStyle
articleTitle: GradientStyle
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.GradientStyle 枚举以获得可自定义的渐变填充样式，通过生动的视觉效果增强您的文档设计。
type: docs
weight: 1330
url: /zh/net/aspose.words.drawing/gradientstyle/
---
## GradientStyle enumeration

指定渐变填充的样式。

```csharp
public enum GradientStyle
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `-1` | 无渐变。 |
| Horizontal | `1` | 渐变水平穿过物体。 |
| Vertical | `2` | 渐变垂直延伸至物体。 |
| DiagonalUp | `3` | 对角渐变从底角向上移动到对角。 |
| DiagonalDown | `4` | 对角渐变从顶角向下移动到对角。 |
| FromCorner | `5` | 渐变从一个角延伸到其他三个角。 |
| FromCenter | `6` | 渐变从中心延伸到角落。 |

## 例子

展示如何用渐变填充形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 对具有渐变填充前景色的形状应用单色渐变填充。
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 对形状应用双色渐变填充。
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// 改变渐变填充的背景颜色。
shape.Fill.BackColor = Color.Yellow;
// 注意将“GradientAngle”更改为“GradientStyle.FromCorner/GradientStyle.FromCenter”
// 渐变填充不会产生任何效果，它只对线性渐变起作用。
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// 如果要获得“GradientStyle”，请使用合规性选项通过 DML 定义形状，
// 文档保存后的“GradientVariant”和“GradientAngle”属性。
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
