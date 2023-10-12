---
title: Stroke.On
second_title: Referencia de API de Aspose.Words para .NET
description: Stroke propiedad. Define si se trazará el camino.
type: docs
weight: 150
url: /es/net/aspose.words.drawing/stroke/on/
---
## Stroke.On property

Define si se trazará el camino.

```csharp
public bool On { get; set; }
```

### Observaciones

El valor predeterminado para un[`Shape`](../../shape/) es`verdadero`.

### Ejemplos

Muestra cómo cambiar las propiedades del trazo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// Las formas básicas, como el rectángulo, tienen dos partes visibles.
// 1 - El relleno, que se aplica al área dentro del contorno de la forma:
shape.Fill.ForeColor = Color.White;

// 2 - El trazo, que marca el contorno de la forma:
// Modifica varias propiedades del trazo de esta forma.
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

### Ver también

* class [Stroke](../)
* espacio de nombres [Aspose.Words.Drawing](../../stroke/)
* asamblea [Aspose.Words](../../../)


