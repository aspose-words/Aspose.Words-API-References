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
enum class GradientStyle
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | -1 | No gradient. |
| Horizontal | 1 | Gradient running horizontally across an object. |
| Vertical | 2 | Gradient running vertically down an object. |
| DiagonalUp | 3 | Diagonal gradient moving from a bottom corner up to the opposite corner. |
| DiagonalDown | 4 | Diagonal gradient moving from a top corner down to the opposite corner. |
| FromCorner | 5 | Gradient running from a corner to the other three corners. |
| FromCenter | 6 | Gradient running from the center out to the corners. |


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
