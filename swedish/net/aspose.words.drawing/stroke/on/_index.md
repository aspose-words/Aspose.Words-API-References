---
title: Stroke.On
linktitle: On
articleTitle: On
second_title: Aspose.Words för .NET
description: Stroke On fast egendom. Definierar om sökvägen ska streckas i C#.
type: docs
weight: 140
url: /sv/net/aspose.words.drawing/stroke/on/
---
## Stroke.On property

Definierar om sökvägen ska streckas.

```csharp
public bool On { get; set; }
```

## Anmärkningar

Standardvärdet för a[`Shape`](../../shape/) är`Sann`.

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

* class [Stroke](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
