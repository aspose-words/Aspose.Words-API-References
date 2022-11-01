---
title: ToImage
second_title: Aspose.Words for C++ API Reference
description: Gets the image stored in the shape as a Image object.
type: docs
weight: 430
url: /cpp/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method


Gets the image stored in the shape as a **Image** object.

```cpp
System::SharedPtr<System::Drawing::Image> Aspose::Words::Drawing::ImageData::ToImage()
```


A new **Image** object is created every time this method is called.

It is the responsibility of the caller to dispose the image object.

## Examples




Shows how to save all images from a document to the file system. 
```cpp
auto imgSourceDoc = MakeObject<Document>(MyDir + u"Images.docx");

// Shapes with the "HasImage" flag set store and display all the document's images.
auto shapesWithImages =
    imgSourceDoc->GetChildNodes(NodeType::Shape, true)->LINQ_Cast<SharedPtr<Shape>>()->LINQ_Where([](SharedPtr<Shape> s) { return s->get_HasImage(); });

// Go through each shape and save its image.
auto formatConverter = MakeObject<System::Drawing::ImageFormatConverter>();

{
    SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<Shape>>> enumerator = shapesWithImages->GetEnumerator();
    int shapeIndex = 0;

    while (enumerator->MoveNext())
    {
        SharedPtr<ImageData> imageData = enumerator->get_Current()->get_ImageData();
        SharedPtr<System::Drawing::Imaging::ImageFormat> format = imageData->ToImage()->get_RawFormat();
        String fileExtension = formatConverter->ConvertToString(format);

        {
            SharedPtr<System::IO::FileStream> fileStream =
                System::IO::File::Create(ArtifactsDir + String::Format(u"Drawing.SaveAllImages.{0}.{1}", ++shapeIndex, fileExtension));
            imageData->Save(fileStream);
        }
    }
}
```

