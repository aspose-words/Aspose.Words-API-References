---
title: get_RelativeHorizontalPosition
second_title: Aspose.Words for C++ API Reference
description: Specifies relative to what the shape is positioned horizontally.
type: docs
weight: 521
url: /cpp/aspose.words.drawing/shapebase/get_relativehorizontalposition/
---
## ShapeBase.get_RelativeHorizontalPosition method


Specifies relative to what the shape is positioned horizontally.

```cpp
Aspose::Words::Drawing::RelativeHorizontalPosition Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition()
```


The default value is **Column**.

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

