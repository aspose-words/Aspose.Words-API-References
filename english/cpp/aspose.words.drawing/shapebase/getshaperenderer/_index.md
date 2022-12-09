---
title: GetShapeRenderer
second_title: Aspose.Words for C++ API Reference
description: Creates and returns an object that can be used to render this shape into an image.
type: docs
weight: 742
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
auto doc = MakeObject<Document>(MyDir + u"Various shapes.docx");
ArrayPtr<SharedPtr<Shape>> shapes = doc->GetChildNodes(NodeType::Shape, true)->LINQ_OfType<SharedPtr<Shape>>()->LINQ_ToArray();

ASSERT_EQ(7, shapes->get_Length());

// There are 7 shapes in the document, including one group shape with 2 child shapes.
// We will render every shape to an image file in the local file system
// while ignoring the group shapes since they have no appearance.
// This will produce 6 image files.
for (const auto& shape : System::IterateOver(doc->GetChildNodes(NodeType::Shape, true)->LINQ_OfType<SharedPtr<Shape>>()))
{
    SharedPtr<ShapeRenderer> renderer = shape->GetShapeRenderer();
    auto options = MakeObject<ImageSaveOptions>(SaveFormat::Png);
    renderer->Save(ArtifactsDir + String::Format(u"Shape.RenderAllShapes.{0}.png", shape->get_Name()), options);
}
```

## See Also

* Class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
