---
title: ShapeBase.FlipOrientation
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase eigendom. Ändert die Ausrichtung einer Form.
type: docs
weight: 180
url: /de/net/aspose.words.drawing/shapebase/fliporientation/
---
## ShapeBase.FlipOrientation property

Ändert die Ausrichtung einer Form.

```csharp
public FlipOrientation FlipOrientation { get; set; }
```

### Bemerkungen

Der Standardwert istNone.

### Beispiele

Zeigt, wie eine Form auf einer Achse gespiegelt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügt eine Bildform ein und belässt ihre Ausrichtung im Standardzustand.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

Assert.AreEqual(FlipOrientation.None, shape.FlipOrientation);

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Setzen Sie die Eigenschaft "FlipOrientation" auf "FlipOrientation.Horizontal", um die zweite Form auf der y-Achse zu spiegeln,
// daraus ein horizontales Spiegelbild der ersten Form machen.
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Setzen Sie die Eigenschaft "FlipOrientation" auf "FlipOrientation.Horizontal", um die dritte Form auf der x-Achse zu spiegeln,
// daraus ein vertikales Spiegelbild der ersten Form machen.
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Setzen Sie die Eigenschaft "FlipOrientation" auf "FlipOrientation.Horizontal", um die vierte Form sowohl auf der x- als auch auf der y-Achse zu spiegeln,
// daraus ein horizontales und vertikales Spiegelbild der ersten Form machen.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### Siehe auch

* enum [FlipOrientation](../../fliporientation/)
* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)


