---
title: GradientStop.Remove
second_title: Referencia de API de Aspose.Words para .NET
description: GradientStop método. Elimina la parada de gradiente del padreGradientStopCollection .
type: docs
weight: 50
url: /es/net/aspose.words.drawing/gradientstop/remove/
---
## GradientStop.Remove method

Elimina la parada de gradiente del padre[`GradientStopCollection`](../../gradientstopcollection/) .

```csharp
public void Remove()
```

### Ejemplos

Muestra cómo agregar paradas de degradado al relleno degradado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Obtener la colección de paradas de degradado.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// Cambiar la primera parada de gradiente.
gradientStops[0].Color = Color.Aqua;
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// Agrega una nueva parada de gradiente al final de la colección.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// Eliminar la parada de gradiente en el índice 1.
gradientStops.RemoveAt(1);
// E inserte una nueva parada de gradiente en el mismo índice 1.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// Elimina la última parada de gradiente en la colección.
gradientStop = gradientStops[2];
gradientStops.Remove(gradientStop);

Assert.AreEqual(2, gradientStops.Count);

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

* class [GradientStop](../)
* espacio de nombres [Aspose.Words.Drawing](../../gradientstop/)
* asamblea [Aspose.Words](../../../)


