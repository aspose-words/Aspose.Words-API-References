---
title: ToByteArray
second_title: Aspose.Words for C++ API Reference
description: Returns image bytes for any image regardless whether the image is stored or linked.
type: docs
weight: 417
url: /cpp/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData::ToByteArray method


Returns image bytes for any image regardless whether the image is stored or linked.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::ImageData::ToByteArray()
```

## Remarks


If the image is linked, downloads the image every time it is called.

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
