---
title: RelativeVerticalSize Enum
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: Aspose.Words für .NET
description: Aspose.Words.Drawing.RelativeVerticalSize opsomming. Gibt relativ dazu an wie die Höhe einer Form oder eines Textrahmens vertikal berechnet wird in C#.
type: docs
weight: 1220
url: /de/net/aspose.words.drawing/relativeverticalsize/
---
## RelativeVerticalSize enumeration

Gibt relativ dazu an, wie die Höhe einer Form oder eines Textrahmens vertikal berechnet wird.

```csharp
public enum RelativeVerticalSize
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Margin | `0` | Gibt an, dass die Höhe relativ zum Abstand zwischen dem oberen und dem unteren Rand berechnet wird. |
| Page | `1` | Gibt an, dass die Höhe relativ zur Seitenhöhe berechnet wird. |
| TopMargin | `2` | Gibt an, dass die Höhe relativ zur Größe des oberen Randbereichs berechnet wird. |
| BottomMargin | `3` | Gibt an, dass die Höhe relativ zur Größe des unteren Randbereichs berechnet wird. |
| InnerMargin | `4` | Gibt an, dass die Höhe relativ zur Größe des inneren Randbereichs, zur Größe des oberen Randbereichs für ungerade Seiten und zur Größe des unteren Randbereichs für gerade Seiten berechnet wird. |
| OuterMargin | `5` | Gibt an, dass die Höhe relativ zur Größe des äußeren Randbereichs berechnet wird, zur Größe des unteren Randbereichs für ungerade Seiten und zur Größe des oberen Randbereichs für gerade Seiten. |
| Default | `1` | Der Standardwert istMargin . |

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

* property [RelativeVerticalSize](../shapebase/relativeverticalsize/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
