---
title: Aspose::Words::Drawing::ImageSize::get_HorizontalResolution method
linktitle: get_HorizontalResolution
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ImageSize::get_HorizontalResolution method. Gets the horizontal resolution in DPI in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.drawing/imagesize/get_horizontalresolution/
---
## ImageSize::get_HorizontalResolution method


Gets the horizontal resolution in DPI.

```cpp
double Aspose::Words::Drawing::ImageSize::get_HorizontalResolution() const
```


## Examples



Shows how to read the properties of an image in a shape. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a shape into the document which contains an image taken from our local file system.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// If the shape contains an image, its ImageData property will be valid,
// and it will contain an ImageSize object.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

// The ImageSize object contains read-only information about the image within the shape.
ASSERT_EQ(400, imageSize->get_HeightPixels());
ASSERT_EQ(400, imageSize->get_WidthPixels());

const double delta = 0.05;
ASSERT_NEAR(95.98, imageSize->get_HorizontalResolution(), delta);
ASSERT_NEAR(95.98, imageSize->get_VerticalResolution(), delta);

// We can base the size of the shape on the size of its image to avoid stretching the image.
shape->set_Width(imageSize->get_WidthPoints() * 2);
shape->set_Height(imageSize->get_HeightPoints() * 2);

doc->Save(get_ArtifactsDir() + u"Drawing.ImageSize.docx");
```

## See Also

* Class [ImageSize](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
