---
title: RelativeHorizontalSize Enum
linktitle: RelativeHorizontalSize
articleTitle: RelativeHorizontalSize
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Drawing.RelativeHorizontalSize für präzise Kontrolle über Form- und Textrahmenbreiten in Ihren Dokumenten. Verbessern Sie noch heute Ihre Formatierung!
type: docs
weight: 1590
url: /de/net/aspose.words.drawing/relativehorizontalsize/
---
## RelativeHorizontalSize enumeration

Gibt an, relativ zu was die Breite einer Form oder eines Textrahmens horizontal berechnet wird.

```csharp
public enum RelativeHorizontalSize
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Margin | `0` | Gibt an, dass die Breite relativ zum Abstand zwischen dem linken und rechten Rand berechnet wird. |
| Page | `1` | Gibt an, dass die Breite relativ zur Seitenbreite berechnet wird. |
| LeftMargin | `2` | Gibt an, dass die Breite relativ zur Größe des linken Randbereichs berechnet wird. |
| RightMargin | `3` | Gibt an, dass die Breite relativ zur Größe des rechten Randbereichs berechnet wird. |
| InnerMargin | `4` | Gibt an, dass die Breite relativ zur Größe des inneren Randbereichs, zur Größe des linken Randbereichs für ungerade Seiten und zur Größe des rechten Randbereichs für gerade Seiten berechnet wird. |
| OuterMargin | `5` | Gibt an, dass die Breite relativ zur Größe des äußeren Randbereichs, zur Größe des rechten Randbereichs für ungerade Seiten und zur Größe des linken Randbereichs für gerade Seiten berechnet wird. |
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

* property [RelativeHorizontalSize](../shapebase/relativehorizontalsize/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
