---
title: SetImage
second_title: Aspose.Words for C++ API Reference
description: Sets the image that the shape displays.
type: docs
weight: 443
url: /cpp/aspose.words.drawing/imagedata/setimage/
---
## ImageData::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Sets the image that the shape displays.

```cpp
void Aspose::Words::Drawing::ImageData::SetImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Parameter | Type | Description |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | The image object. |

## Examples



Shows how to display images from the local file system in a document. 
```cpp
auto doc = MakeObject<Document>();

// To display an image in a document, we will need to create a shape
// which will contain an image, and then append it to the document's body.
SharedPtr<Shape> imgShape;

// Below are two ways of getting an image from a file in the local file system.
// 1 -  Create an image object from an image file:
{
    SharedPtr<System::Drawing::Image> srcImage = System::Drawing::Image::FromFile(ImageDir + u"Logo.jpg");
    imgShape = MakeObject<Shape>(doc, ShapeType::Image);
    doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(imgShape);
    imgShape->get_ImageData()->SetImage(srcImage);
}

// 2 -  Open an image file from the local file system using a stream:
{
    SharedPtr<System::IO::Stream> stream =
        MakeObject<System::IO::FileStream>(ImageDir + u"Logo.jpg", System::IO::FileMode::Open, System::IO::FileAccess::Read);
    imgShape = MakeObject<Shape>(doc, ShapeType::Image);
    doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(imgShape);
    imgShape->get_ImageData()->SetImage(stream);
    imgShape->set_Left(150.0f);
}

doc->Save(ArtifactsDir + u"Drawing.ImportImage.docx");
```

## See Also

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
## ImageData::SetImage(const System::SharedPtr\<System::IO::Stream\>\&) method


Sets the image that the shape displays.

```cpp
void Aspose::Words::Drawing::ImageData::SetImage(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | The stream that contains the image. |

## Examples



Shows how to display images from the local file system in a document. 
```cpp
auto doc = MakeObject<Document>();

// To display an image in a document, we will need to create a shape
// which will contain an image, and then append it to the document's body.
SharedPtr<Shape> imgShape;

// Below are two ways of getting an image from a file in the local file system.
// 1 -  Create an image object from an image file:
{
    SharedPtr<System::Drawing::Image> srcImage = System::Drawing::Image::FromFile(ImageDir + u"Logo.jpg");
    imgShape = MakeObject<Shape>(doc, ShapeType::Image);
    doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(imgShape);
    imgShape->get_ImageData()->SetImage(srcImage);
}

// 2 -  Open an image file from the local file system using a stream:
{
    SharedPtr<System::IO::Stream> stream =
        MakeObject<System::IO::FileStream>(ImageDir + u"Logo.jpg", System::IO::FileMode::Open, System::IO::FileAccess::Read);
    imgShape = MakeObject<Shape>(doc, ShapeType::Image);
    doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(imgShape);
    imgShape->get_ImageData()->SetImage(stream);
    imgShape->set_Left(150.0f);
}

doc->Save(ArtifactsDir + u"Drawing.ImportImage.docx");
```

## See Also

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
## ImageData::SetImage(const System::String\&) method


Sets the image that the shape displays.

```cpp
void Aspose::Words::Drawing::ImageData::SetImage(const System::String &fileName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | The image file. Can be a file name or a URL. |

## Examples



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

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
## ImageData::SetImage(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Drawing::ImageData::SetImage(std::basic_istream<CharType, Traits> &stream)
```

## See Also

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
