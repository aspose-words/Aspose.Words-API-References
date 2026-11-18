---
title: Aspose::Words::Drawing::Fill::TwoColorGradient method
linktitle: TwoColorGradient
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Fill::TwoColorGradient method. Sets the specified fill to a two-color gradient in C++.'
type: docs
weight: 44000
url: /cpp/aspose.words.drawing/fill/twocolorgradient/
---
## Fill::TwoColorGradient(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) method


Sets the specified fill to a two-color gradient.

```cpp
void Aspose::Words::Drawing::Fill::TwoColorGradient(Aspose::Words::Drawing::GradientStyle style, Aspose::Words::Drawing::GradientVariant variant)
```


| Parameter | Type | Description |
| --- | --- | --- |
| style | Aspose::Words::Drawing::GradientStyle | The gradient style [GradientStyle](../../gradientstyle/). |
| variant | Aspose::Words::Drawing::GradientVariant | The gradient variant [GradientVariant](../../gradientvariant/) |
## Examples


Shows how to fill a shape with a gradients.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(ShapeType::Rectangle, static_cast<double>(80), static_cast<double>(80));
// Apply One-color gradient fill to the shape with ForeColor of gradient fill.
shape->get_Fill()->OneColorGradient(System::Drawing::Color::get_Red(), GradientStyle::Horizontal, GradientVariant::Variant2, 0.1);

ASSERT_EQ(shape->get_Fill()->get_ForeColor().ToArgb(), System::Drawing::Color::get_Red().ToArgb());
ASSERT_EQ(shape->get_Fill()->get_GradientStyle(), GradientStyle::Horizontal);
ASSERT_EQ(shape->get_Fill()->get_GradientVariant(), GradientVariant::Variant2);
ASPOSE_ASSERT_EQ(shape->get_Fill()->get_GradientAngle(), 270);

shape = builder->InsertShape(ShapeType::Rectangle, static_cast<double>(80), static_cast<double>(80));
// Apply Two-color gradient fill to the shape.
shape->get_Fill()->TwoColorGradient(GradientStyle::FromCorner, GradientVariant::Variant4);
// Change BackColor of gradient fill.
shape->get_Fill()->set_BackColor(System::Drawing::Color::get_Yellow());
// Note that changes "GradientAngle" for "GradientStyle.FromCorner/GradientStyle.FromCenter"
// gradient fill don't get any effect, it will work only for linear gradient.
shape->get_Fill()->set_GradientAngle(15);

ASSERT_EQ(shape->get_Fill()->get_BackColor().ToArgb(), System::Drawing::Color::get_Yellow().ToArgb());
ASSERT_EQ(shape->get_Fill()->get_GradientStyle(), GradientStyle::FromCorner);
ASSERT_EQ(shape->get_Fill()->get_GradientVariant(), GradientVariant::Variant4);
ASPOSE_ASSERT_EQ(shape->get_Fill()->get_GradientAngle(), 0);

// Use the compliance option to define the shape using DML if you want to get "GradientStyle",
// "GradientVariant" and "GradientAngle" properties after the document saves.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientFill.docx", saveOptions);
```
## See Also

* Enum [GradientStyle](../../gradientstyle/)
* Enum [GradientVariant](../../gradientvariant/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::TwoColorGradient(System::Drawing::Color, System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) method


Sets the specified fill to a two-color gradient.

```cpp
void Aspose::Words::Drawing::Fill::TwoColorGradient(System::Drawing::Color color1, System::Drawing::Color color2, Aspose::Words::Drawing::GradientStyle style, Aspose::Words::Drawing::GradientVariant variant)
```


| Parameter | Type | Description |
| --- | --- | --- |
| color1 | System::Drawing::Color | The first color to build the gradient. |
| color2 | System::Drawing::Color | The second color to build the gradient. |
| style | Aspose::Words::Drawing::GradientStyle | The gradient style [GradientStyle](../../gradientstyle/). |
| variant | Aspose::Words::Drawing::GradientVariant | The gradient variant [GradientVariant](../../gradientvariant/) |
## Examples


Shows how to fill a shape with a gradients.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(ShapeType::Rectangle, static_cast<double>(80), static_cast<double>(80));
// Apply One-color gradient fill to the shape with ForeColor of gradient fill.
shape->get_Fill()->OneColorGradient(System::Drawing::Color::get_Red(), GradientStyle::Horizontal, GradientVariant::Variant2, 0.1);

ASSERT_EQ(shape->get_Fill()->get_ForeColor().ToArgb(), System::Drawing::Color::get_Red().ToArgb());
ASSERT_EQ(shape->get_Fill()->get_GradientStyle(), GradientStyle::Horizontal);
ASSERT_EQ(shape->get_Fill()->get_GradientVariant(), GradientVariant::Variant2);
ASPOSE_ASSERT_EQ(shape->get_Fill()->get_GradientAngle(), 270);

shape = builder->InsertShape(ShapeType::Rectangle, static_cast<double>(80), static_cast<double>(80));
// Apply Two-color gradient fill to the shape.
shape->get_Fill()->TwoColorGradient(GradientStyle::FromCorner, GradientVariant::Variant4);
// Change BackColor of gradient fill.
shape->get_Fill()->set_BackColor(System::Drawing::Color::get_Yellow());
// Note that changes "GradientAngle" for "GradientStyle.FromCorner/GradientStyle.FromCenter"
// gradient fill don't get any effect, it will work only for linear gradient.
shape->get_Fill()->set_GradientAngle(15);

ASSERT_EQ(shape->get_Fill()->get_BackColor().ToArgb(), System::Drawing::Color::get_Yellow().ToArgb());
ASSERT_EQ(shape->get_Fill()->get_GradientStyle(), GradientStyle::FromCorner);
ASSERT_EQ(shape->get_Fill()->get_GradientVariant(), GradientVariant::Variant4);
ASPOSE_ASSERT_EQ(shape->get_Fill()->get_GradientAngle(), 0);

// Use the compliance option to define the shape using DML if you want to get "GradientStyle",
// "GradientVariant" and "GradientAngle" properties after the document saves.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientFill.docx", saveOptions);
```
## See Also

* Enum [GradientStyle](../../gradientstyle/)
* Enum [GradientVariant](../../gradientvariant/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
