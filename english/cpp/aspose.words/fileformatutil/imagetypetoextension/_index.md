---
title: Aspose::Words::FileFormatUtil::ImageTypeToExtension method
linktitle: ImageTypeToExtension
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::FileFormatUtil::ImageTypeToExtension method. Converts an Aspose.Words image type enumerated value into a file extension. The returned extension is a lower-case string with a leading dot in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/fileformatutil/imagetypetoextension/
---
## FileFormatUtil::ImageTypeToExtension method


Converts an Aspose.Words image type enumerated value into a file extension. The returned extension is a lower-case string with a leading dot.

```cpp
static System::String Aspose::Words::FileFormatUtil::ImageTypeToExtension(Aspose::Words::Drawing::ImageType imageType)
```


## Examples



Shows how to extract images from a document, and save them to the local file system as individual files. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Images.docx");

// Get the collection of shapes from the document,
// and save the image data of every shape with an image as a file to the local file system.
SharedPtr<NodeCollection> shapes = doc->GetChildNodes(NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count([](SharedPtr<Node> s) { return (System::ExplicitCast<Shape>(s))->get_HasImage(); }));

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

## See Also

* Enum [ImageType](../../../aspose.words.drawing/imagetype/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
