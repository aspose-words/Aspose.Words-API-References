---
title: LocalToParent
second_title: Aspose.Words for C++ API Reference
description: Converts a value from the local coordinate space into the coordinate space of the parent shape.
type: docs
weight: 781
url: /cpp/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase::LocalToParent method


Converts a value from the local coordinate space into the coordinate space of the parent shape.

```cpp
System::Drawing::PointF Aspose::Words::Drawing::ShapeBase::LocalToParent(System::Drawing::PointF value)
```


## Examples



Shows how to translate the x and y coordinate location on a shape's coordinate plane to a location on the parent shape's coordinate plane. 
```cpp
auto doc = MakeObject<Document>();

// Insert a group shape, and place it 100 points below and to the right of
// the document's x and Y coordinate origin point.
auto group = MakeObject<GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(100.0f, 100.0f, 500.0f, 500.0f));

// Use the "LocalToParent" method to determine that (0, 0) on the group's internal x and y coordinates
// lies on (100, 100) of its parent shape's coordinate system. The group shape's parent is the document itself.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(100.0f, 100.0f), group->LocalToParent(System::Drawing::PointF(0.0f, 0.0f)));

// By default, a shape's internal coordinate plane has the top left corner at (0, 0),
// and the bottom right corner at (1000, 1000). Due to its size, our group shape covers an area of 500pt x 500pt
// in the document's plane. This means that a movement of 1pt on the document's coordinate plane will translate
// to a movement of 2pts on the group shape's coordinate plane.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(150.0f, 150.0f), group->LocalToParent(System::Drawing::PointF(100.0f, 100.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(200.0f, 200.0f), group->LocalToParent(System::Drawing::PointF(200.0f, 200.0f)));
ASPOSE_ASSERT_EQ(System::Drawing::PointF(250.0f, 250.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Move the group shape's x and y axis origin from the top left corner to the center.
// This will offset the group's internal coordinates relative to the document's coordinates even further.
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(375.0f, 375.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// Changing the scale of the coordinate plane will also affect relative locations.
group->set_CoordSize(System::Drawing::Size(500, 500));

ASPOSE_ASSERT_EQ(System::Drawing::PointF(650.0f, 650.0f), group->LocalToParent(System::Drawing::PointF(300.0f, 300.0f)));

// If we wish to add a shape to this group while defining its location based on a location in the document,
// we will need to first confirm a location in the group shape that will match the document's location.
ASPOSE_ASSERT_EQ(System::Drawing::PointF(700.0f, 700.0f), group->LocalToParent(System::Drawing::PointF(350.0f, 350.0f)));

auto shape = MakeObject<Shape>(doc, ShapeType::Rectangle);
shape->set_Width(100);
shape->set_Height(100);
shape->set_Left(700);
shape->set_Top(700);

group->AppendChild(shape);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(group);

doc->Save(ArtifactsDir + u"Shape.LocalToParent.docx");
```

## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
