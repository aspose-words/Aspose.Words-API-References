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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a floating image that will appear behind the overlapping text and align it to the page's center.
SharedPtr<Shape> shape = builder->InsertImage(ImageDir + u"Logo.jpg");
shape->set_WrapType(WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(HorizontalAlignment::Center);
shape->set_VerticalAlignment(VerticalAlignment::Center);

doc->Save(ArtifactsDir + u"Image.CreateFloatingPageCenter.docx");
```

## See Also

* Enum [VerticalAlignment](../../verticalalignment/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
