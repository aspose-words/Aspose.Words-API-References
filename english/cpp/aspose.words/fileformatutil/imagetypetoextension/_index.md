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
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Get the collection of shapes from the document,
// and save the image data of every shape with an image as a file to the local file system.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> s)>>([](System::SharedPtr<Aspose::Words::Node> s) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Drawing::Shape>(s))->get_HasImage();
}))));

int32_t imageIndex = 0;
for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    if (shape->get_HasImage())
    {
        // The image data of shapes may contain images of many possible image formats.
        // We can determine a file extension for each image automatically, based on its format.
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```

## See Also

* Enum [ImageType](../../../aspose.words.drawing/imagetype/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
