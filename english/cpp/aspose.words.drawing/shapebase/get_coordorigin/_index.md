---
title: get_CoordOrigin
second_title: Aspose.Words for C++ API Reference
description: The coordinates at the top-left corner of the containing block of this shape.
type: docs
weight: 144
url: /cpp/aspose.words.drawing/shapebase/get_coordorigin/
---
## ShapeBase::get_CoordOrigin method


The coordinates at the top-left corner of the containing block of this shape.

```cpp
System::Drawing::Point Aspose::Words::Drawing::ShapeBase::get_CoordOrigin()
```

## Remarks


The default value is (0,0).

## Examples



Shows how to create and populate a group shape. 
```cpp
auto doc = MakeObject<Document>();

// Create a group shape. A group shape can display a collection of child shape nodes.
// In Microsoft Word, clicking within the group shape's boundary or on one of the group shape's child shapes will
// select all the other child shapes within this group and allow us to scale and move all the shapes at once.
auto group = MakeObject<GroupShape>(doc);

ASSERT_EQ(WrapType::None, group->get_WrapType());

// Create a 400pt x 400pt group shape and place it at the document's floating shape coordinate origin.
group->set_Bounds(System::Drawing::RectangleF(0.0f, 0.0f, 400.0f, 400.0f));

// Set the group's internal coordinate plane size to 500 x 500pt.
// The top left corner of the group will have an x and y coordinate of (0, 0),
// and the bottom right corner will have an x and y coordinate of (500, 500).
group->set_CoordSize(System::Drawing::Size(500, 500));

// Set the coordinates of the top left corner of the group to (-250, -250).
// The group's center will now have an x and y coordinate value of (0, 0),
// and the bottom right corner will be at (250, 250).
group->set_CoordOrigin(System::Drawing::Point(-250, -250));

// Create a rectangle that will display the boundary of this group shape and add it to the group.
auto rectangle = MakeObject<Shape>(doc, ShapeType::Rectangle);
rectangle->set_Width(group->get_CoordSize().get_Width());
rectangle->set_Height(group->get_CoordSize().get_Height());
rectangle->set_Left(group->get_CoordOrigin().get_X());
rectangle->set_Top(group->get_CoordOrigin().get_Y());
group->AppendChild(rectangle);

// Once a shape is a part of a group shape, we can access it as a child node and then modify it.
(System::DynamicCast<Shape>(group->GetChild(NodeType::Shape, 0, true)))->get_Stroke()->set_DashStyle(DashStyle::Dash);

// Create a small red star and insert it into the group.
// Line up the shape with the group's coordinate origin, which we have moved to the center.
auto smallRedStar = MakeObject<Shape>(doc, ShapeType::Star);
smallRedStar->set_Width(20);
smallRedStar->set_Height(20);
smallRedStar->set_Left(-10);
smallRedStar->set_Top(-10);
smallRedStar->set_FillColor(System::Drawing::Color::get_Red());
group->AppendChild(smallRedStar);

// Insert a rectangle, and then insert a slightly smaller rectangle in the same place with an image.
// Newer shapes that we add to the group overlap older shapes. The light blue rectangle will partially overlap the red star,
// and then the shape with the image will overlap the light blue rectangle, using it as a frame.
// We cannot use the "ZOrder" properties of shapes to manipulate their arrangement within a group shape.
auto lightBlueRectangle = MakeObject<Shape>(doc, ShapeType::Rectangle);
lightBlueRectangle->set_Width(250);
lightBlueRectangle->set_Height(250);
lightBlueRectangle->set_Left(-250);
lightBlueRectangle->set_Top(-250);
lightBlueRectangle->set_FillColor(System::Drawing::Color::get_LightBlue());
group->AppendChild(lightBlueRectangle);

auto image = MakeObject<Shape>(doc, ShapeType::Image);
image->set_Width(200);
image->set_Height(200);
image->set_Left(-225);
image->set_Top(-225);
group->AppendChild(image);

(System::DynamicCast<Shape>(group->GetChild(NodeType::Shape, 3, true)))->get_ImageData()->SetImage(ImageDir + u"Logo.jpg");

// Insert a text box into the group shape. Set the "Left" property so that the text box's right edge
// touches the right boundary of the group shape. Set the "Top" property so that the text box sits outside
// the boundary of the group shape, with its top size lined up along the group shape's bottom margin.
auto textBox = MakeObject<Shape>(doc, ShapeType::TextBox);
textBox->set_Width(200);
textBox->set_Height(50);
textBox->set_Left(group->get_CoordSize().get_Width() + group->get_CoordOrigin().get_X() - 200);
textBox->set_Top(group->get_CoordSize().get_Height() + group->get_CoordOrigin().get_Y());
group->AppendChild(textBox);

auto builder = MakeObject<DocumentBuilder>(doc);
builder->InsertNode(group);
builder->MoveTo((System::DynamicCast<Shape>(group->GetChild(NodeType::Shape, 4, true)))->AppendChild(MakeObject<Paragraph>(doc)));
builder->Write(u"Hello world!");

doc->Save(ArtifactsDir + u"Shape.GroupShape.docx");
```


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
