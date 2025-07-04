---
title: ShapeBase.LocalToParent
linktitle: LocalToParent
articleTitle: LocalToParent
second_title: Aspose.Words for .NET
description: Transform local coordinates to parent shape space with the ShapeBase LocalToParent method. Enhance precision in your 3D modeling projects today!
type: docs
weight: 680
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
Assert.That(group.LocalToParent(new PointF(0, 0)), Is.EqualTo(new PointF(100, 100)));

// By default, a shape's internal coordinate plane has the top left corner at (0, 0),
// and the bottom right corner at (1000, 1000). Due to its size, our group shape covers an area of 500pt x 500pt
// in the document's plane. This means that a movement of 1pt on the document's coordinate plane will translate
// to a movement of 2pts on the group shape's coordinate plane.
Assert.That(group.LocalToParent(new PointF(100, 100)), Is.EqualTo(new PointF(150, 150)));
Assert.That(group.LocalToParent(new PointF(200, 200)), Is.EqualTo(new PointF(200, 200)));
Assert.That(group.LocalToParent(new PointF(300, 300)), Is.EqualTo(new PointF(250, 250)));

// Move the group shape's x and y axis origin from the top left corner to the center.
// This will offset the group's internal coordinates relative to the document's coordinates even further.
group.CoordOrigin = new Point(-250, -250);

Assert.That(group.LocalToParent(new PointF(300, 300)), Is.EqualTo(new PointF(375, 375)));

// Changing the scale of the coordinate plane will also affect relative locations.
group.CoordSize = new Size(500, 500);

Assert.That(group.LocalToParent(new PointF(300, 300)), Is.EqualTo(new PointF(650, 650)));

// If we wish to add a shape to this group while defining its location based on a location in the document,
// we will need to first confirm a location in the group shape that will match the document's location.
Assert.That(group.LocalToParent(new PointF(350, 350)), Is.EqualTo(new PointF(700, 700)));

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
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
