---
title: Fill.OneColorGradient
linktitle: OneColorGradient
articleTitle: OneColorGradient
second_title: Aspose.Words for .NET
description: 探索如何使用 OneColorGradient 方法为您的设计创建令人惊叹的单色渐变效果。轻松提升您的项目效果！
type: docs
weight: 220
url: /zh/net/aspose.words.drawing/fill/onecolorgradient/
---
## OneColorGradient(*[GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/), double*) {#onecolorgradient}

将指定的填充设置为单色渐变。

```csharp
public void OneColorGradient(GradientStyle style, GradientVariant variant, double degree)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| style | GradientStyle | 渐变风格[`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | 渐变变体[`GradientVariant`](../../gradientvariant/) |
| degree | Double | 渐变程度。取值范围为 0.0（暗）到 1.0（亮）。 |

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

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)

---

## OneColorGradient(*Color, [GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/), double*) {#onecolorgradient_1}

使用指定颜色将指定填充设置为单色渐变。

```csharp
public void OneColorGradient(Color color, GradientStyle style, GradientVariant variant, 
    double degree)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| color | Color | 构建渐变的颜色。 |
| style | GradientStyle | 渐变风格[`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | 渐变变体[`GradientVariant`](../../gradientvariant/) |
| degree | Double | 渐变程度。取值范围为 0.0（暗）到 1.0（亮）。 |

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

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
