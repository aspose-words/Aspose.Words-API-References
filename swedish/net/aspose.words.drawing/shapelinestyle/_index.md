---
title: ShapeLineStyle Enum
linktitle: ShapeLineStyle
articleTitle: ShapeLineStyle
second_title: Aspose.Words för .NET
description: Upptäck enumerationen Aspose.Words.Drawing.ShapeLineStyle för att förbättra din dokumentdesign med anpassningsbara sammansatta linjestilar för former.
type: docs
weight: 1660
url: /sv/net/aspose.words.drawing/shapelinestyle/
---
## ShapeLineStyle enumeration

Anger den sammansatta linjestilen för en[`Shape`](../shape/) .

```csharp
public enum ShapeLineStyle
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Single | `0` | En rad. |
| Double | `1` | Dubbla linjer med samma bredd. |
| ThickThin | `2` | Dubbla linjer, en tjock, en tunn. |
| ThinThick | `3` | Dubbla linjer, en tunn, en tjock. |
| Triple | `4` | Tre linjer, tunna, tjocka, tunna. |
| Default | `0` | Standardvärdet ärSingle . |

## Exempel

Visar hur man ändrar penseldragsegenskaper.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Grundläggande former, som rektangeln, har två synliga delar.
// 1 - Fyllningen, som gäller området inom formens kontur:
shape.Fill.ForeColor = Color.White;

// 2 - Linjen, som markerar formens konturer:
// Ändra olika egenskaper för den här formens linje.
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

### Se även

* property [LineStyle](../stroke/linestyle/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
