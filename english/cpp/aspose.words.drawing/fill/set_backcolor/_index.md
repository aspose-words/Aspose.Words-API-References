---
title: Aspose::Words::Drawing::Fill::set_BackColor method
linktitle: set_BackColor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Fill::set_BackColor method. Sets a Color object that represents the background color for the fill in C++.'
type: docs
weight: 66000
url: /cpp/aspose.words.drawing/fill/set_backcolor/
---
## Fill::set_BackColor method


Sets a Color object that represents the background color for the fill.

```cpp
void Aspose::Words::Drawing::Fill::set_BackColor(System::Drawing::Color value)
```

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

* [get_BackColor](../get_backcolor/)

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
