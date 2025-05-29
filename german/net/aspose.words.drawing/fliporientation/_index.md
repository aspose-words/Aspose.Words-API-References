---
title: FlipOrientation Enum
linktitle: FlipOrientation
articleTitle: FlipOrientation
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Drawing.FlipOrientation für vielseitige Formausrichtungsoptionen. Verbessern Sie Ihr Dokumentdesign mit flexibler Anpassung!
type: docs
weight: 1290
url: /de/net/aspose.words.drawing/fliporientation/
---
## FlipOrientation enumeration

Mögliche Werte für die Ausrichtung einer Form.

```csharp
[Flags]
public enum FlipOrientation
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Koordinaten werden nicht umgedreht. |
| Horizontal | `1` | Spiegeln Sie entlang der y-Achse und kehren Sie die x-Koordinaten um. |
| Vertical | `2` | Spiegeln Sie entlang der x-Achse und kehren Sie die y-Koordinaten um. |
| Both | `3` | Spiegeln Sie entlang der y- und x-Achse. |

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

* property [FlipOrientation](../shapebase/fliporientation/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
