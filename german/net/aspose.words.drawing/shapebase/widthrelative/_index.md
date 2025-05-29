---
title: ShapeBase.WidthRelative
linktitle: WidthRelative
articleTitle: WidthRelative
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase WidthRelative-Eigenschaft, um die Formbreite einfach als Prozentsatz anzupassen und so die Flexibilität und Präzision Ihres Designs zu verbessern.
type: docs
weight: 620
url: /de/net/aspose.words.drawing/shapebase/widthrelative/
---
## ShapeBase.WidthRelative property

Ruft den Wert ab oder legt ihn fest, der den Prozentsatz der relativen Breite der Form darstellt.

```csharp
public float WidthRelative { get; set; }
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
