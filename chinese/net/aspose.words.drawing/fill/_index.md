---
title: Fill Class
linktitle: Fill
articleTitle: Fill
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.Fill 班级. 表示对象的填充格式 在 C#.
type: docs
weight: 950
url: /zh/net/aspose.words.drawing/fill/
---
## Fill class

表示对象的填充格式。

要了解更多信息，请访问[使用图形元素](https://docs.aspose.com/words/net/working-with-graphic-elements/)文档文章。

```csharp
public class Fill
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | 获取或设置一个 Color 对象，该对象表示填充的背景颜色。 |
| [BackThemeColor](../../aspose.words.drawing/fill/backthemecolor/) { get; set; } | 获取或设置一个 ThemeColor 对象，该对象表示填充的背景颜色。 |
| [BackTintAndShade](../../aspose.words.drawing/fill/backtintandshade/) { get; set; } | 获取或设置使背景颜色变亮或变暗的双精度值。 |
| [Color](../../aspose.words.drawing/fill/color/) { get; set; } | 获取或设置一个 Color 对象，该对象表示填充的前景色。 |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | 获取填充类型。 |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | 获取或设置一个 Color 对象，该对象表示填充的前景色。 |
| [ForeThemeColor](../../aspose.words.drawing/fill/forethemecolor/) { get; set; } | 获取或设置一个 ThemeColor 对象，该对象表示填充的前景色。 |
| [ForeTintAndShade](../../aspose.words.drawing/fill/foretintandshade/) { get; set; } | 获取或设置使前景色变亮或变暗的双精度值。 |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | 获取或设置渐变填充的角度。 |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | 获取集合[`GradientStop`](../gradientstop/)用于填充的对象. |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | 获取渐变样式[`GradientStyle`](../gradientstyle/)用于填充. |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | 获取渐变变量[`GradientVariant`](../gradientvariant/)用于填充. |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | 获取填充纹理或图案的原始字节。 |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | 获取或设置指定填充的不透明度，其值介于 0.0（透明）和 1.0（不透明）之间。 |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | 获得[`PatternType`](../patterntype/)用于填充. |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | 获得[`PresetTexture`](../presettexture/)用于填充. |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | 获取或设置填充是否随指定对象旋转。 |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | 获取或设置图块纹理填充的对齐方式。 |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | 获取或设置指定填充的透明度，其值介于 0.0（不透明）和 1.0（透明）之间。 |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | 获取或设置值`真的`如果应用于此实例的格式可见。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | 将指定填充设置为单色渐变。 |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(*Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | 使用指定颜色将指定填充设置为单色渐变。 |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(*[PatternType](../patterntype/)*) | 将指定填充设置为图案。 |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(*[PatternType](../patterntype/), Color, Color*) | 将指定填充设置为图案。 |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(*[PresetTexture](../presettexture/)*) | 将填充设置为预设纹理。 |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(*byte[]*) | 将填充类型更改为单个图像。 |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(*Stream*) | 将填充类型更改为单个图像。 |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(*string*) | 将填充类型更改为单个图像。 |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | 将填充设置为统一颜色。 |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(*Color*) | 将填充设置为指定的统一颜色。 |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | 将指定填充设置为二色渐变。 |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(*Color, Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | 将指定填充设置为二色渐变。 |

## 评论

使用[`Fill`](../shapebase/fill/)或者[`Fill`](../../aspose.words/font/fill/)属性来访问对象的填充属性。 您不创建该对象的实例`Fill`直接上课。

## 例子

演示如何用纯色填充形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 写一些文本，然后用浮动形状覆盖它。
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// 使用“StrokeColor”属性设置形状轮廓的颜色。
shape.StrokeColor = Color.CadetBlue;

// 使用“FillColor”属性设置形状内部区域的颜色。
shape.FillColor = Color.LightBlue;

// “Opacity”属性决定颜色在 0-1 范围内的透明度，
// 1 表示完全不透明，0 表示不可见。
// 默认情况下，形状填充是完全不透明的，因此我们看不到该形状上方的文本。
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// 将形状填充颜色的不透明度设置为较低的值，以便我们可以看到其下方的文本。
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
