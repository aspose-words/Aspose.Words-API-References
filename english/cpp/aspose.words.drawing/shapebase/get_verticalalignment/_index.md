---
title: Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment method
linktitle: get_VerticalAlignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment method. Specifies how the shape is positioned vertically in C++.'
type: docs
weight: 53000
url: /cpp/aspose.words.drawing/shapebase/get_verticalalignment/
---
## ShapeBase::get_VerticalAlignment method


Specifies how the shape is positioned vertically.

```cpp
Aspose::Words::Drawing::VerticalAlignment Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment()
```

## Remarks


The default value is [None](../../verticalalignment/).

Has effect only for top level floating shapes.

## Examples



Shows how to insert a floating image to the center of a page. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a floating image that will appear behind the overlapping text and align it to the page's center.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## See Also

* Enum [VerticalAlignment](../../verticalalignment/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
