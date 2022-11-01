---
title: get_BehindText
second_title: Aspose.Words for C++ API Reference
description: Specifies whether the shape is below or above text.
type: docs
weight: 66
url: /cpp/aspose.words.drawing/shapebase/get_behindtext/
---
## ShapeBase.get_BehindText method


Specifies whether the shape is below or above text.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_BehindText()
```


Has effect only for top level shapes.

The default value is **false**.

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

