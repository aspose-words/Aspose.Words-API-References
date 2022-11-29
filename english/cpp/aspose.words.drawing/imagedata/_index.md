---
title: ImageData
second_title: Aspose.Words for C++ API Reference
description: Defines an image for a shape.
type: docs
weight: 66
url: /cpp/aspose.words.drawing/imagedata/
---
## ImageData class


Defines an image for a shape.

```cpp
class ImageData : public Aspose::Words::IBorderAttrSource
```

## Methods

| Method | Description |
| --- | --- |
| [get_BiLevel](./get_bilevel/)() | Determines whether an image will be displayed in black and white. |
| [get_Borders](./get_borders/)() | Gets the collection of borders of the image. Borders only have effect for inline images. |
| [get_Brightness](./get_brightness/)() | Gets or sets the brightness of the picture. The value for this property must be a number from 0.0 (dimmest) to 1.0 (brightest). |
| [get_ChromaKey](./get_chromakey/)() | Defines the color value of the image that will be treated as transparent. |
| [get_Contrast](./get_contrast/)() | Gets or sets the contrast for the specified picture. The value for this property must be a number from 0.0 (the least contrast) to 1.0 (the greatest contrast). |
| [get_CropBottom](./get_cropbottom/)() | Defines the fraction of picture removal from the bottom side. |
| [get_CropLeft](./get_cropleft/)() | Defines the fraction of picture removal from the left side. |
| [get_CropRight](./get_cropright/)() | Defines the fraction of picture removal from the right side. |
| [get_CropTop](./get_croptop/)() | Defines the fraction of picture removal from the top side. |
| [get_GrayScale](./get_grayscale/)() | Determines whether a picture will display in grayscale mode. |
| [get_HasImage](./get_hasimage/)() | Returns true if the shape has image bytes or links an image. |
| [get_ImageBytes](./get_imagebytes/)() | Gets or sets the raw bytes of the image stored in the shape. |
| [get_ImageSize](./get_imagesize/)() | Gets the information about image size and resolution. |
| [get_ImageType](./get_imagetype/)() | Gets the type of the image. |
| [get_IsLink](./get_islink/)() | Returns true if the image is linked to the shape (when [SourceFullName](./get_sourcefullname/) is specified). |
| [get_IsLinkOnly](./get_islinkonly/)() | Returns true if the image is linked and not stored in the document. |
| [get_SourceFullName](./get_sourcefullname/)() | Gets or sets the path and name of the source file for the linked image. |
| [get_Title](./get_title/)() | Defines the title of an image. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Saves the image into the specified stream. |
| [Save](./save/)(const System::String\&) | Saves the image into a file. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_BiLevel](./set_bilevel/)(bool) | Setter for [Aspose::Words::Drawing::ImageData::get_BiLevel](./get_bilevel/). |
| [set_Brightness](./set_brightness/)(double) | Setter for [Aspose::Words::Drawing::ImageData::get_Brightness](./get_brightness/). |
| [set_ChromaKey](./set_chromakey/)(System::Drawing::Color) | Setter for [Aspose::Words::Drawing::ImageData::get_ChromaKey](./get_chromakey/). |
| [set_Contrast](./set_contrast/)(double) | Setter for [Aspose::Words::Drawing::ImageData::get_Contrast](./get_contrast/). |
| [set_CropBottom](./set_cropbottom/)(double) | Setter for [Aspose::Words::Drawing::ImageData::get_CropBottom](./get_cropbottom/). |
| [set_CropLeft](./set_cropleft/)(double) | Setter for [Aspose::Words::Drawing::ImageData::get_CropLeft](./get_cropleft/). |
| [set_CropRight](./set_cropright/)(double) | Setter for [Aspose::Words::Drawing::ImageData::get_CropRight](./get_cropright/). |
| [set_CropTop](./set_croptop/)(double) | Setter for [Aspose::Words::Drawing::ImageData::get_CropTop](./get_croptop/). |
| [set_GrayScale](./set_grayscale/)(bool) | Setter for [Aspose::Words::Drawing::ImageData::get_GrayScale](./get_grayscale/). |
| [set_ImageBytes](./set_imagebytes/)(const System::ArrayPtr\<uint8_t\>\&) | Setter for [Aspose::Words::Drawing::ImageData::get_ImageBytes](./get_imagebytes/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Setter for [Aspose::Words::Drawing::ImageData::get_SourceFullName](./get_sourcefullname/). |
| [set_Title](./set_title/)(const System::String\&) | Setter for [Aspose::Words::Drawing::ImageData::get_Title](./get_title/). |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Sets the image that the shape displays. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Sets the image that the shape displays. |
| [SetImage](./setimage/)(const System::String\&) | Sets the image that the shape displays. |
| [SetImage](./setimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [ToByteArray](./tobytearray/)() | Returns image bytes for any image regardless whether the image is stored or linked. |
| [ToImage](./toimage/)() | Gets the image stored in the shape as a **Image** object. |
| [ToStream](./tostream/)() | Creates and returns a stream that contains the image bytes. |
## Remarks


Use the [ImageData](../shape/get_imagedata/) property to access and modify the image inside a shape. You do not create instances of the [ImageData](./) class directly.

An image can be stored inside a shape, linked to external file or both (linked and stored in the document).

Regardless of whether the image is stored inside the shape or linked, you can always access the actual image using the [ToByteArray](./tobytearray/), [ToStream](./tostream/), [ToImage](./toimage/) or [Save()](../) methods. If the image is stored inside the shape, you can also directly access it using the [ImageBytes](./get_imagebytes/) property.

To store an image inside a shape use the [SetImage()](../) method. To link an image to a shape, set the [SourceFullName](./get_sourcefullname/) property.

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


Shows how to insert a linked image into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

String imageFileName = ImageDir + u"Windows MetaFile.wmf";

// Below are two ways of applying an image to a shape so that it can display it.
// 1 -  Set the shape to contain the image.
auto shape = MakeObject<Shape>(builder->get_Document(), ShapeType::Image);
shape->set_WrapType(WrapType::Inline);
shape->get_ImageData()->SetImage(imageFileName);

builder->InsertNode(shape);

doc->Save(ArtifactsDir + u"Image.CreateLinkedImage.Embedded.docx");

// Every image that we store in shape will increase the size of our document.
ASSERT_TRUE(70000 < MakeObject<System::IO::FileInfo>(ArtifactsDir + u"Image.CreateLinkedImage.Embedded.docx")->get_Length());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->RemoveAllChildren();

// 2 -  Set the shape to link to an image file in the local file system.
shape = MakeObject<Shape>(builder->get_Document(), ShapeType::Image);
shape->set_WrapType(WrapType::Inline);
shape->get_ImageData()->set_SourceFullName(imageFileName);

builder->InsertNode(shape);
doc->Save(ArtifactsDir + u"Image.CreateLinkedImage.Linked.docx");

// Linking to images will save space and result in a smaller document.
// However, the document can only display the image correctly while
// the image file is present at the location that the shape's "SourceFullName" property points to.
ASSERT_TRUE(10000 > MakeObject<System::IO::FileInfo>(ArtifactsDir + u"Image.CreateLinkedImage.Linked.docx")->get_Length());
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words](../../)
