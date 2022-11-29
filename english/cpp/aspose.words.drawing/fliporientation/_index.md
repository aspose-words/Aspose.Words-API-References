---
title: FlipOrientation
second_title: Aspose.Words for C++ API Reference
description: Possible values for the orientation of a shape.
type: docs
weight: 287
url: /cpp/aspose.words.drawing/fliporientation/
---
## FlipOrientation enum


Possible values for the orientation of a shape.

```cpp
enum class FlipOrientation
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | Coordinates are not flipped. |
| Horizontal | 1 | Flip along the y-axis, reversing the x-coordinates. |
| Vertical | 2 | Flip along the x-axis, reversing the y-coordinates. |
| Both | 3 | Flip along both the y- and x-axis. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words](../../)
