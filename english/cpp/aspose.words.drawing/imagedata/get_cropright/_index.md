---
title: Aspose::Words::Drawing::ImageData::get_CropRight method
linktitle: get_CropRight
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ImageData::get_CropRight method. Defines the fraction of picture removal from the right side in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.drawing/imagedata/get_cropright/
---
## ImageData::get_CropRight method


Defines the fraction of picture removal from the right side.

```cpp
double Aspose::Words::Drawing::ImageData::get_CropRight()
```

## Remarks


The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note that a value of 1 will display no picture at all. Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape). Positive values less than 1 will result in the remaining picture being stretched to fit the shape.

The default value is 0.

## Examples



Shows how to edit a shape's image data. 
```cpp
auto imgSourceDoc = MakeObject<Document>(MyDir + u"Images.docx");
auto sourceShape = System::DynamicCast<Shape>(imgSourceDoc->GetChildNodes(NodeType::Shape, true)->idx_get(0));

auto dstDoc = MakeObject<Document>();

// Import a shape from the source document and append it to the first paragraph.
auto importedShape = System::DynamicCast<Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(importedShape);

// The imported shape contains an image. We can access the image's properties and raw data via the ImageData object.
SharedPtr<ImageData> imageData = importedShape->get_ImageData();
imageData->set_Title(u"Imported Image");

ASSERT_TRUE(imageData->get_HasImage());

// If an image has no borders, its ImageData object will define the border color as empty.
ASSERT_EQ(4, imageData->get_Borders()->get_Count());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, imageData->get_Borders()->idx_get(0)->get_Color());

// This image does not link to another shape or image file in the local file system.
ASSERT_FALSE(imageData->get_IsLink());
ASSERT_FALSE(imageData->get_IsLinkOnly());

// The "Brightness" and "Contrast" properties define image brightness and contrast
// on a 0-1 scale, with the default value at 0.5.
imageData->set_Brightness(0.8);
imageData->set_Contrast(1.0);

// The above brightness and contrast values have created an image with a lot of white.
// We can select a color with the ChromaKey property to replace with transparency, such as white.
imageData->set_ChromaKey(System::Drawing::Color::get_White());

// Import the source shape again and set the image to monochrome.
importedShape = System::DynamicCast<Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(importedShape);

importedShape->get_ImageData()->set_GrayScale(true);

// Import the source shape again to create a third image and set it to BiLevel.
// BiLevel sets every pixel to either black or white, whichever is closer to the original color.
importedShape = System::DynamicCast<Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(importedShape);

importedShape->get_ImageData()->set_BiLevel(true);

// Cropping is determined on a 0-1 scale. Cropping a side by 0.3
// will crop 30% of the image out at the cropped side.
importedShape->get_ImageData()->set_CropBottom(0.3);
importedShape->get_ImageData()->set_CropLeft(0.3);
importedShape->get_ImageData()->set_CropTop(0.3);
importedShape->get_ImageData()->set_CropRight(0.3);

dstDoc->Save(ArtifactsDir + u"Drawing.ImageData.docx");
```

## See Also

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
