---
title: get_Top
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the position of the top edge of the containing block of the shape.
type: docs
weight: 651
url: /cpp/aspose.words.drawing/shapebase/get_top/
---
## ShapeBase::get_Top method


Gets or sets the position of the top edge of the containing block of the shape.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Top()
```

## Remarks


For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

Has effect only for floating shapes.

## Examples



Shows how to insert a floating image, and specify its position and size. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertImage(ImageDir + u"Logo.jpg");
shape->set_WrapType(WrapType::None);

// Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
// as the shape's horizontal distance, in points, from the left side of the page.
shape->set_RelativeHorizontalPosition(RelativeHorizontalPosition::Page);

// Set the shape's horizontal distance from the left side of the page to 100.
shape->set_Left(100);

// Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
shape->set_RelativeVerticalPosition(RelativeVerticalPosition::Page);
shape->set_Top(80);

// Set the shape's height, which will automatically scale the width to preserve dimensions.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// The "Bottom" and "Right" properties contain the bottom and right edges of the image.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(ArtifactsDir + u"Image.CreateFloatingPositionSize.docx");
```

## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
