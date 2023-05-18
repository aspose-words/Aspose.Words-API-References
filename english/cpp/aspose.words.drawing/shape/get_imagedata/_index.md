---
title: Aspose::Words::Drawing::Shape::get_ImageData method
linktitle: get_ImageData
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Shape::get_ImageData method. Provides access to the image of the shape. Returns null if the shape cannot have an image in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.drawing/shape/get_imagedata/
---
## Shape::get_ImageData method


Provides access to the image of the shape. Returns **null** if the shape cannot have an image.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ImageData> Aspose::Words::Drawing::Shape::get_ImageData()
```


## Examples



Shows how to extract images from a document, and save them to the local file system as individual files. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Images.docx");

// Get the collection of shapes from the document,
// and save the image data of every shape with an image as a file to the local file system.
SharedPtr<NodeCollection> shapes = doc->GetChildNodes(NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count([](SharedPtr<Node> s) { return (System::ExplicitCast<Shape>(s))->get_HasImage(); }));

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

* Class [ImageData](../../imagedata/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
