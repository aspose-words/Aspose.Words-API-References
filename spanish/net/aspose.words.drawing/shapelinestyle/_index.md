---
title: Enum ShapeLineStyle
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.ShapeLineStyle enumeración. Especifica el estilo de línea compuesta de unShape .
type: docs
weight: 1120
url: /es/net/aspose.words.drawing/shapelinestyle/
---
## ShapeLineStyle enumeration

Especifica el estilo de línea compuesta de un[`Shape`](../shape/) .

```csharp
public enum ShapeLineStyle
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Single | `0` | Línea única. |
| Double | `1` | Líneas dobles de igual ancho. |
| ThickThin | `2` | Líneas dobles, una gruesa, una delgada. |
| ThinThick | `3` | Trazos dobles, uno fino, otro grueso. |
| Triple | `4` | Tres líneas, delgada, gruesa, delgada. |
| Default | `0` | El valor predeterminado esSingle . |

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

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### Ver también

* property [LineStyle](../stroke/linestyle/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)


