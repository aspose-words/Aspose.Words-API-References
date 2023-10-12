---
title: Stroke.Fill
second_title: Aspose.Words för .NET API Referens
description: Stroke fast egendom. Får fyllningsformatering förStroke .
type: docs
weight: 100
url: /sv/net/aspose.words.drawing/stroke/fill/
---
## Stroke.Fill property

Får fyllningsformatering för[`Stroke`](../) .

```csharp
public Fill Fill { get; }
```

### Exempel

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

* class [Fill](../../fill/)
* class [Stroke](../)
* namnutrymme [Aspose.Words.Drawing](../../stroke/)
* hopsättning [Aspose.Words](../../../)


