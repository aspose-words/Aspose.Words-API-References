---
title: Enum RelativeHorizontalSize
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.RelativeHorizontalSize opsomming. Gibt relativ dazu an wie die Breite einer Form oder eines Textrahmens horizontal berechnet wird.
type: docs
weight: 1200
url: /de/net/aspose.words.drawing/relativehorizontalsize/
---
## RelativeHorizontalSize enumeration

Gibt relativ dazu an, wie die Breite einer Form oder eines Textrahmens horizontal berechnet wird.

```csharp
public enum RelativeHorizontalSize
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Margin | `0` | Gibt an, dass die Breite relativ zum Abstand zwischen dem linken und dem rechten Rand berechnet wird. |
| Page | `1` | Gibt an, dass die Breite relativ zur Seitenbreite berechnet wird. |
| LeftMargin | `2` | Gibt an, dass die Breite relativ zur Größe des linken Randbereichs berechnet wird. |
| RightMargin | `3` | Gibt an, dass die Breite relativ zur Größe des rechten Randbereichs berechnet wird. |
| InnerMargin | `4` | Gibt an, dass die Breite relativ zur Größe des inneren Randbereichs berechnet wird, zur Größe des linken Randbereichs für ungerade Seiten und zur Größe des rechten Randbereichs für gerade Seiten. |
| OuterMargin | `5` | Gibt an, dass die Breite relativ zur Größe des äußeren Randbereichs berechnet wird, zur Größe des rechten Randbereichs für ungerade Seiten und zur Größe des linken Randbereichs für gerade Seiten. |
| Default | `1` | Der Standardwert istMargin . |

### Beispiele

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

* property [RelativeHorizontalSize](../shapebase/relativehorizontalsize/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)


