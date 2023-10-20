---
title: ShapeBase.RelativeHorizontalSize
linktitle: RelativeHorizontalSize
articleTitle: RelativeHorizontalSize
second_title: Aspose.Words für .NET
description: ShapeBase RelativeHorizontalSize eigendom. Ruft den Wert der relativen Größe der Form in horizontaler Richtung ab oder legt diesen fest in C#.
type: docs
weight: 430
url: /de/net/aspose.words.drawing/shapebase/relativehorizontalsize/
---
## ShapeBase.RelativeHorizontalSize property

Ruft den Wert der relativen Größe der Form in horizontaler Richtung ab oder legt diesen fest.

```csharp
public RelativeHorizontalSize RelativeHorizontalSize { get; set; }
```

## Bemerkungen

Der Standardwert ist[`RelativeHorizontalSize`](../../relativehorizontalsize/).

Hat nur Wirkung, wenn[`WidthRelative`](../widthrelative/) eingestellt ist.

## Beispiele

Zeigt, wie die relative Größe und Position festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine einfache Form mit absoluter Größe und Position hinzufügen.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// WrapType auf WrapType.None setzen, da Inline-Formen automatisch in absolute Einheiten konvertiert werden.
shape.WrapType = WrapType.None;

// Überprüfen und Einstellen der relativen horizontalen Größe.
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // Die horizontale Größenbindung auf Margin setzen.
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // Breite auf 50 % der Randbreite setzen.
    shape.WidthRelative = 50;
}

// Überprüfen und Einstellen der relativen vertikalen Größe.
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // Die vertikale Größenbindung auf Margin setzen.
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // Höhe auf 30 % der Randhöhe einstellen.
    shape.HeightRelative = 30;
}

// Überprüfen und Einstellen der relativen vertikalen Position.
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // Festlegen der Positionsbindung an TopMargin.
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // Relatives Top auf 30 % der TopMargin-Position setzen.
    shape.TopRelative = 30;
}

// Überprüfen und Einstellen der relativen horizontalen Position.
if (shape.RelativeHorizontalPosition == RelativeHorizontalPosition.Default)
{
    // Positionsbindung auf RightMargin setzen.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.RightMargin;
    // Der Positionsrelativwert kann negativ sein.
    shape.LeftRelative = -260;
}

doc.Save(ArtifactsDir + "Shape.RelativeSizeAndPosition.docx");
```

### Siehe auch

* enum [RelativeHorizontalSize](../../relativehorizontalsize/)
* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
