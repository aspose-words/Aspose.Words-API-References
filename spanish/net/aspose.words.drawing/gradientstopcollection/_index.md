---
title: GradientStopCollection Class
linktitle: GradientStopCollection
articleTitle: GradientStopCollection
second_title: Aspose.Words para .NET
description: Aspose.Words.Drawing.GradientStopCollection clase. Contiene una colección deGradientStop objetos en C#.
type: docs
weight: 990
url: /es/net/aspose.words.drawing/gradientstopcollection/
---
## GradientStopCollection class

Contiene una colección de[`GradientStop`](../gradientstop/) objetos.

Para obtener más información, visite el[Trabajar con elementos gráficos](https://docs.aspose.com/words/net/working-with-graphic-elements/) artículo de documentación.

```csharp
public class GradientStopCollection : IEnumerable<GradientStop>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.drawing/gradientstopcollection/count/) { get; } | Obtiene un valor entero que indica el número de elementos de la colección. |
| [Item](../../aspose.words.drawing/gradientstopcollection/item/) { get; set; } | Obtiene o establece un[`GradientStop`](../gradientstop/) objeto en la colección. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.drawing/gradientstopcollection/add/)(*[GradientStop](../gradientstop/)*) | Agrega un especificado[`GradientStop`](../gradientstop/) a un gradiente. |
| [GetEnumerator](../../aspose.words.drawing/gradientstopcollection/getenumerator/)() | Devuelve un enumerador que recorre en iteración la colección. |
| [Insert](../../aspose.words.drawing/gradientstopcollection/insert/)(*int, [GradientStop](../gradientstop/)*) | Inserta un[`GradientStop`](../gradientstop/) a la colección en un índice especificado. |
| [Remove](../../aspose.words.drawing/gradientstopcollection/remove/)(*[GradientStop](../gradientstop/)*) | Elimina un especificado[`GradientStop`](../gradientstop/) de la colección. |
| [RemoveAt](../../aspose.words.drawing/gradientstopcollection/removeat/)(*int*) | Elimina un[`GradientStop`](../gradientstop/) de la colección en un índice especificado. |

## Observaciones

No crea instancias de esta clase directamente. Utilice el[`GradientStops`](../fill/gradientstops/)propiedad para acceder a paradas de degradado de objetos de relleno.

## Ejemplos

Muestra cómo agregar paradas de degradado al relleno de degradado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Obtener la colección de paradas de gradiente.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// Cambia la primera parada de gradiente.            
gradientStops[0].Color = Color.Aqua;            
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// Agrega una nueva parada de degradado al final de la colección.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// Elimina la parada de gradiente en el índice 1.
gradientStops.RemoveAt(1);
// E insertamos una nueva parada de gradiente en el mismo índice 1.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// Elimina la última parada de degradado de la colección.
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

// Usa la opción de cumplimiento para definir la forma usando DML
// si desea obtener la propiedad "GradientStops" después de guardar el documento.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### Ver también

* class [GradientStop](../gradientstop/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
