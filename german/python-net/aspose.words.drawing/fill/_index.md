---
title: Fill class
linktitle: Fill class
articleTitle: Fill class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.Fill class. Represents fill formatting for an object"
type: docs
weight: 80
url: /de/python-net/aspose.words.drawing/fill/
---

## Fill class

Represents fill formatting for an object.
To learn more, visit the [Working with Graphic Elements](https://docs.aspose.com/words/python-net/working-with-graphic-elements/) documentation article.




### Remarks

Use the [ShapeBase.fill](../shapebase/fill/) or [Font.fill](../../aspose.words/font/fill/) property to access fill properties of an object.
You do not create instances of the [Fill](./) class directly.




### Properties

| Name | Description |
| --- | --- |
| [back_color](./back_color/) | Gets or sets a Color object that represents the background color for the fill. |
| [back_theme_color](./back_theme_color/) | Gets or sets a ThemeColor object that represents the background color for the fill. |
| [back_tint_and_shade](./back_tint_and_shade/) | Gets or sets a double value that lightens or darkens the background color. |
| [base_fore_color](./base_fore_color/) | Gets a Color object that represents the base foreground color for the fill without any modifiers. |
| [color](./color/) | Gets or sets a Color object that represents the foreground color for the fill. |
| [fill_type](./fill_type/) | Gets a fill type. |
| [fore_color](./fore_color/) | Gets or sets a Color object that represents the foreground color for the fill. |
| [fore_theme_color](./fore_theme_color/) | Gets or sets a ThemeColor object that represents the foreground color for the fill. |
| [fore_tint_and_shade](./fore_tint_and_shade/) | Gets or sets a double value that lightens or darkens the foreground color. |
| [gradient_angle](./gradient_angle/) | Gets or sets the angle of the gradient fill. |
| [gradient_stops](./gradient_stops/) | Gets a collection of [GradientStop](../gradientstop/) objects for the fill. |
| [gradient_style](./gradient_style/) | Gets the gradient style [GradientStyle](../gradientstyle/) for the fill. |
| [gradient_variant](./gradient_variant/) | Gets the gradient variant [GradientVariant](../gradientvariant/) for the fill. |
| [image_bytes](./image_bytes/) | Gets the raw bytes of the fill texture or pattern. |
| [opacity](./opacity/) | Gets or sets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque). |
| [pattern](./pattern/) | Gets a [PatternType](../patterntype/) for the fill. |
| [preset_texture](./preset_texture/) | Gets a [PresetTexture](../presettexture/) for the fill. |
| [rotate_with_object](./rotate_with_object/) | Gets or sets whether the fill rotates with the specified object. |
| [texture_alignment](./texture_alignment/) | Gets or sets the alignment for tile texture fill. |
| [transparency](./transparency/) | Gets or sets the degree of transparency of the specified fill as a value between 0.0 (opaque) and 1.0 (clear). |
| [visible](./visible/) | Gets or sets value that is ``True`` if the formatting applied to this instance, is visible. |

### Methods

| Name | Description |
| --- | --- |
|[ one_color_gradient(style, variant, degree)](./one_color_gradient/#gradientstyle_gradientvariant_float) | Sets the specified fill to a one-color gradient. |
|[ one_color_gradient(color, style, variant, degree)](./one_color_gradient/#color_gradientstyle_gradientvariant_float) | Sets the specified fill to a one-color gradient using the specified color. |
|[ patterned(pattern_type)](./patterned/#patterntype) | Sets the specified fill to a pattern. |
|[ patterned(pattern_type, fore_color, back_color)](./patterned/#patterntype_color_color) | Sets the specified fill to a pattern. |
|[ preset_textured(preset_texture)](./preset_textured/#presettexture) | Sets the fill to a preset texture. |
|[ set_image(file_name)](./set_image/#str) | Changes the fill type to single image. |
|[ set_image(stream)](./set_image/#bytesio) | Changes the fill type to single image. |
|[ set_image(image_bytes)](./set_image/#bytes) | Changes the fill type to single image. |
|[ solid()](./solid/#default) | Sets the fill to a uniform color. |
|[ solid(color)](./solid/#color) | Sets the fill to a specified uniform color. |
|[ two_color_gradient(style, variant)](./two_color_gradient/#gradientstyle_gradientvariant) | Sets the specified fill to a two-color gradient. |
|[ two_color_gradient(color1, color2, style, variant)](./two_color_gradient/#color_color_gradientstyle_gradientvariant) | Sets the specified fill to a two-color gradient. |

### Examples

Shows how to fill a shape with a solid color.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Schreiben Sie etwas Text und bedecken Sie ihn dann mit einer schwebenden Form.
builder.font.size = 32
builder.writeln('Hello world!')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.CLOUD_CALLOUT, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=25, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=25, width=250, height=150, wrap_type=aw.drawing.WrapType.NONE)
# Verwenden Sie die "StrokeColor"-Eigenschaft, um die Farbe der Kontur der Form festzulegen.
shape.stroke_color = aspose.pydrawing.Color.cadet_blue
# Verwenden Sie die "FillColor"-Eigenschaft, um die Farbe des Innenbereichs der Form festzulegen.
shape.fill_color = aspose.pydrawing.Color.light_blue
# Die "Opacity"-Eigenschaft bestimmt, wie transparent die Farbe auf einer Skala von 0 bis 1 ist,
# wobei 1 vollständig undurchsichtig und 0 unsichtbar ist.
# Die Füllung der Form ist standardmäßig vollständig undurchsichtig, sodass wir den Text, über dem sich die Form befindet, nicht sehen können.
self.assertEqual(1, shape.fill.opacity)
# Setzen Sie die Opazität der Füllfarbe der Form auf einen niedrigeren Wert, damit wir den darunter liegenden Text sehen können.
shape.fill.opacity = 0.3
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Fill.docx')
```

### See Also

* module [aspose.words.drawing](../)

