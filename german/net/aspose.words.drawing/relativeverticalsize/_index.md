---
title: RelativeVerticalSize Enum
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Drawing.RelativeVerticalSize, die vertikale Höhenberechnungen für Formen und Textrahmen definiert und so die Präzision des Dokumentlayouts verbessert.
type: docs
weight: 1610
url: /de/net/aspose.words.drawing/relativeverticalsize/
---
## RelativeVerticalSize enumeration

Gibt an, relativ zu welchem Wert die Höhe einer Form oder eines Textrahmens vertikal berechnet wird.

```csharp
public enum RelativeVerticalSize
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Margin | `0` | Gibt an, dass die Höhe relativ zum Abstand zwischen dem oberen und unteren Rand berechnet wird. |
| Page | `1` | Gibt an, dass die Höhe relativ zur Seitenhöhe berechnet wird. |
| TopMargin | `2` | Gibt an, dass die Höhe relativ zur Größe des oberen Randbereichs berechnet wird. |
| BottomMargin | `3` | Gibt an, dass die Höhe relativ zur Größe des unteren Randbereichs berechnet wird. |
| InnerMargin | `4` | Gibt an, dass die Höhe relativ zur Größe des inneren Randbereichs, zur Größe des oberen Randbereichs für ungerade Seiten und zur Größe des unteren Randbereichs für gerade Seiten berechnet wird. |
| OuterMargin | `5` | Gibt an, dass die Höhe relativ zur Größe des äußeren Randbereichs, zur Größe des unteren Randbereichs für ungerade Seiten und zur Größe des oberen Randbereichs für gerade Seiten berechnet wird. |
| Default | `1` | Der Standardwert istMargin . |

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

* property [RelativeVerticalSize](../shapebase/relativeverticalsize/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
