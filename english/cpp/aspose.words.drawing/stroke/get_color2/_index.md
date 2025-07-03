---
title: Aspose::Words::Drawing::Stroke::get_Color2 method
linktitle: get_Color2
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Stroke::get_Color2 method. Defines a second color for a stroke in C++.'
type: docs
weight: 4000
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
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();

// Strokes can have two colors, which are used to create a pattern defined by two-tone image data.
// Strokes with a single color do not use the Color2 property.
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 128, 0, 0), stroke->get_Color());
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 255, 255, 0), stroke->get_Color2());

ASSERT_FALSE(System::TestTools::IsNull(stroke->get_ImageBytes()));
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Drawing.StrokePattern.png", stroke->get_ImageBytes());
```

## See Also

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
