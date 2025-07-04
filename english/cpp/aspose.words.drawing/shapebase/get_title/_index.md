---
title: Aspose::Words::Drawing::ShapeBase::get_Title method
linktitle: get_Title
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_Title method. Gets or sets the title (caption) of the current shape object in C++.'
type: docs
weight: 51000
url: /cpp/aspose.words.drawing/shapebase/get_title/
---
## ShapeBase::get_Title method


Gets or sets the title (caption) of the current shape object.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Title()
```

## Remarks


Default is empty string.

Cannot be **null**, but can be an empty string.

## Examples



Shows how to set the title of a shape. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Create a shape, give it a title, and then add it to the document.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_Width(200);
shape->set_Height(200);
shape->set_Title(u"My cube");

builder->InsertNode(shape);

// When we save a document with a shape that has a title,
// Aspose.Words will store that title in the shape's Alt Text.
doc->Save(get_ArtifactsDir() + u"Shape.Title.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Title.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::String::Empty, shape->get_Title());
ASSERT_EQ(u"Title: My cube", shape->get_AlternativeText());
```

## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
