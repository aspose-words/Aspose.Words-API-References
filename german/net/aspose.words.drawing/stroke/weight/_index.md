---
title: Stroke.Weight
linktitle: Weight
articleTitle: Weight
second_title: Aspose.Words für .NET
description: Entdecken Sie die Strichstärke-Eigenschaft, um die Pinselstärke für Formen anzupassen. Verbessern Sie Ihre Designs mit präzisen Pfadstrichen in Punkten!
type: docs
weight: 260
url: /de/net/aspose.words.drawing/stroke/weight/
---
## Stroke.Weight property

Definiert die Pinseldicke in Punkten, mit der der Pfad einer Form nachgezeichnet wird.

```csharp
public double Weight { get; set; }
```

## Bemerkungen

Der Standardwert für eine[`Shape`](../../shape/) beträgt 0,75.

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

* class [Stroke](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
