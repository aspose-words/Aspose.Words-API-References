---
title: Fill.TwoColorGradient
linktitle: TwoColorGradient
articleTitle: TwoColorGradient
second_title: 用于 .NET 的 Aspose.Words
description: Fill TwoColorGradient 方法. 将指定填充设置为二色渐变 在 C#.
type: docs
weight: 260
url: /zh/net/aspose.words.drawing/fill/twocolorgradient/
---
## TwoColorGradient(*[GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/)*) {#twocolorgradient}

将指定填充设置为二色渐变。

```csharp
public void TwoColorGradient(GradientStyle style, GradientVariant variant)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| style | GradientStyle | 渐变风格[`GradientStyle`](../../gradientstyle/)。 |
| variant | GradientVariant | 梯度变体[`GradientVariant`](../../gradientvariant/) |

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

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)

---

## TwoColorGradient(*Color, Color, [GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/)*) {#twocolorgradient_1}

将指定填充设置为二色渐变。

```csharp
public void TwoColorGradient(Color color1, Color color2, GradientStyle style, 
    GradientVariant variant)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| color1 | Color | 构建渐变的第一个颜色。 |
| color2 | Color | 用于构建渐变的第二种颜色。 |
| style | GradientStyle | 渐变风格[`GradientStyle`](../../gradientstyle/)。 |
| variant | GradientVariant | 梯度变体[`GradientVariant`](../../gradientvariant/) |

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

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
