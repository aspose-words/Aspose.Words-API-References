---
title: GradientStop Class
linktitle: GradientStop
articleTitle: GradientStop
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.GradientStop, su solución para crear degradados impresionantes con paradas personalizables para mejorar las imágenes de sus documentos.
type: docs
weight: 1310
url: /es/net/aspose.words.drawing/gradientstop/
---
## GradientStop class

Representa un paso de gradiente.

Para obtener más información, visite el[Trabajar con elementos gráficos](https://docs.aspose.com/words/net/working-with-graphic-elements/) Artículo de documentación.

```csharp
public class GradientStop
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [GradientStop](gradientstop/#constructor)(*Color, double*) | Inicializa una nueva instancia del`GradientStop` clase. |
| [GradientStop](gradientstop/#constructor_1)(*Color, double, double*) | Inicializa una nueva instancia del`GradientStop` clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BaseColor](../../aspose.words.drawing/gradientstop/basecolor/) { get; } | Obtiene un valor que representa el color del punto de degradado sin ningún modificador. |
| [Color](../../aspose.words.drawing/gradientstop/color/) { get; set; } | Obtiene o establece un valor que representa el color del punto de degradado. |
| [Position](../../aspose.words.drawing/gradientstop/position/) { get; set; } | Obtiene o establece un valor que representa la posición de una parada dentro del gradiente expresado como un porcentaje en el rango de 0,0 a 1,0. |
| [Transparency](../../aspose.words.drawing/gradientstop/transparency/) { get; set; } | Obtiene o establece un valor que representa la transparencia del relleno de degradado expresado como un porcentaje en el rango de 0,0 a 1,0. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Remove](../../aspose.words.drawing/gradientstop/remove/)() | Elimina el punto de degradado del elemento principal.[`GradientStopCollection`](../gradientstopcollection/) . |

## Ejemplos

Muestra cómo agregar paradas de degradado al relleno de degradado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Obtener la colección de paradas de degradado.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// Cambiar la primera parada del gradiente.
gradientStops[0].Color = Color.Aqua;
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

//Agrega un nuevo punto de degradado al final de la colección.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// Eliminar la parada de degradado en el índice 1.
gradientStops.RemoveAt(1);
// E inserte un nuevo punto de degradado en el mismo índice 1.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

//Eliminar la última parada de degradado en la colección.
gradientStop = gradientStops[2];
gradientStops.Remove(gradientStop);

Assert.AreEqual(2, gradientStops.Count);

Assert.AreEqual(Color.FromArgb(255, 0, 255, 255), gradientStops[0].BaseColor);
Assert.AreEqual(Color.Aqua.ToArgb(), gradientStops[0].Color.ToArgb());
Assert.AreEqual(0.1d, gradientStops[0].Position, 0.01d);
Assert.AreEqual(0.25d, gradientStops[0].Transparency, 0.01d);

Assert.AreEqual(Color.Chocolate.ToArgb(), gradientStops[1].Color.ToArgb());
Assert.AreEqual(0.75d, gradientStops[1].Position, 0.01d);
Assert.AreEqual(0.3d, gradientStops[1].Transparency, 0.01d);

// Utilice la opción de cumplimiento para definir la forma usando DML
// si desea obtener la propiedad "GradientStops" después de guardar el documento.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
