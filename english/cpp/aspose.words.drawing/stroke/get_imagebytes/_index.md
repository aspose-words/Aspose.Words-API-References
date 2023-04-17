---
title: Aspose::Words::Drawing::Stroke::get_ImageBytes method
linktitle: get_ImageBytes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Stroke::get_ImageBytes method. Defines the image for a stroke image or pattern fill in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.drawing/stroke/get_imagebytes/
---
## Stroke::get_ImageBytes method


Defines the image for a stroke image or pattern fill.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::Stroke::get_ImageBytes()
```


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
* Library [Aspose.Words for C++](../../../)
