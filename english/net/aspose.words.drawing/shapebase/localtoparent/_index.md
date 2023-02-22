---
title: LocalToParent
second_title: Aspose.Words for .NET API Reference
description: ShapeBase method. Converts a value from the local coordinate space into the coordinate space of the parent shape in C#.
type: docs
weight: 610
url: /net/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase.LocalToParent method

Converts a value from the local coordinate space into the coordinate space of the parent shape.

```csharp
public PointF LocalToParent(PointF value)
```

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

### See Also

* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../shapebase/)
* assembly [Aspose.Words](../../../)
