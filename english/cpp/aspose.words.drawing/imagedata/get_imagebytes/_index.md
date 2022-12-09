---
title: get_ImageBytes
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the raw bytes of the image stored in the shape.
type: docs
weight: 157
url: /cpp/aspose.words.drawing/imagedata/get_imagebytes/
---
## ImageData::get_ImageBytes method


Gets or sets the raw bytes of the image stored in the shape.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::ImageData::get_ImageBytes()
```

## Remarks


Setting the value to **null** or an empty array will remove the image from the shape.

Returns **null** if the image is not stored in the document (e.g the image is probably linked in this case).

## Examples



Shows how to create an image file from a shape's raw image data. 
```cpp
auto imgSourceDoc = MakeObject<Document>(MyDir + u"Images.docx");

auto imgShape = System::DynamicCast<Shape>(imgSourceDoc->GetChild(NodeType::Shape, 0, true));

ASSERT_TRUE(imgShape->get_HasImage());

// ToByteArray() returns the array stored in the ImageBytes property.
ASPOSE_ASSERT_EQ(imgShape->get_ImageData()->get_ImageBytes(), imgShape->get_ImageData()->ToByteArray());

// Save the shape's image data to an image file in the local file system.
{
    SharedPtr<System::IO::Stream> imgStream = imgShape->get_ImageData()->ToStream();
    {
        auto outStream = MakeObject<System::IO::FileStream>(ArtifactsDir + u"Drawing.GetDataFromImage.png", System::IO::FileMode::Create,
                                                            System::IO::FileAccess::ReadWrite);
        imgStream->CopyTo(outStream);
    }
}
```

## See Also

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
