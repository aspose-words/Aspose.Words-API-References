---
title: get_FlipOrientation
second_title: Aspose.Words for C++ API Reference
description: Switches the orientation of a shape.
type: docs
weight: 248
url: /cpp/aspose.words.drawing/shapebase/get_fliporientation/
---
## ShapeBase::get_FlipOrientation method


Switches the orientation of a shape.

```cpp
Aspose::Words::Drawing::FlipOrientation Aspose::Words::Drawing::ShapeBase::get_FlipOrientation()
```

## Remarks


The default value is [None](../../fliporientation/).

## Examples



Shows how to flip a shape on an axis. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert an image shape and leave its orientation in its default state.
SharedPtr<Shape> shape = builder->InsertShape(ShapeType::Rectangle, RelativeHorizontalPosition::LeftMargin, 100, RelativeVerticalPosition::TopMargin,
                                              100, 100, 100, WrapType::None);
shape->get_ImageData()->SetImage(ImageDir + u"Logo.jpg");

ASSERT_EQ(FlipOrientation::None, shape->get_FlipOrientation());

shape = builder->InsertShape(ShapeType::Rectangle, RelativeHorizontalPosition::LeftMargin, 250, RelativeVerticalPosition::TopMargin, 100, 100, 100,
                             WrapType::None);
shape->get_ImageData()->SetImage(ImageDir + u"Logo.jpg");

// Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the second shape on the y-axis,
// making it into a horizontal mirror image of the first shape.
shape->set_FlipOrientation(FlipOrientation::Horizontal);

shape = builder->InsertShape(ShapeType::Rectangle, RelativeHorizontalPosition::LeftMargin, 100, RelativeVerticalPosition::TopMargin, 250, 100, 100,
                             WrapType::None);
shape->get_ImageData()->SetImage(ImageDir + u"Logo.jpg");

// Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the third shape on the x-axis,
// making it into a vertical mirror image of the first shape.
shape->set_FlipOrientation(FlipOrientation::Vertical);

shape = builder->InsertShape(ShapeType::Rectangle, RelativeHorizontalPosition::LeftMargin, 250, RelativeVerticalPosition::TopMargin, 250, 100, 100,
                             WrapType::None);
shape->get_ImageData()->SetImage(ImageDir + u"Logo.jpg");

// Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the fourth shape on both the x and y axes,
// making it into a horizontal and vertical mirror image of the first shape.
shape->set_FlipOrientation(FlipOrientation::Both);

doc->Save(ArtifactsDir + u"Shape.FlipShapeOrientation.docx");
```

## See Also

* Enum [FlipOrientation](../../fliporientation/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
