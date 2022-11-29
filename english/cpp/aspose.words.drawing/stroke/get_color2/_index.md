---
title: get_Color2
second_title: Aspose.Words for C++ API Reference
description: Defines a second color for a stroke.
type: docs
weight: 27
url: /cpp/aspose.words.drawing/stroke/get_color2/
---
## Stroke::get_Color2 method


Defines a second color for a stroke.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Stroke::get_Color2()
```

## Remarks


The default value for a [Shape](../../shape/) is **White**.

## Examples



Shows how to process shape stroke features. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Shape stroke pattern border.docx");
auto shape = System::DynamicCast<Shape>(doc->GetChild(NodeType::Shape, 0, true));
SharedPtr<Stroke> stroke = shape->get_Stroke();

// Strokes can have two colors, which are used to create a pattern defined by two-tone image data.
// Strokes with a single color do not use the Color2 property.
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 128, 0, 0), stroke->get_Color());
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 255, 255, 0), stroke->get_Color2());

ASSERT_FALSE(stroke->get_ImageBytes() == nullptr);
System::IO::File::WriteAllBytes(ArtifactsDir + u"Drawing.StrokePattern.png", stroke->get_ImageBytes());
```

## See Also

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
