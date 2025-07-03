---
title: Aspose::Words::Drawing::ShapeBase::GetShapeRenderer method
linktitle: GetShapeRenderer
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::GetShapeRenderer method. Creates and returns an object that can be used to render this shape into an image in C++.'
type: docs
weight: 58000
url: /cpp/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase::GetShapeRenderer method


Creates and returns an object that can be used to render this shape into an image.

```cpp
System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> Aspose::Words::Drawing::ShapeBase::GetShapeRenderer()
```


### ReturnValue

The renderer object for this shape.
## Remarks


This method just invokes the [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/) constructor and passes this object as a parameter.

## Examples



Shows how to use a shape renderer to export shapes to files in the local file system. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(7, shapes->get_Length());

// There are 7 shapes in the document, including one group shape with 2 child shapes.
// We will render every shape to an image file in the local file system
// while ignoring the group shapes since they have no appearance.
// This will produce 6 image files.
for (auto&& shape : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> renderer = shape->GetShapeRenderer();
    auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
    renderer->Save(get_ArtifactsDir() + System::String::Format(u"Shape.RenderAllShapes.{0}.png", shape->get_Name()), options);
}
```

## See Also

* Class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
