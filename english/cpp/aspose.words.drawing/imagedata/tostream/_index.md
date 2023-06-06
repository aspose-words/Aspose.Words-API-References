---
title: Aspose::Words::Drawing::ImageData::ToStream method
linktitle: ToStream
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ImageData::ToStream method. Creates and returns a stream that contains the image bytes in C++.'
type: docs
weight: 38000
url: /cpp/aspose.words.drawing/imagedata/tostream/
---
## ImageData::ToStream method


Creates and returns a stream that contains the image bytes.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Drawing::ImageData::ToStream()
```

## Remarks


If the image bytes are stored in the shape, creates and returns a **MemoryStream** object.

If the image is linked and stored in a file, opens the file and returns a **FileStream** object.

If the image is linked and stored in an external URL, downloads the file and returns a **MemoryStream** object.

Is it the responsibility of the caller to dispose the stream object.

## Examples



Shows how to create an image file from a shape's raw image data. 
```cpp
auto imgSourceDoc = MakeObject<Document>(MyDir + u"Images.docx");

auto imgShape = System::ExplicitCast<Shape>(imgSourceDoc->GetChild(NodeType::Shape, 0, true));

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
* Library [Aspose.Words for C++](../../../)
