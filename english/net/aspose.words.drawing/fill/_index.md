---
title: Class Fill
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Drawing.Fill class. Represents fill formatting for an object in C#.
type: docs
weight: 820
url: /net/aspose.words.drawing/fill/
---
## Fill class

Represents fill formatting for an object.

To learn more, visit the [Working with Graphic Elements](https://docs.aspose.com/words/net/working-with-graphic-elements/) documentation article.

```csharp
public class Fill
```

## Properties

| Name | Description |
| --- | --- |
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | Gets or sets a Color object that represents the background color for the fill. |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | Gets a fill type. |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | Gets or sets a Color object that represents the foreground color for the fill. |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | Gets or sets the angle of the gradient fill. |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | Gets a collection of [`GradientStop`](../gradientstop/) objects for the fill. |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | Gets the gradient style [`GradientStyle`](../gradientstyle/) for the fill. |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | Gets the gradient variant [`GradientVariant`](../gradientvariant/) for the fill. |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | Gets the raw bytes of the fill texture or pattern. |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | Gets or sets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque). |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | Gets a [`PatternType`](../patterntype/) for the fill. |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | Gets a [`PresetTexture`](../presettexture/) for the fill. |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | Gets or sets whether the fill rotates with the specified object. |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | Gets or sets the alignment for tile texture fill. |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | Gets or sets the degree of transparency of the specified fill as a value between 0.0 (opaque) and 1.0 (clear). |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | Gets or sets value that is `true` if the formatting applied to this instance, is visible. |

## Methods

| Name | Description |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(GradientStyle, GradientVariant, double) | Sets the specified fill to a one-color gradient. |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(Color, GradientStyle, GradientVariant, double) | Sets the specified fill to a one-color gradient using the specified color. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(PatternType) | Sets the specified fill to a pattern. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(PatternType, Color, Color) | Sets the specified fill to a pattern. |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(PresetTexture) | Sets the fill to a preset texture. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(byte[]) | Changes the fill type to single image. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(Stream) | Changes the fill type to single image. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(string) | Changes the fill type to single image. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | Sets the fill to a uniform color. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(Color) | Sets the fill to a specified uniform color. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(GradientStyle, GradientVariant) | Sets the specified fill to a two-color gradient. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(Color, Color, GradientStyle, GradientVariant) | Sets the specified fill to a two-color gradient. |

## Remarks

Use the [`Fill`](../shapebase/fill/) or [`Fill`](../../aspose.words/font/fill/) property to access fill properties of an object. You do not create instances of the `Fill` class directly.

## Examples

Shows how to fill a shape with a solid color.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Write some text, and then cover it with a floating shape.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Use the "StrokeColor" property to set the color of the outline of the shape.
shape.StrokeColor = Color.CadetBlue;

// Use the "FillColor" property to set the color of the inside area of the shape.
shape.FillColor = Color.LightBlue;

// The "Opacity" property determines how transparent the color is on a 0-1 scale,
// with 1 being fully opaque, and 0 being invisible.
// The shape fill by default is fully opaque, so we cannot see the text that this shape is on top of.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Set the shape fill color's opacity to a lower value so that we can see the text underneath it.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
