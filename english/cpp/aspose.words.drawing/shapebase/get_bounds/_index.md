---
title: get_Bounds
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the location and size of the containing block of the shape.
type: docs
weight: 92
url: /cpp/aspose.words.drawing/shapebase/get_bounds/
---
## ShapeBase.get_Bounds method


Gets or sets the location and size of the containing block of the shape.

```cpp
System::Drawing::RectangleF Aspose::Words::Drawing::ShapeBase::get_Bounds()
```


Ignores aspect ratio lock upon setting.

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

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

