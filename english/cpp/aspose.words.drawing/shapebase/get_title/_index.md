---
title: get_Title
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the title (caption) of the current shape object.
type: docs
weight: 651
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create a shape, give it a title, and then add it to the document.
auto shape = MakeObject<Shape>(doc, ShapeType::Cube);
shape->set_Width(200);
shape->set_Height(200);
shape->set_Title(u"My cube");

builder->InsertNode(shape);

// When we save a document with a shape that has a title,
// Aspose.Words will store that title in the shape's Alt Text.
doc->Save(ArtifactsDir + u"Shape.Title.docx");

doc = MakeObject<Document>(ArtifactsDir + u"Shape.Title.docx");
shape = System::DynamicCast<Shape>(doc->GetChild(NodeType::Shape, 0, true));

ASSERT_EQ(String::Empty, shape->get_Title());
ASSERT_EQ(u"Title: My cube", shape->get_AlternativeText());
```

## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
