---
title: Aspose::Words::Drawing::ImageData::set_ImageBytes method
linktitle: set_ImageBytes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ImageData::set_ImageBytes method. Sets the raw bytes of the image stored in the shape in C++.'
type: docs
weight: 67000
url: /cpp/aspose.words.drawing/imagedata/set_imagebytes/
---
## ImageData::set_ImageBytes method


Sets the raw bytes of the image stored in the shape.

```cpp
void Aspose::Words::Drawing::ImageData::set_ImageBytes(const System::ArrayPtr<uint8_t> & value)
```

## Remarks


Setting the value to **null** or an empty array will remove the image from the shape.

Returns **null** if the image is not stored in the document (e.g the image is probably linked in this case).
## Examples


Shows how to create an image file from a shape's raw image data.

```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Images.docx"));

auto imgShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChild(NodeType::Shape, 0, true));

ASSERT_TRUE(imgShape->get_HasImage());

// ToByteArray() returns the array stored in the ImageBytes property.
ASPOSE_ASSERT_EQ(imgShape->get_ImageData()->get_ImageBytes(), imgShape->get_ImageData()->ToByteArray());

// Save the shape's image data to an image file in the local file system.
{
    System::SharedPtr<System::IO::Stream> imgStream = imgShape->get_ImageData()->ToStream();
    {
        auto outStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Drawing.GetDataFromImage.png", System::IO::FileMode::Create, System::IO::FileAccess::ReadWrite);
        imgStream->CopyTo(outStream);
    }
}
```
## See Also

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
