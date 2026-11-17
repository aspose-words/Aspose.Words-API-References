---
title: Aspose::Words::Drawing::GradientStyle enum
linktitle: GradientStyle
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::GradientStyle enum. Specifies the style for a gradient fill in C++.'
type: docs
weight: 24000
url: /cpp/aspose.words.drawing/gradientstyle/
---
## GradientStyle enum


Specifies the style for a gradient fill.

```cpp
enum class GradientStyle : int
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| DiagonalDown | 4 | Diagonal gradient moving from a top corner down to the opposite corner. |
| DiagonalUp | 3 | Diagonal gradient moving from a bottom corner up to the opposite corner. |
| FromCenter | 6 | Gradient running from the center out to the corners. |
| FromCorner | 5 | Gradient running from a corner to the other three corners. |
| Horizontal | 1 | Gradient running horizontally across an object. |
| None | -1 | No gradient. |
| Vertical | 2 | Gradient running vertically down an object. |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
