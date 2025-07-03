---
title: Aspose::Words::Drawing::ShapeBase::get_Height method
linktitle: get_Height
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_Height method. Gets or sets the height of the containing block of the shape in C++.'
type: docs
weight: 22000
url: /cpp/aspose.words.drawing/shapebase/get_height/
---
## ShapeBase::get_Height method


Gets or sets the height of the containing block of the shape.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Height()
```

## Remarks


For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

## Examples



Shows how to insert a floating image, and specify its position and size. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
// as the shape's horizontal distance, in points, from the left side of the page.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// Set the shape's horizontal distance from the left side of the page to 100.
shape->set_Left(100);

// Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// Set the shape's height, which will automatically scale the width to preserve dimensions.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// The "Bottom" and "Right" properties contain the bottom and right edges of the image.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```


Shows how to resize a shape with an image. 
```cpp
// When we insert an image using the "InsertImage" method, the builder scales the shape that displays the image so that,
// when we view the document using 100% zoom in Microsoft Word, the shape displays the image in its actual size.
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// A 400x400 image will create an ImageData object with an image size of 300x300pt.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// If a shape's dimensions match the image data's dimensions,
// then the shape is displaying the image in its original size.
ASPOSE_ASSERT_EQ(300.0, shape->get_Width());
ASPOSE_ASSERT_EQ(300.0, shape->get_Height());

// Reduce the overall size of the shape by 50%.
System::WithLambda::setter_mul_wrap(GETTER_SETTER_LAMBDA_ARGS(shape, Width), 0.5);

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

doc->Save(get_ArtifactsDir() + u"Image.ScaleImage.docx");
```

## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
