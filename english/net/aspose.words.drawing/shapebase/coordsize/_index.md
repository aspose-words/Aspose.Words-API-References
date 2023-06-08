---
title: ShapeBase.CoordSize
linktitle: CoordSize
articleTitle: CoordSize
second_title: Aspose.Words for .NET
description: ShapeBase CoordSize property. The width and height of the coordinate space inside the containing block of this shape in C#.
type: docs
weight: 120
url: /net/aspose.words.drawing/shapebase/coordsize/
---
## ShapeBase.CoordSize property

The width and height of the coordinate space inside the containing block of this shape.

```csharp
public Size CoordSize { get; set; }
```

## Remarks

The default value is (1000, 1000).

## Examples

Shows how to translate the x and y coordinate location on a shape's coordinate plane to a location on the parent shape's coordinate plane.

```csharp
Document doc = new Document();

// Insert a group shape, and place it 100 points below and to the right of
// the document's x and Y coordinate origin point.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Use the "LocalToParent" method to determine that (0, 0) on the group's internal x and y coordinates
// lies on (100, 100) of its parent shape's coordinate system. The group shape's parent is the document itself.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// By default, a shape's internal coordinate plane has the top left corner at (0, 0),
// and the bottom right corner at (1000, 1000). Due to its size, our group shape covers an area of 500pt x 500pt
// in the document's plane. This means that a movement of 1pt on the document's coordinate plane will translate
// to a movement of 2pts on the group shape's coordinate plane.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Move the group shape's x and y axis origin from the top left corner to the center.
// This will offset the group's internal coordinates relative to the document's coordinates even further.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// Changing the scale of the coordinate plane will also affect relative locations.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// If we wish to add a shape to this group while defining its location based on a location in the document,
// we will need to first confirm a location in the group shape that will match the document's location.
Assert.AreEqual(new PointF(700, 700), group.LocalToParent(new PointF(350, 350)));

Shape shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

group.AppendChild(shape);
doc.FirstSection.Body.FirstParagraph.AppendChild(group);

doc.Save(ArtifactsDir + "Shape.LocalToParent.docx");
```

Shows how to create and populate a group shape.

```csharp
Document doc = new Document();

// Create a group shape. A group shape can display a collection of child shape nodes.
// In Microsoft Word, clicking within the group shape's boundary or on one of the group shape's child shapes will
// select all the other child shapes within this group and allow us to scale and move all the shapes at once.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// Create a 400pt x 400pt group shape and place it at the document's floating shape coordinate origin.
group.Bounds = new RectangleF(0, 0, 400, 400);

// Set the group's internal coordinate plane size to 500 x 500pt. 
// The top left corner of the group will have an x and y coordinate of (0, 0),
// and the bottom right corner will have an x and y coordinate of (500, 500).
group.CoordSize = new Size(500, 500);

// Set the coordinates of the top left corner of the group to (-250, -250). 
// The group's center will now have an x and y coordinate value of (0, 0),
// and the bottom right corner will be at (250, 250).
group.CoordOrigin = new Point(-250, -250);

// Create a rectangle that will display the boundary of this group shape and add it to the group.
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
});

// Once a shape is a part of a group shape, we can access it as a child node and then modify it.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// Create a small red star and insert it into the group.
// Line up the shape with the group's coordinate origin, which we have moved to the center.
group.AppendChild(new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
});

// Insert a rectangle, and then insert a slightly smaller rectangle in the same place with an image. 
// Newer shapes that we add to the group overlap older shapes. The light blue rectangle will partially overlap the red star,
// and then the shape with the image will overlap the light blue rectangle, using it as a frame.
// We cannot use the "ZOrder" properties of shapes to manipulate their arrangement within a group shape. 
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = 250,
    Height = 250,
    Left = -250,
    Top = -250,
    FillColor = Color.LightBlue
});

group.AppendChild(new Shape(doc, ShapeType.Image)
{
    Width = 200,
    Height = 200,
    Left = -225,
    Top = -225
});

((Shape)group.GetChild(NodeType.Shape, 3, true)).ImageData.SetImage(ImageDir + "Logo.jpg");

// Insert a text box into the group shape. Set the "Left" property so that the text box's right edge
// touches the right boundary of the group shape. Set the "Top" property so that the text box sits outside
// the boundary of the group shape, with its top size lined up along the group shape's bottom margin.
group.AppendChild(new Shape(doc, ShapeType.TextBox)
{
    Width = 200,
    Height = 50,
    Left = group.CoordSize.Width + group.CoordOrigin.X - 200,
    Top = group.CoordSize.Height + group.CoordOrigin.Y
});

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(group);
builder.MoveTo(((Shape)group.GetChild(NodeType.Shape, 4, true)).AppendChild(new Paragraph(doc)));
builder.Write("Hello world!");

doc.Save(ArtifactsDir + "Shape.GroupShape.docx");
```

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
