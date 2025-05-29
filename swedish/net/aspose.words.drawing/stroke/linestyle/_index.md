---
title: Stroke.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Stroke LineStyle för att anpassa din design med unika linjestilar för linjer, vilket förbättrar ditt projekts visuella attraktionskraft.
type: docs
weight: 180
url: /sv/net/aspose.words.drawing/stroke/linestyle/
---
## Stroke.LineStyle property

Definierar linjestilen för linjen.

```csharp
public ShapeLineStyle LineStyle { get; set; }
```

## Anmärkningar

Standardvärdet ärSingle.

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

* enum [ShapeLineStyle](../../shapelinestyle/)
* class [Stroke](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
