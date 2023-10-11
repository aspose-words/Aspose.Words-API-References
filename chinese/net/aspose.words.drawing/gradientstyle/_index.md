---
title: Enum GradientStyle
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.GradientStyle 枚举. 指定渐变填充的样式
type: docs
weight: 1000
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
| Horizontal | `1` | 渐变水平穿过对象。 |
| Vertical | `2` | 垂直向下对象的渐变。 |
| DiagonalUp | `3` | 从底角到对角的对角渐变。 |
| DiagonalDown | `4` | 从顶角向下移动到对角的对角渐变。 |
| FromCorner | `5` | 从一个角到其他三个角的渐变。 |
| FromCenter | `6` | 从中心向外到角落的渐变。 |

### 例子

演示如何使用渐变填充形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 使用渐变填充的前景色对形状应用一种颜色渐变填充。
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 对形状应用双色渐变填充。
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// 更改渐变填充的背景颜色。
shape.Fill.BackColor = Color.Yellow;
// 请注意，将“GradientAngle”更改为“GradientStyle.FromCorner/GradientStyle.FromCenter”
// 渐变填充不会产生任何效果，它仅适用于线性渐变。
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// 如果你想获得“GradientStyle”，请使用compliance选项通过DML定义形状，
// 文档保存后的“GradientVariant”和“GradientAngle”属性。
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)


