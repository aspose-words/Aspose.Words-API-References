---
title: ShapeLineStyle Enum
linktitle: ShapeLineStyle
articleTitle: ShapeLineStyle
second_title: Aspose.Words för .NET
description: Aspose.Words.Drawing.ShapeLineStyle uppräkning. Anger den sammansatta linjestilen för enShape  i C#.
type: docs
weight: 1270
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
| Single | `0` | Enkel linje. |
| Double | `1` | Dubbla linjer med samma bredd. |
| ThickThin | `2` | Dubbla linjer, en tjock, en tunn. |
| ThinThick | `3` | Dubbla linjer, en tunn, en tjock. |
| Triple | `4` | Tre linjer, tunn, tjock, tunn. |
| Default | `0` | Standardvärdet ärSingle . |

## Exempel

Visar hur man ändrar slagegenskaper.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Grundformer, som rektangeln, har två synliga delar.
// 1 - Fyllningen, som gäller området inom konturen av formen:
shape.Fill.ForeColor = Color.White;

// 2 - Stroget, som markerar konturen av formen:
// Ändra olika egenskaper för denna forms streck.
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
