---
title: Aspose::Words::Drawing::Fill::get_GradientVariant method
linktitle: get_GradientVariant
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Fill::get_GradientVariant method. Gets the gradient variant GradientVariant for the fill in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.drawing/fill/get_gradientvariant/
---
## Fill::get_GradientVariant method


Gets the gradient variant [GradientVariant](../../gradientvariant/) for the fill.

```cpp
Aspose::Words::Drawing::GradientVariant Aspose::Words::Drawing::Fill::get_GradientVariant()
```


## Examples



Shows how to fill a shape with a gradients. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Apply One-color gradient fill to the shape with ForeColor of gradient fill.
shape->get_Fill()->OneColorGradient(System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2, 0.1);

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shape->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::Horizontal, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant2, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(270, shape->get_Fill()->get_GradientAngle());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Apply Two-color gradient fill to the shape.
shape->get_Fill()->TwoColorGradient(Aspose::Words::Drawing::GradientStyle::FromCorner, Aspose::Words::Drawing::GradientVariant::Variant4);
// Change BackColor of gradient fill.
shape->get_Fill()->set_BackColor(System::Drawing::Color::get_Yellow());
// Note that changes "GradientAngle" for "GradientStyle.FromCorner/GradientStyle.FromCenter"
// gradient fill don't get any effect, it will work only for linear gradient.
shape->get_Fill()->set_GradientAngle(15);

ASSERT_EQ(System::Drawing::Color::get_Yellow().ToArgb(), shape->get_Fill()->get_BackColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::FromCorner, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant4, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(0, shape->get_Fill()->get_GradientAngle());

// Use the compliance option to define the shape using DML if you want to get "GradientStyle",
// "GradientVariant" and "GradientAngle" properties after the document saves.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientFill.docx", saveOptions);
```

## See Also

* Enum [GradientVariant](../../gradientvariant/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
