---
title: Aspose::Words::Drawing::ImageSize::get_WidthPoints method
linktitle: get_WidthPoints
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ImageSize::get_WidthPoints method. Gets the width of the image in points. 1 point is 1/72 inch in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.drawing/imagesize/get_widthpoints/
---
## ImageSize::get_WidthPoints method


Gets the width of the image in points. 1 point is 1/72 inch.

```cpp
double Aspose::Words::Drawing::ImageSize::get_WidthPoints()
```


## Examples



Shows how to resize a shape with an image. 
```cpp
// When we insert an image using the "InsertImage" method, the builder scales the shape that displays the image so that,
// when we view the document using 100% zoom in Microsoft Word, the shape displays the image in its actual size.
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
SharedPtr<Shape> shape = builder->InsertImage(ImageDir + u"Logo.jpg");

// A 400x400 image will create an ImageData object with an image size of 300x300pt.
SharedPtr<ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// If a shape's dimensions match the image data's dimensions,
// then the shape is displaying the image in its original size.
ASPOSE_ASSERT_EQ(300.0, shape->get_Width());
ASPOSE_ASSERT_EQ(300.0, shape->get_Height());

// Reduce the overall size of the shape by 50%.
System::setter_mul_wrap(shape.GetPointer(), &ShapeBase::get_Width, &ShapeBase::set_Width, 0.5);

// Scaling factors apply to both the width and the height at the same time to preserve the shape's proportions.
ASPOSE_ASSERT_EQ(150.0, shape->get_Width());
ASPOSE_ASSERT_EQ(150.0, shape->get_Height());

// When we resize the shape, the size of the image data remains the same.
ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// We can reference the image data dimensions to apply a scaling based on the size of the image.
shape->set_Width(imageSize->get_WidthPoints() * 1.1);

ASPOSE_ASSERT_EQ(330.0, shape->get_Width());
ASPOSE_ASSERT_EQ(330.0, shape->get_Height());

doc->Save(ArtifactsDir + u"Image.ScaleImage.docx");
```

## See Also

* Class [ImageSize](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
