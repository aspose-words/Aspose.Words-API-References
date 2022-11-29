---
title: Save
second_title: Aspose.Words for C++ API Reference
description: Saves the image into the specified stream.
type: docs
weight: 235
url: /cpp/aspose.words.drawing/imagedata/save/
---
## ImageData::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


Saves the image into the specified stream.

```cpp
void Aspose::Words::Drawing::ImageData::Save(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | The stream where to save the image to. |
## Remarks


Is it the responsibility of the caller to dispose the stream object.

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

## See Also

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
## ImageData::Save(const System::String\&) method


Saves the image into a file.

```cpp
void Aspose::Words::Drawing::ImageData::Save(const System::String &fileName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | The file name where to save the image. |

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

## See Also

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
## ImageData::Save(std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Drawing::ImageData::Save(std::basic_ostream<CharType, Traits> &stream)
```

## See Also

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
