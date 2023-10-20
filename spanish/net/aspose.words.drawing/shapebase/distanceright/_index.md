---
title: ShapeBase.DistanceRight
linktitle: DistanceRight
articleTitle: DistanceRight
second_title: Aspose.Words para .NET
description: ShapeBase DistanceRight propiedad. Devuelve o establece la distancia en puntos entre el texto del documento y el borde derecho de la forma en C#.
type: docs
weight: 150
url: /es/net/aspose.words.drawing/shapebase/distanceright/
---
## ShapeBase.DistanceRight property

Devuelve o establece la distancia (en puntos) entre el texto del documento y el borde derecho de la forma.

```csharp
public double DistanceRight { get; set; }
```

## Observaciones

El valor predeterminado es 1/8 de pulgada.

Tiene efecto sólo para formas de nivel superior.

## Ejemplos

Muestra cómo establecer la distancia de ajuste para un texto que rodea una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta un rectángulo y consigue que el texto se ajuste firmemente alrededor de sus límites.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 150, 150);
shape.WrapType = WrapType.Tight;

// Establece la distancia mínima entre la forma y el texto circundante en 40 puntos desde todos los lados.
shape.DistanceTop = 40;
shape.DistanceBottom = 40;
shape.DistanceLeft = 40;
shape.DistanceRight = 40;

// Mueve la forma más cerca del centro de la página y luego gira la forma 60 grados en el sentido de las agujas del reloj.
shape.Top = 75;
shape.Left = 150; 
shape.Rotation = 60;

// Agrega texto que rodeará la forma.
builder.Font.Size = 24;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "Shape.Coordinates.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
