---
title: Aspose::Words::Drawing::Shape::get_HasImage method
linktitle: get_HasImage
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Shape::get_HasImage method. Returns true if the shape has image bytes or links an image in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.drawing/shape/get_hasimage/
---
## Shape::get_HasImage method


Returns **true** if the shape has image bytes or links an image.

```cpp
bool Aspose::Words::Drawing::Shape::get_HasImage()
```


## Examples



Shows how to extract images from a document, and save them to the local file system as individual files. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Images.docx");

// Get the collection of shapes from the document,
// and save the image data of every shape with an image as a file to the local file system.
SharedPtr<NodeCollection> shapes = doc->GetChildNodes(NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count([](SharedPtr<Node> s) { return (System::DynamicCast<Shape>(s))->get_HasImage(); }));

int imageIndex = 0;
for (const auto& shape : System::IterateOver(shapes->LINQ_OfType<SharedPtr<Shape>>()))
{
    if (shape->get_HasImage())
    {
        // The image data of shapes may contain images of many possible image formats.
        // We can determine a file extension for each image automatically, based on its format.
        String imageFileName =
            String::Format(u"File.ExtractImages.{0}{1}", imageIndex, FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```


Shows how to delete all shapes with images from a document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Images.docx");
SharedPtr<NodeCollection> shapes = doc->GetChildNodes(NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_OfType<SharedPtr<Shape>>()->LINQ_Count([](SharedPtr<Shape> s) { return s->get_HasImage(); }));

for (const auto& shape : System::IterateOver(shapes->LINQ_OfType<SharedPtr<Shape>>()))
{
    if (shape->get_HasImage())
    {
        shape->Remove();
    }
}

ASSERT_EQ(0, shapes->LINQ_OfType<SharedPtr<Shape>>()->LINQ_Count([](SharedPtr<Shape> s) { return s->get_HasImage(); }));
```

## See Also

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
