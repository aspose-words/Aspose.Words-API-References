---
title: ShapeBase.AdjustWithEffects
second_title: Referencia de API de Aspose.Words para .NET
description: ShapeBase método. Agrega al rectángulo de origen los valores de la extensión del efecto y devuelve el rectángulo final.
type: docs
weight: 560
url: /es/net/aspose.words.drawing/shapebase/adjustwitheffects/
---
## ShapeBase.AdjustWithEffects method

Agrega al rectángulo de origen los valores de la extensión del efecto y devuelve el rectángulo final.

```csharp
public RectangleF AdjustWithEffects(RectangleF source)
```

### Ejemplos

Muestra cómo comprobar cómo los límites de una forma se ven afectados por los efectos de forma.

```csharp
Document doc = new Document(MyDir + "Shape shadow effect.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// Las dos formas son idénticas en términos de dimensiones y tipo de forma.
Assert.AreEqual(shapes[0].Width, shapes[1].Width);
Assert.AreEqual(shapes[0].Height, shapes[1].Height);
Assert.AreEqual(shapes[0].ShapeType, shapes[1].ShapeType);

// La primera forma no tiene efectos, y la segunda tiene una sombra y un contorno grueso.
// Estos efectos hacen que el tamaño de la silueta de la segunda forma sea mayor que el de la primera.
// Aunque el tamaño del rectángulo aparece cuando hacemos clic en estas formas en Microsoft Word,
// los límites exteriores visibles de la segunda forma se ven afectados por la sombra y el contorno y, por lo tanto, son más grandes.
// Podemos usar el método "AdjustWithEffects" para ver el tamaño real de la forma.
Assert.AreEqual(0.0, shapes[0].StrokeWeight);
Assert.AreEqual(20.0, shapes[1].StrokeWeight);
Assert.False(shapes[0].ShadowEnabled);
Assert.True(shapes[1].ShadowEnabled);

Shape shape = shapes[0];

// Crea un objeto RectangleF, que representa un rectángulo,
// que potencialmente podríamos usar como coordenadas y límites para una forma.
RectangleF rectangleF = new RectangleF(200, 200, 1000, 1000);

// Ejecute este método para ajustar el tamaño del rectángulo para todos nuestros efectos de forma.
RectangleF rectangleFOut = shape.AdjustWithEffects(rectangleF);

// Dado que la forma no tiene efectos de cambio de borde, las dimensiones de sus límites no se ven afectadas.
Assert.AreEqual(200, rectangleFOut.X);
Assert.AreEqual(200, rectangleFOut.Y);
Assert.AreEqual(1000, rectangleFOut.Width);
Assert.AreEqual(1000, rectangleFOut.Height);

// Verifica la extensión final de la primera forma, en puntos.
Assert.AreEqual(0, shape.BoundsWithEffects.X);
Assert.AreEqual(0, shape.BoundsWithEffects.Y);
Assert.AreEqual(147, shape.BoundsWithEffects.Width);
Assert.AreEqual(147, shape.BoundsWithEffects.Height);

shape = shapes[1];
rectangleF = new RectangleF(200, 200, 1000, 1000);
rectangleFOut = shape.AdjustWithEffects(rectangleF);

// Los efectos de forma han movido ligeramente la esquina superior izquierda aparente de la forma.
Assert.AreEqual(171.5, rectangleFOut.X);
Assert.AreEqual(167, rectangleFOut.Y);

// Los efectos también han afectado las dimensiones visibles de la forma.
Assert.AreEqual(1045, rectangleFOut.Width);
Assert.AreEqual(1132, rectangleFOut.Height);

// Los efectos también han afectado los límites visibles de la forma.
Assert.AreEqual(-28.5, shape.BoundsWithEffects.X);
Assert.AreEqual(-33, shape.BoundsWithEffects.Y);
Assert.AreEqual(192, shape.BoundsWithEffects.Width);
Assert.AreEqual(279, shape.BoundsWithEffects.Height);
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../shapebase/)
* asamblea [Aspose.Words](../../../)


