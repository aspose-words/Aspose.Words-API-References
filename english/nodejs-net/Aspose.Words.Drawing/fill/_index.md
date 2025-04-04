---
title: Fill class
linktitle: Fill class
articleTitle: Fill class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Fill class. Represents fill formatting for an object"
type: docs
weight: 90
url: /nodejs-net/aspose.words.drawing/fill/
---

## Fill class

Represents fill formatting for an object.
To learn more, visit the [Working with Graphic Elements](https://docs.aspose.com/words/nodejs-net/working-with-graphic-elements/) documentation article.




### Remarks

Use the [ShapeBase.fill](../shapebase/fill/) or [Font.fill](../../aspose.words/font/fill/) property to access fill properties of an object.
You do not create instances of the [Fill](./) class directly.




### Properties

| Name | Description |
| --- | --- |
| [backColor](./backColor/) | Gets or sets a Color object that represents the background color for the fill. |
| [backThemeColor](./backThemeColor/) | Gets or sets a ThemeColor object that represents the background color for the fill. |
| [backTintAndShade](./backTintAndShade/) | Gets or sets a double value that lightens or darkens the background color. |
| [baseForeColor](./baseForeColor/) | Gets a Color object that represents the base foreground color for the fill without any modifiers. |
| [color](./color/) | Gets or sets a Color object that represents the foreground color for the fill. |
| [fillType](./fillType/) | Gets a fill type. |
| [foreColor](./foreColor/) | Gets or sets a Color object that represents the foreground color for the fill. |
| [foreThemeColor](./foreThemeColor/) | Gets or sets a ThemeColor object that represents the foreground color for the fill. |
| [foreTintAndShade](./foreTintAndShade/) | Gets or sets a double value that lightens or darkens the foreground color. |
| [gradientAngle](./gradientAngle/) | Gets or sets the angle of the gradient fill. |
| [gradientStops](./gradientStops/) | Gets a collection of [GradientStop](../gradientstop/) objects for the fill. |
| [gradientStyle](./gradientStyle/) | Gets the gradient style [GradientStyle](../gradientstyle/) for the fill. |
| [gradientVariant](./gradientVariant/) | Gets the gradient variant [GradientVariant](../gradientvariant/) for the fill. |
| [imageBytes](./imageBytes/) | Gets the raw bytes of the fill texture or pattern. |
| [opacity](./opacity/) | Gets or sets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque). |
| [pattern](./pattern/) | Gets a [PatternType](../patterntype/) for the fill. |
| [presetTexture](./presetTexture/) | Gets a [PresetTexture](../presettexture/) for the fill. |
| [rotateWithObject](./rotateWithObject/) | Gets or sets whether the fill rotates with the specified object. |
| [textureAlignment](./textureAlignment/) | Gets or sets the alignment for tile texture fill. |
| [transparency](./transparency/) | Gets or sets the degree of transparency of the specified fill as a value between 0.0 (opaque) and 1.0 (clear). |
| [visible](./visible/) | Gets or sets value that is ``true`` if the formatting applied to this instance, is visible. |

### Methods

| Name | Description |
| --- | --- |
|[ oneColorGradient(style, variant, degree)](./oneColorGradient/#gradientstyle_gradientvariant_number) | Sets the specified fill to a one-color gradient. |
|[ oneColorGradient(color, style, variant, degree)](./oneColorGradient/#string_gradientstyle_gradientvariant_number) | Sets the specified fill to a one-color gradient using the specified color. |
|[ patterned(patternType)](./patterned/#patterntype) | Sets the specified fill to a pattern. |
|[ patterned(patternType, foreColor, backColor)](./patterned/#patterntype_string_string) | Sets the specified fill to a pattern. |
|[ presetTextured(presetTexture)](./presetTextured/#presettexture) | Sets the fill to a preset texture. |
|[ setImage(fileName)](./setImage/#string) | Changes the fill type to single image. |
|[ setImage(stream)](./setImage/#buffer) | Changes the fill type to single image. |
|[ setImage(imageBytes)](./setImage/#number[]) | Changes the fill type to single image. |
|[ solid()](./solid/#default) | Sets the fill to a uniform color. |
|[ solid(color)](./solid/#string) | Sets the fill to a specified uniform color. |
|[ twoColorGradient(style, variant)](./twoColorGradient/#gradientstyle_gradientvariant) | Sets the specified fill to a two-color gradient. |
|[ twoColorGradient(color1, color2, style, variant)](./twoColorGradient/#string_string_gradientstyle_gradientvariant) | Sets the specified fill to a two-color gradient. |

### Examples

Shows how to fill a shape with a solid color.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Write some text, and then cover it with a floating shape.
builder.font.size = 32;
builder.writeln("Hello world!");

let shape = builder.insertShape(aw.Drawing.ShapeType.CloudCallout, aw.Drawing.RelativeHorizontalPosition.LeftMargin, 25,
  aw.Drawing.RelativeVerticalPosition.TopMargin, 25, 250, 150, aw.Drawing.WrapType.None);

// Use the "StrokeColor" property to set the color of the outline of the shape.
shape.strokeColor = "#5F9EA0";

// Use the "FillColor" property to set the color of the inside area of the shape.
shape.fillColor = "#ADD8E6";

// The "Opacity" property determines how transparent the color is on a 0-1 scale,
// with 1 being fully opaque, and 0 being invisible.
// The shape fill by default is fully opaque, so we cannot see the text that this shape is on top of.
expect(shape.fill.opacity).toEqual(1.0);

// Set the shape fill color's opacity to a lower value so that we can see the text underneath it.
shape.fill.opacity = 0.3;

doc.save(base.artifactsDir + "Shape.fill.docx");
```

### See Also

* module [Aspose.Words.Drawing](../)

