---
title: Stroke.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words per .NET
description: Scopri la proprietà Stroke LineStyle per personalizzare il tuo design con stili di linea unici per i tratti, migliorando l'aspetto visivo del tuo progetto.
type: docs
weight: 180
url: /it/net/aspose.words.drawing/stroke/linestyle/
---
## Stroke.LineStyle property

Definisce lo stile della linea del tratto.

```csharp
public ShapeLineStyle LineStyle { get; set; }
```

## Osservazioni

Il valore predefinito èSingle.

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

* enum [ShapeLineStyle](../../shapelinestyle/)
* class [Stroke](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
