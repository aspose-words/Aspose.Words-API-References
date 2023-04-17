---
title: Aspose::Words::Drawing::GradientVariant enum
linktitle: GradientVariant
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::GradientVariant enum. Specifies the variant for a gradient fill in C++.'
type: docs
weight: 25000
url: /cpp/aspose.words.drawing/gradientvariant/
---
## GradientVariant enum


Specifies the variant for a gradient fill.

```cpp
enum class GradientVariant
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | Gradient variant 'None'. |
| Variant1 | 1 | Gradient variant 1. |
| Variant2 | 2 | Gradient variant 2. |
| Variant3 | 3 | Gradient variant 3. |
| Variant4 | 4 | Gradient variant 4. |


## Examples



Shows how to fill a shape with a gradients. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertShape(ShapeType::Rectangle, 80, 80);
// Apply One-color gradient fill to the shape with ForeColor of gradient fill.
shape->get_Fill()->OneColorGradient(System::Drawing::Color::get_Red(), GradientStyle::Horizontal, GradientVariant::Variant2, 0.1);

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shape->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(GradientStyle::Horizontal, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(GradientVariant::Variant2, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(270, shape->get_Fill()->get_GradientAngle());

shape = builder->InsertShape(ShapeType::Rectangle, 80, 80);
// Apply Two-color gradient fill to the shape.
shape->get_Fill()->TwoColorGradient(GradientStyle::FromCorner, GradientVariant::Variant4);
// Change BackColor of gradient fill.
shape->get_Fill()->set_BackColor(System::Drawing::Color::get_Yellow());
// Note that changes "GradientAngle" for "GradientStyle.FromCorner/GradientStyle.FromCenter"
// gradient fill don't get any effect, it will work only for linear gradient.
shape->get_Fill()->set_GradientAngle(15);

ASSERT_EQ(System::Drawing::Color::get_Yellow().ToArgb(), shape->get_Fill()->get_BackColor().ToArgb());
ASSERT_EQ(GradientStyle::FromCorner, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(GradientVariant::Variant4, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(0, shape->get_Fill()->get_GradientAngle());

// Use the compliance option to define the shape using DML if you want to get "GradientStyle",
// "GradientVariant" and "GradientAngle" properties after the document saves.
auto saveOptions = MakeObject<OoxmlSaveOptions>();
saveOptions->set_Compliance(OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(ArtifactsDir + u"Shape.GradientFill.docx", saveOptions);
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
