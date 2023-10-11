---
title: GradientStop.Transparency
second_title: Referencia de API de Aspose.Words para .NET
description: GradientStop propiedad. Obtiene o establece un valor que representa la transparencia del gradiente fill expresado como porcentaje en el rango de 00 a 10.
type: docs
weight: 50
url: /es/net/aspose.words.drawing/gradientstop/transparency/
---
## GradientStop.Transparency property

Obtiene o establece un valor que representa la transparencia del gradiente fill expresado como porcentaje en el rango de 0,0 a 1,0.

```csharp
public double Transparency { get; set; }
```

### Ejemplos

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

* class [GradientStop](../)
* espacio de nombres [Aspose.Words.Drawing](../../gradientstop/)
* asamblea [Aspose.Words](../../../)


