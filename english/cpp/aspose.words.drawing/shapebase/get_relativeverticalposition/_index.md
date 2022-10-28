---
title: get_RelativeVerticalPosition
second_title: Aspose.Words for C++ API Reference
description: Specifies relative to what the shape is positioned vertically.
type: docs
weight: 534
url: /cpp/aspose.words.drawing/shapebase/get_relativeverticalposition/
---
## ShapeBase.get_RelativeVerticalPosition method


Specifies relative to what the shape is positioned vertically.

```cpp
Aspose::Words::Drawing::RelativeVerticalPosition Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition()
```


The default value is **Paragraph**.

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

