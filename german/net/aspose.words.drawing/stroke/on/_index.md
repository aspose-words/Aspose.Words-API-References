---
title: Stroke.On
linktitle: On
articleTitle: On
second_title: Aspose.Words für .NET
description: Steuern Sie die Pfadgestaltung mit der Eigenschaft „Strich ein“. Optimieren Sie Ihre Designs, indem Sie die Strichführung für Pfade definieren und so ein elegantes, professionelles Aussehen erzielen.
type: docs
weight: 190
url: /de/net/aspose.words.drawing/stroke/on/
---
## Stroke.On property

Definiert, ob der Pfad mit Strichen versehen wird.

```csharp
public bool On { get; set; }
```

## Bemerkungen

Der Standardwert für eine[`Shape`](../../shape/) Ist`WAHR`.

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
