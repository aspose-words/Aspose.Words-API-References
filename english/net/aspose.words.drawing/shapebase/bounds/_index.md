---
title: ShapeBase.Bounds
second_title: Aspose.Words for .NET API Reference
description: ShapeBase property. Gets or sets the location and size of the containing block of the shape in C#
type: docs
weight: 70
url: /net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

Gets or sets the location and size of the containing block of the shape.

```csharp
public RectangleF Bounds { get; set; }
```

## Remarks

Ignores aspect ratio lock upon setting.

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

## Examples

Shows how to verify shape containing block boundaries.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// Even though the line itself takes up little space on the document page,
// it occupies a rectangular containing block, the size of which we can determine using the "Bounds" properties.
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// Create a group shape, and then set the size of its containing block using the "Bounds" property.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// Create a rectangle, verify the size of its bounding block, and then add it to the group shape.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// The group shape's coordinate plane has its origin on the top left-hand side corner of its containing block,
// and the x and y coordinates of (1000, 1000) on the bottom right-hand side corner.
// Our group shape is 250x250pt in size, so every 4pt on the group shape's coordinate plane
// translates to 1pt in the document body's coordinate plane.
// Every shape that we insert will also shrink in size by a factor of 4.
// The change in the shape's "BoundsInPoints" property will reflect this.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// Insert a shape and place it outside of the bounds of the group shape's containing block.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// The group shape's footprint in the document body has increased, but the containing block remains the same.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
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
* namespace [Aspose.Words.Drawing](../../shapebase/)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
