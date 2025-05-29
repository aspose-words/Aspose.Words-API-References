---
title: Stroke Class
linktitle: Stroke
articleTitle: Stroke
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Stroke para mejorar sus formas con trazos personalizables y agregar un toque profesional a sus documentos sin esfuerzo.
type: docs
weight: 1720
url: /es/net/aspose.words.drawing/stroke/
---
## Stroke class

Define un trazo para una forma.

Para obtener más información, visite el[Trabajando con formas](https://docs.aspose.com/words/net/working-with-shapes/) Artículo de documentación.

```csharp
public class Stroke
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BackColor](../../aspose.words.drawing/stroke/backcolor/) { get; set; } | Obtiene o establece el color de fondo del trazo. |
| [BackThemeColor](../../aspose.words.drawing/stroke/backthemecolor/) { get; set; } | Obtiene o establece un objeto ThemeColor que representa el color de fondo del trazo. |
| [BackTintAndShade](../../aspose.words.drawing/stroke/backtintandshade/) { get; set; } | Obtiene o establece un valor doble que aclara u oscurece el color de fondo del trazo. |
| [BaseForeColor](../../aspose.words.drawing/stroke/baseforecolor/) { get; } | Obtiene el color de primer plano base del trazo sin ningún modificador. |
| [Color](../../aspose.words.drawing/stroke/color/) { get; set; } | Define el color de un trazo. |
| [Color2](../../aspose.words.drawing/stroke/color2/) { get; set; } | Define un segundo color para un trazo. |
| [DashStyle](../../aspose.words.drawing/stroke/dashstyle/) { get; set; } | Especifica el patrón de puntos y guiones para un trazo. |
| [EndArrowLength](../../aspose.words.drawing/stroke/endarrowlength/) { get; set; } | Define la longitud de la punta de flecha para el final de un trazo. |
| [EndArrowType](../../aspose.words.drawing/stroke/endarrowtype/) { get; set; } | Define la punta de flecha para el final de un trazo. |
| [EndArrowWidth](../../aspose.words.drawing/stroke/endarrowwidth/) { get; set; } | Define el ancho de la punta de flecha para el final de un trazo. |
| [EndCap](../../aspose.words.drawing/stroke/endcap/) { get; set; } | Define el estilo de tapa para el final de un trazo. |
| [Fill](../../aspose.words.drawing/stroke/fill/) { get; } | Obtiene el formato de relleno para el`Stroke` . |
| [ForeColor](../../aspose.words.drawing/stroke/forecolor/) { get; set; } | Obtiene o establece el color de primer plano del trazo. |
| [ForeThemeColor](../../aspose.words.drawing/stroke/forethemecolor/) { get; set; } | Obtiene o establece un objeto ThemeColor que representa el color de primer plano del trazo. |
| [ForeTintAndShade](../../aspose.words.drawing/stroke/foretintandshade/) { get; set; } | Obtiene o establece un valor doble que aclara u oscurece el color de primer plano del trazo. |
| [ImageBytes](../../aspose.words.drawing/stroke/imagebytes/) { get; } | Define la imagen para una imagen de trazo o relleno de patrón. |
| [JoinStyle](../../aspose.words.drawing/stroke/joinstyle/) { get; set; } | Define el estilo de unión de una polilínea. |
| [LineStyle](../../aspose.words.drawing/stroke/linestyle/) { get; set; } | Define el estilo de línea del trazo. |
| [On](../../aspose.words.drawing/stroke/on/) { get; set; } | Define si se trazará un trazo. |
| [Opacity](../../aspose.words.drawing/stroke/opacity/) { get; set; } | Define el grado de transparencia de un trazo. El rango válido es de 0 a 1. |
| [StartArrowLength](../../aspose.words.drawing/stroke/startarrowlength/) { get; set; } | Define la longitud de la punta de flecha para el inicio de un trazo. |
| [StartArrowType](../../aspose.words.drawing/stroke/startarrowtype/) { get; set; } | Define la punta de flecha para el inicio de un trazo. |
| [StartArrowWidth](../../aspose.words.drawing/stroke/startarrowwidth/) { get; set; } | Define el ancho de la punta de flecha para el inicio de un trazo. |
| [Transparency](../../aspose.words.drawing/stroke/transparency/) { get; set; } | Obtiene o establece un valor entre 0,0 (opaco) y 1,0 (transparente) que representa el grado de transparencia del trazo. |
| [Visible](../../aspose.words.drawing/stroke/visible/) { get; set; } | Obtiene o establece un indicador que indica si el trazo es visible. |
| [Weight](../../aspose.words.drawing/stroke/weight/) { get; set; } | Define el grosor del pincel que traza la ruta de una forma en puntos. |

## Observaciones

Utilice el[`Stroke`](../shape/stroke/)propiedad para acceder a las propiedades del trazo de una forma. No crea instancias de la`Stroke` clase directamente.

## Ejemplos

Muestra cómo cambiar las propiedades del trazo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

//Las formas básicas, como el rectángulo, tienen dos partes visibles.
// 1 - El relleno, que se aplica al área dentro del contorno de la forma:
shape.Fill.ForeColor = Color.White;

// 2 - El trazo, que marca el contorno de la forma:
//Modifica varias propiedades del trazo de esta forma.
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

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
