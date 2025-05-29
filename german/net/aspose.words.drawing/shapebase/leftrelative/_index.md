---
title: ShapeBase.LeftRelative
linktitle: LeftRelative
articleTitle: LeftRelative
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase LeftRelative-Eigenschaft, um die relative linke Position von Formen einfach prozentual anzupassen. Verbessern Sie noch heute Ihre Designpräzision!
type: docs
weight: 400
url: /de/net/aspose.words.drawing/shapebase/leftrelative/
---
## ShapeBase.LeftRelative property

Ruft den Wert ab oder legt ihn fest, der die relative linke Position der Form in Prozent darstellt.

```csharp
public float LeftRelative { get; set; }
```

## Beispiele

Zeigt, wie die relative Größe und Position festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Hinzufügen einer einfachen Form mit absoluter Größe und Position.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// WrapType auf WrapType.None setzen, da Inline-Formen automatisch in absolute Einheiten konvertiert werden.
shape.WrapType = WrapType.None;

// Überprüfen und Festlegen der relativen horizontalen Größe.
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // Festlegen der horizontalen Größenbindung an den Rand.
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // Einstellen der Breite auf 50 % der Randbreite.
    shape.WidthRelative = 50;
}

// Überprüfen und Festlegen der relativen vertikalen Größe.
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // Festlegen der vertikalen Größenbindung an den Rand.
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // Einstellen der Höhe auf 30 % der Randhöhe.
    shape.HeightRelative = 30;
}

// Überprüfen und Festlegen der relativen vertikalen Position.
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // Festlegen der Positionsbindung an TopMargin.
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // Relatives Top auf 30 % der TopMargin-Position festlegen.
    shape.TopRelative = 30;
}

// Überprüfen und Festlegen der relativen horizontalen Position.
if (shape.RelativeHorizontalPosition == RelativeHorizontalPosition.Default)
{
    // Festlegen der Positionsbindung auf RightMargin.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.RightMargin;
    // Der relative Positionswert kann negativ sein.
    shape.LeftRelative = -260;
}

doc.Save(ArtifactsDir + "Shape.RelativeSizeAndPosition.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
