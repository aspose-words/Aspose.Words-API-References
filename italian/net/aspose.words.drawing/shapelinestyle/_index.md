---
title: ShapeLineStyle Enum
linktitle: ShapeLineStyle
articleTitle: ShapeLineStyle
second_title: Aspose.Words per .NET
description: Aspose.Words.Drawing.ShapeLineStyle enum. Specifica lo stile di linea composto di aShape  in C#.
type: docs
weight: 1270
url: /it/net/aspose.words.drawing/shapelinestyle/
---
## ShapeLineStyle enumeration

Specifica lo stile di linea composto di a[`Shape`](../shape/) .

```csharp
public enum ShapeLineStyle
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Single | `0` | Riga singola. |
| Double | `1` | Doppie linee di uguale larghezza. |
| ThickThin | `2` | Doppie linee, una spessa, una sottile. |
| ThinThick | `3` | Doppie linee, una sottile, una spessa. |
| Triple | `4` | Tre linee, sottile, spessa, sottile. |
| Default | `0` | Il valore predefinito èSingle . |

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

* property [LineStyle](../stroke/linestyle/)
* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
