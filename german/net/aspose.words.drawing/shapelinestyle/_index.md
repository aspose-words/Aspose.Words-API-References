---
title: ShapeLineStyle Enum
linktitle: ShapeLineStyle
articleTitle: ShapeLineStyle
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Drawing.ShapeLineStyle, um Ihr Dokumentdesign mit anpassbaren zusammengesetzten Linienstilen für Formen zu verbessern.
type: docs
weight: 1660
url: /de/net/aspose.words.drawing/shapelinestyle/
---
## ShapeLineStyle enumeration

Gibt den zusammengesetzten Linienstil einer[`Shape`](../shape/) .

```csharp
public enum ShapeLineStyle
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Single | `0` | Einzelne Zeile. |
| Double | `1` | Doppelte Linien gleicher Breite. |
| ThickThin | `2` | Doppelte Linien, eine dick, eine dünn. |
| ThinThick | `3` | Doppelte Linien, eine dünn, eine dick. |
| Triple | `4` | Drei Linien, dünn, dick, dünn. |
| Default | `0` | Der Standardwert istSingle . |

## Beispiele

Zeigt, wie Stricheigenschaften geändert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Grundformen wie das Rechteck haben zwei sichtbare Teile.
// 1 – Die Füllung, die auf den Bereich innerhalb des Umrisses der Form angewendet wird:
shape.Fill.ForeColor = Color.White;

// 2 - Der Strich, der den Umriss der Form markiert:
// Verschiedene Eigenschaften des Strichs dieser Form ändern.
Stroke stroke = shape.Stroke;
stroke.On = true;
stroke.Weight = 5;
stroke.Color = Color.Red;
stroke.DashStyle = DashStyle.ShortDashDotDot;
stroke.JoinStyle = JoinStyle.Miter;
stroke.EndCap = EndCap.Square;
stroke.LineStyle = ShapeLineStyle.Triple;
stroke.Fill.TwoColorGradient(Color.Red, Color.Blue, GradientStyle.Vertical, GradientVariant.Variant1);

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### Siehe auch

* property [LineStyle](../stroke/linestyle/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
