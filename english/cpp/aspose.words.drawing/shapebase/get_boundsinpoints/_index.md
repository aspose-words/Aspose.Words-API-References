---
title: get_BoundsInPoints
second_title: Aspose.Words for C++ API Reference
description: Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape.
type: docs
weight: 105
url: /cpp/aspose.words.drawing/shapebase/get_boundsinpoints/
---
## ShapeBase::get_BoundsInPoints method


Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_BoundsInPoints()
```


## Examples



Shows how to verify shape containing block boundaries. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> line = builder->InsertShape(ShapeType::Line, RelativeHorizontalPosition::LeftMargin, 50, RelativeVerticalPosition::TopMargin, 50, 100,
                                             100, WrapType::None);
line->set_StrokeColor(System::Drawing::Color::get_Orange());

// Even though the line itself takes up little space on the document page,
// it occupies a rectangular containing block, the size of which we can determine using the "Bounds" properties.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), line->get_Bounds());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(50.0f, 50.0f, 100.0f, 100.0f), line->get_BoundsInPoints());

// Create a group shape, and then set the size of its containing block using the "Bounds" property.
auto group = MakeObject<GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f));

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());

// Create a rectangle, verify the size of its bounding block, and then add it to the group shape.
auto rectangle = MakeObject<Shape>(doc, ShapeType::Rectangle);
rectangle->set_Width(100);
rectangle->set_Height(100);
rectangle->set_Left(700);
rectangle->set_Top(700);

ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(700.0f, 700.0f, 100.0f, 100.0f), rectangle->get_BoundsInPoints());

group->AppendChild(rectangle);

// The group shape's coordinate plane has its origin on the top left-hand side corner of its containing block,
// and the x and y coordinates of (1000, 1000) on the bottom right-hand side corner.
// Our group shape is 250x250pt in size, so every 4pt on the group shape's coordinate plane
// translates to 1pt in the document body's coordinate plane.
// Every shape that we insert will also shrink in size by a factor of 4.
// The change in the shape's "BoundsInPoints" property will reflect this.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(175.0f, 275.0f, 25.0f, 25.0f), rectangle->get_BoundsInPoints());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(group);

// Insert a shape and place it outside of the bounds of the group shape's containing block.
auto shape = MakeObject<Shape>(doc, ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(1000);
shape->set_Top(1000);

group->AppendChild(shape);

// The group shape's footprint in the document body has increased, but the containing block remains the same.
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(0.0f, 100.0f, 250.0f, 250.0f), group->get_BoundsInPoints());
ASPOSE_ASSERT_EQ(System::Drawing::RectangleF(250.0f, 350.0f, 25.0f, 25.0f), shape->get_BoundsInPoints());

doc->Save(ArtifactsDir + u"Shape.Bounds.docx");
```

## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
