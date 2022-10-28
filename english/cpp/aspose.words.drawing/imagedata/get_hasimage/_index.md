---
title: get_HasImage
second_title: Aspose.Words for C++ API Reference
description: Returns true if the shape has image bytes or links an image.
type: docs
weight: 131
url: /cpp/aspose.words.drawing/imagedata/get_hasimage/
---
## ImageData.get_HasImage method


Returns true if the shape has image bytes or links an image.

```cpp
bool Aspose::Words::Drawing::ImageData::get_HasImage()
```


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

