---
title: Aspose::Words::Drawing::Fill class
linktitle: Fill
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Fill class. Represents fill formatting for an object. To learn more, visit the  documentation article in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.drawing/fill/
---
## Fill class


Represents fill formatting for an object. To learn more, visit the [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/) documentation article.

```cpp
class Fill : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Gets or sets a Color object that represents the background color for the fill. |
| [get_BackThemeColor](./get_backthemecolor/)() | Gets or sets a ThemeColor object that represents the background color for the fill. |
| [get_BackTintAndShade](./get_backtintandshade/)() | Gets or sets a double value that lightens or darkens the background color. |
| [get_BaseForeColor](./get_baseforecolor/)() | Gets a Color object that represents the base foreground color for the fill without any modifiers. |
| [get_Color](./get_color/)() | Gets or sets a Color object that represents the foreground color for the fill. |
| [get_FillType](./get_filltype/)() | Gets a fill type. |
| [get_ForeColor](./get_forecolor/)() | Gets a Color object that represents the foreground color for the fill. |
| [get_ForeThemeColor](./get_forethemecolor/)() | Gets or sets a ThemeColor object that represents the foreground color for the fill. |
| [get_ForeTintAndShade](./get_foretintandshade/)() | Gets or sets a double value that lightens or darkens the foreground color. |
| [get_GradientAngle](./get_gradientangle/)() | Gets or sets the angle of the gradient fill. |
| [get_GradientStops](./get_gradientstops/)() | Gets a collection of [GradientStop](../gradientstop/) objects for the fill. |
| [get_GradientStyle](./get_gradientstyle/)() | Gets the gradient style [GradientStyle](../gradientstyle/) for the fill. |
| [get_GradientVariant](./get_gradientvariant/)() | Gets the gradient variant [GradientVariant](../gradientvariant/) for the fill. |
| [get_ImageBytes](./get_imagebytes/)() | Gets the raw bytes of the fill texture or pattern. |
| [get_Opacity](./get_opacity/)() | Gets or sets the degree of opacity of the specified fill as a value between 0.0 (clear) and 1.0 (opaque). |
| [get_Pattern](./get_pattern/)() | Gets a [PatternType](../patterntype/) for the fill. |
| [get_PresetTexture](./get_presettexture/)() | Gets a [PresetTexture](../presettexture/) for the fill. |
| [get_RotateWithObject](./get_rotatewithobject/)() | Gets whether the fill rotates with the specified object. |
| [get_TextureAlignment](./get_texturealignment/)() | Gets or sets the alignment for tile texture fill. |
| [get_Transparency](./get_transparency/)() | Gets or sets the degree of transparency of the specified fill as a value between 0.0 (opaque) and 1.0 (clear). |
| [get_Visible](./get_visible/)() | Gets value that is **true** if the formatting applied to this instance, is visible. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OneColorGradient](./onecolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | Sets the specified fill to a one-color gradient. |
| [OneColorGradient](./onecolorgradient/)(System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | Sets the specified fill to a one-color gradient using the specified color. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType) | Sets the specified fill to a pattern. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType, System::Drawing::Color, System::Drawing::Color) | Sets the specified fill to a pattern. |
| [PresetTextured](./presettextured/)(Aspose::Words::Drawing::PresetTexture) | Sets the fill to a preset texture. |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Setter for [Aspose::Words::Drawing::Fill::get_BackColor](./get_backcolor/). |
| [set_BackThemeColor](./set_backthemecolor/)(Aspose::Words::Themes::ThemeColor) | Setter for [Aspose::Words::Drawing::Fill::get_BackThemeColor](./get_backthemecolor/). |
| [set_BackTintAndShade](./set_backtintandshade/)(double) | Setter for [Aspose::Words::Drawing::Fill::get_BackTintAndShade](./get_backtintandshade/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Setter for [Aspose::Words::Drawing::Fill::get_Color](./get_color/). |
| [set_ForeColor](./set_forecolor/)(System::Drawing::Color) | Sets a Color object that represents the foreground color for the fill. |
| [set_ForeThemeColor](./set_forethemecolor/)(Aspose::Words::Themes::ThemeColor) | Setter for [Aspose::Words::Drawing::Fill::get_ForeThemeColor](./get_forethemecolor/). |
| [set_ForeTintAndShade](./set_foretintandshade/)(double) | Setter for [Aspose::Words::Drawing::Fill::get_ForeTintAndShade](./get_foretintandshade/). |
| [set_GradientAngle](./set_gradientangle/)(double) | Setter for [Aspose::Words::Drawing::Fill::get_GradientAngle](./get_gradientangle/). |
| [set_Opacity](./set_opacity/)(double) | Setter for [Aspose::Words::Drawing::Fill::get_Opacity](./get_opacity/). |
| [set_RotateWithObject](./set_rotatewithobject/)(bool) | Sets whether the fill rotates with the specified object. |
| [set_TextureAlignment](./set_texturealignment/)(Aspose::Words::Drawing::TextureAlignment) | Setter for [Aspose::Words::Drawing::Fill::get_TextureAlignment](./get_texturealignment/). |
| [set_Transparency](./set_transparency/)(double) | Setter for [Aspose::Words::Drawing::Fill::get_Transparency](./get_transparency/). |
| [set_Visible](./set_visible/)(bool) | Sets value that is **true** if the formatting applied to this instance, is visible. |
| [SetImage](./setimage/)(const System::String\&) | Changes the fill type to single image. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Changes the fill type to single image. |
| [SetImage](./setimage/)(const System::ArrayPtr\<uint8_t\>\&) | Changes the fill type to single image. |
| [Solid](./solid/)() | Sets the fill to a uniform color. |
| [Solid](./solid/)(System::Drawing::Color) | Sets the fill to a specified uniform color. |
| [TwoColorGradient](./twocolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | Sets the specified fill to a two-color gradient. |
| [TwoColorGradient](./twocolorgradient/)(System::Drawing::Color, System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | Sets the specified fill to a two-color gradient. |
| static [Type](./type/)() |  |
## Remarks


Use the [Fill](../shapebase/get_fill/) or [Fill](../../aspose.words/font/get_fill/) property to access fill properties of an object. You do not create instances of the [Fill](./) class directly.

## Examples



Shows how to fill a shape with a solid color. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Write some text, and then cover it with a floating shape.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// Use the "StrokeColor" property to set the color of the outline of the shape.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// Use the "FillColor" property to set the color of the inside area of the shape.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// The "Opacity" property determines how transparent the color is on a 0-1 scale,
// with 1 being fully opaque, and 0 being invisible.
// The shape fill by default is fully opaque, so we cannot see the text that this shape is on top of.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// Set the shape fill color's opacity to a lower value so that we can see the text underneath it.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
