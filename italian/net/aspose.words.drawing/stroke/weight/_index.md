---
title: Stroke.Weight
linktitle: Weight
articleTitle: Weight
second_title: Aspose.Words per .NET
description: Stroke Weight proprietà. Definisce lo spessore del pennello che traccia il percorso di una forma in punti in C#.
type: docs
weight: 210
url: /it/net/aspose.words.drawing/stroke/weight/
---
## Stroke.Weight property

Definisce lo spessore del pennello che traccia il percorso di una forma in punti.

```csharp
public double Weight { get; set; }
```

## Osservazioni

Il valore predefinito per a[`Shape`](../../shape/) è 0,75.

## Esempi

Mostra come modificare le proprietà del tratto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Le forme base, come il rettangolo, hanno due parti visibili.
// 1 - Il riempimento, che si applica all'area all'interno del contorno della forma:
shape.Fill.ForeColor = Color.White;

// 2 - Il tratto, che segna il contorno della forma:
// Modifica varie proprietà del tratto di questa forma.
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

### Guarda anche

* class [Stroke](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
