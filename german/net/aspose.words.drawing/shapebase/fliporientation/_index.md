---
title: ShapeBase.FlipOrientation
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase FlipOrientation-Eigenschaft, um mühelos die Ausrichtung Ihrer Form zu ändern und Ihre Designs mit Leichtigkeit und Kreativität zu verbessern.
type: docs
weight: 180
url: /de/net/aspose.words.drawing/shapebase/fliporientation/
---
## ShapeBase.FlipOrientation property

Ändert die Ausrichtung einer Form.

```csharp
public FlipOrientation FlipOrientation { get; set; }
```

## Bemerkungen

Der Standardwert istNone.

## Beispiele

Zeigt, wie eine Form auf einer Achse umgedreht wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie eine Bildform ein und belassen Sie ihre Ausrichtung im Standardzustand.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

Assert.AreEqual(FlipOrientation.None, shape.FlipOrientation);

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Setzen Sie die Eigenschaft „FlipOrientation“ auf „FlipOrientation.Horizontal“, um die zweite Form auf der Y-Achse zu spiegeln.
// und macht es zu einem horizontalen Spiegelbild der ersten Form.
shape.FlipOrientation = FlipOrientation.Horizontal;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Setzen Sie die Eigenschaft „FlipOrientation“ auf „FlipOrientation.Horizontal“, um die dritte Form auf der x-Achse umzudrehen,
// und macht es zu einem vertikalen Spiegelbild der ersten Form.
shape.FlipOrientation = FlipOrientation.Vertical;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 250,
    RelativeVerticalPosition.TopMargin, 250, 100, 100, WrapType.None);
shape.ImageData.SetImage(ImageDir + "Logo.jpg");

// Setzen Sie die Eigenschaft „FlipOrientation“ auf „FlipOrientation.Horizontal“, um die vierte Form sowohl auf der x- als auch auf der y-Achse zu spiegeln.
// und macht es zu einem horizontalen und vertikalen Spiegelbild der ersten Form.
shape.FlipOrientation = FlipOrientation.Both;

doc.Save(ArtifactsDir + "Shape.FlipShapeOrientation.docx");
```

### Siehe auch

* enum [FlipOrientation](../../fliporientation/)
* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
