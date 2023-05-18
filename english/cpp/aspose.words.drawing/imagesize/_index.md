---
title: Aspose::Words::Drawing::ImageSize class
linktitle: ImageSize
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ImageSize class. Contains information about image size and resolution. To learn more, visit the  documentation article in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.drawing/imagesize/
---
## ImageSize class


Contains information about image size and resolution. To learn more, visit the [Working with Images](https://docs.aspose.com/words/cpp/working-with-images/) documentation article.

```cpp
class ImageSize : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_HeightPixels](./get_heightpixels/)() const | Gets the height of the image in pixels. |
| [get_HeightPoints](./get_heightpoints/)() | Gets the height of the image in points. 1 point is 1/72 inch. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | Gets the horizontal resolution in DPI. |
| [get_VerticalResolution](./get_verticalresolution/)() const | Gets the vertical resolution in DPI. |
| [get_WidthPixels](./get_widthpixels/)() const | Gets the width of the image in pixels. |
| [get_WidthPoints](./get_widthpoints/)() | Gets the width of the image in points. 1 point is 1/72 inch. |
| [GetType](./gettype/)() const override |  |
| [ImageSize](./imagesize/)(int32_t, int32_t) | Initializes width and height to the given values in pixels. Initializes resolution to 96 dpi. |
| [ImageSize](./imagesize/)(int32_t, int32_t, double, double) | Initializes width, height and resolution to the given values. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
