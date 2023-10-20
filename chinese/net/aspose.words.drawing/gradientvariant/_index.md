---
title: GradientVariant Enum
linktitle: GradientVariant
articleTitle: GradientVariant
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.GradientVariant 枚举. 指定渐变填充的变体 在 C#.
type: docs
weight: 1010
url: /zh/net/aspose.words.drawing/gradientvariant/
---
## GradientVariant enumeration

指定渐变填充的变体。

```csharp
public enum GradientVariant
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 渐变变体“无”。 |
| Variant1 | `1` | 梯度变体 1. |
| Variant2 | `2` | 梯度变体 2. |
| Variant3 | `3` | 梯度变体 3. |
| Variant4 | `4` | 梯度变体 4. |

## 评论

对应于 Word 中“填充效果”对话框中“渐变”选项卡上的四种变体。

## 例子

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
