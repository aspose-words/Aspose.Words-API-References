---
title: Aspose::Words::Drawing::ShapeBase::get_FlipOrientation method
linktitle: get_FlipOrientation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_FlipOrientation method. Switches the orientation of a shape in C++.'
type: docs
weight: 20000
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
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert an image shape and leave its orientation in its default state.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

ASSERT_EQ(Aspose::Words::Drawing::FlipOrientation::None, shape->get_FlipOrientation());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the second shape on the y-axis,
// making it into a horizontal mirror image of the first shape.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Horizontal);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the third shape on the x-axis,
// making it into a vertical mirror image of the first shape.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Vertical);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Set the "FlipOrientation" property to "FlipOrientation.Horizontal" to flip the fourth shape on both the x and y axes,
// making it into a horizontal and vertical mirror image of the first shape.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Both);

doc->Save(get_ArtifactsDir() + u"Shape.FlipShapeOrientation.docx");
```

## See Also

* Enum [FlipOrientation](../../fliporientation/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
