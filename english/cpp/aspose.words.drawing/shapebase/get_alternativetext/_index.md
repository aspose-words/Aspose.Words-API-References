---
title: get_AlternativeText
second_title: Aspose.Words for C++ API Reference
description: Defines alternative text to be displayed instead of a graphic.
type: docs
weight: 27
url: /cpp/aspose.words.drawing/shapebase/get_alternativetext/
---
## ShapeBase.get_AlternativeText method


Defines alternative text to be displayed instead of a graphic.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_AlternativeText()
```


The default value is an empty string.

## Examples




Shows how to use a shape's alternative text. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
SharedPtr<Shape> shape = builder->InsertShape(ShapeType::Cube, 150, 150);
shape->set_Name(u"MyCube");

shape->set_AlternativeText(u"Alt text for MyCube.");

// We can access the alternative text of a shape by right-clicking it, and then via "Format AutoShape" -> "Alt Text".
doc->Save(ArtifactsDir + u"Shape.AltText.docx");

// Save the document to HTML, and then delete the linked image that belongs to our shape.
// The browser that is reading our HTML will display the alt text in place of the missing image.
doc->Save(ArtifactsDir + u"Shape.AltText.html");
System::IO::File::Delete(ArtifactsDir + u"Shape.AltText.001.png");
```

