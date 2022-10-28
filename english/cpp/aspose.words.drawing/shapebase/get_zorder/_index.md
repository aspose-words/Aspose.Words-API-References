---
title: get_ZOrder
second_title: Aspose.Words for C++ API Reference
description: Determines the display order of overlapping shapes.
type: docs
weight: 716
url: /cpp/aspose.words.drawing/shapebase/get_zorder/
---
## ShapeBase.get_ZOrder method


Determines the display order of overlapping shapes.

```cpp
int32_t Aspose::Words::Drawing::ShapeBase::get_ZOrder()
```


Has effect only for top level shapes.

The default value is 0.

The number represents the stacking precedence. A shape with a higher number will be displayed as if it were overlapping (in "front" of) a shape with a lower number.

The order of overlapping shapes is independent for shapes in the header and in the main text of the document.

The display order of child shapes in a group shape is determined by their order inside the group shape.

## Examples




Shows how to manipulate the order of shapes. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert three different colored rectangles that partially overlap each other.
// When we insert a shape that overlaps another shape, Aspose.Words places the newer shape on top of the old one.
// The light green rectangle will overlap the light blue rectangle and partially obscure it,
// and the light blue rectangle will obscure the orange rectangle.
SharedPtr<Shape> shape = builder->InsertShape(ShapeType::Rectangle, RelativeHorizontalPosition::LeftMargin, 100, RelativeVerticalPosition::TopMargin,
                                              100, 200, 200, WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

shape = builder->InsertShape(ShapeType::Rectangle, RelativeHorizontalPosition::LeftMargin, 150, RelativeVerticalPosition::TopMargin, 150, 200, 200,
                             WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

shape = builder->InsertShape(ShapeType::Rectangle, RelativeHorizontalPosition::LeftMargin, 200, RelativeVerticalPosition::TopMargin, 200, 200, 200,
                             WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightGreen());

ArrayPtr<SharedPtr<Shape>> shapes = doc->GetChildNodes(NodeType::Shape, true)->LINQ_OfType<SharedPtr<Shape>>()->LINQ_ToArray();

// The "ZOrder" property of a shape determines its stacking priority among other overlapping shapes.
// If two overlapping shapes have different "ZOrder" values,
// Microsoft Word will place the shape with a higher value over the shape with the lower value.
// Set the "ZOrder" values of our shapes to place the first orange rectangle over the second light blue one
// and the second light blue rectangle over the third light green rectangle.
// This will reverse their original stacking order.
shapes[0]->set_ZOrder(3);
shapes[1]->set_ZOrder(2);
shapes[2]->set_ZOrder(1);

doc->Save(ArtifactsDir + u"Shape.ZOrder.docx");
```

