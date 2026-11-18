---
title: Aspose::Words::Drawing::ShapeBase::set_RelativeVerticalPosition method
linktitle: set_RelativeVerticalPosition
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::set_RelativeVerticalPosition method. Specifies relative to what the shape is positioned vertically in C++.'
type: docs
weight: 83000
url: /cpp/aspose.words.drawing/shapebase/set_relativeverticalposition/
---
## ShapeBase::set_RelativeVerticalPosition method


Specifies relative to what the shape is positioned vertically.

```cpp
void Aspose::Words::Drawing::ShapeBase::set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition value)
```

## Remarks


The default value is [Paragraph](../../relativeverticalposition/).

Has effect only for top level floating shapes.
## Examples


Shows how to insert a floating image to the center of a page.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a floating image that will appear behind the overlapping text and align it to the page's center.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(HorizontalAlignment::Center);
shape->set_VerticalAlignment(VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```
## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
