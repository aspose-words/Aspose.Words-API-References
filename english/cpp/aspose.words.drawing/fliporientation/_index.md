---
title: Aspose::Words::Drawing::FlipOrientation enum
linktitle: FlipOrientation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::FlipOrientation enum. Possible values for the orientation of a shape in C++.'
type: docs
weight: 23000
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
| None | n/a | Coordinates are not flipped. |
| Horizontal | n/a | Flip along the y-axis, reversing the x-coordinates. |
| Vertical | n/a | Flip along the x-axis, reversing the y-coordinates. |
| Both | n/a | Flip along both the y- and x-axis. |


## Examples



Shows how to flip a shape on an axis. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert an image shape and leave its orientation in its default state.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, static_cast<double>(100), Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, static_cast<double>(100), static_cast<double>(100), static_cast<double>(100), Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

ASSERT_EQ(Aspose::Words::Drawing::FlipOrientation::None, shape->get_FlipOrientation());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, static_cast<double>(250), Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, static_cast<double>(100), static_cast<double>(100), static_cast<double>(100), Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the second shape on the y-axis,
// making it into a horizontal mirror image of the first shape.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Horizontal);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, static_cast<double>(100), Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, static_cast<double>(250), static_cast<double>(100), static_cast<double>(100), Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the third shape on the x-axis,
// making it into a vertical mirror image of the first shape.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Vertical);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, static_cast<double>(250), Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, static_cast<double>(250), static_cast<double>(100), static_cast<double>(100), Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the fourth shape on both the x and y axes,
// making it into a horizontal and vertical mirror image of the first shape.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Both);

doc->Save(get_ArtifactsDir() + u"Shape.FlipShapeOrientation.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
