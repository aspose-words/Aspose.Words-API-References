---
title: Stroke.JoinStyle
second_title: Aspose.Words för .NET API Referens
description: Stroke fast egendom. Definierar kopplingsstilen för en polylinje.
type: docs
weight: 130
url: /sv/net/aspose.words.drawing/stroke/joinstyle/
---
## Stroke.JoinStyle property

Definierar kopplingsstilen för en polylinje.

```csharp
public JoinStyle JoinStyle { get; set; }
```

### Anmärkningar

Standardvärdet ärRound.

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

* enum [JoinStyle](../../joinstyle/)
* class [Stroke](../)
* namnutrymme [Aspose.Words.Drawing](../../stroke/)
* hopsättning [Aspose.Words](../../../)


