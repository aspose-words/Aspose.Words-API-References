---
title: Class Fill
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.Fill 班级. 表示对象的填充格式
type: docs
weight: 820
url: /zh/net/aspose.words.drawing/fill/
---
## Fill class

表示对象的填充格式。

```csharp
public class Fill
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | 获取或设置一个 Color 对象，表示填充的背景色。 |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | 获取填充类型。 |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | 获取或设置表示填充前景色的 Color 对象。 |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | 获取或设置渐变填充的角度。 |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | 获取一个集合[`GradientStop`](../gradientstop/)填充对象。 |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | 获取渐变样式[`GradientStyle`](../gradientstyle/)用于填充。 |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | 获取渐变变体[`GradientVariant`](../gradientvariant/)用于填充。 |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | 获取填充纹理或图案的原始字节。 |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | 获取或设置指定填充的不透明度为 0.0（透明）和 1.0（不透明）之间的值。 |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | 得到一个[`PatternType`](../patterntype/)用于填充。 |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | 得到一个[`PresetTexture`](../presettexture/)用于填充。 |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | 获取或设置填充是否随指定对象旋转 |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | 获取或设置平铺纹理填充的对齐方式。 |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | 获取或设置指定填充的透明度为 0.0（不透明）和 1.0（透明）之间的值。 |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | 获取或设置值为`真的`如果应用于此实例的格式是可见的。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(GradientStyle, GradientVariant, double) | 将指定的填充设置为单色渐变。 |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(Color, GradientStyle, GradientVariant, double) | 使用指定颜色将指定填充设置为单色渐变。 |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(PatternType) | 将指定的填充设置为图案。 |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(PatternType, Color, Color) | 将指定的填充设置为图案。 |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(PresetTexture) | 将填充设置为预设纹理。 |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(byte[]) | 将填充类型更改为单个图像。 |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(Stream) | 将填充类型更改为单个图像。 |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(string) | 将填充类型更改为单个图像。 |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | 将填充设置为统一颜色。 |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(Color) | 将填充设置为指定的统一颜色。 |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(GradientStyle, GradientVariant) | 将指定的填充设置为双色渐变。 |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(Color, Color, GradientStyle, GradientVariant) | 将指定的填充设置为双色渐变。 |

### 评论

使用[`Fill`](../shapebase/fill/)或者[`Fill`](../../aspose.words/font/fill/)属性来访问对象的填充属性。 您不创建的实例`Fill`直接上课。

### 例子

显示如何用纯色填充形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 写一些文字，然后用浮动形状覆盖它。
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
// 默认情况下，形状填充是完全不透明的，所以我们看不到这个形状上面的文本。
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// 将形状填充颜色的不透明度设置为较低的值，以便我们可以看到它下面的文本。
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)


