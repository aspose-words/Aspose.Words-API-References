---
title: ShapeBase.ZOrder
linktitle: ZOrder
articleTitle: ZOrder
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad ShapeBase ZOrder mejora su diseño al controlar el orden de visualización de las formas superpuestas para un diseño más claro y organizado.
type: docs
weight: 650
url: /es/net/aspose.words.drawing/shapebase/zorder/
---
## ShapeBase.ZOrder property

Determina el orden de visualización de las formas superpuestas.

```csharp
public int ZOrder { get; set; }
```

## Observaciones

Tiene efecto sólo para formas de nivel superior.

El valor predeterminado es 0.

El número representa la precedencia de apilamiento. Una forma con un número mayor se mostrará como si se superpusiera (delante de) una forma con un número menor.

El orden de las formas superpuestas es independiente para las formas en el encabezado y en el texto main del documento.

El orden de visualización de las formas secundarias en una forma de grupo está determinado por su orden dentro de la forma de grupo.

## Ejemplos

Muestra cómo manipular el orden de las formas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte tres rectángulos de diferentes colores que se superpongan parcialmente entre sí.
// Cuando insertamos una forma que se superpone a otra forma, Aspose.Words coloca la forma más nueva encima de la anterior.
// El rectángulo verde claro se superpondrá al rectángulo azul claro y lo oscurecerá parcialmente.
// y el rectángulo azul claro oscurecerá el rectángulo naranja.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);
shape.FillColor = Color.Orange;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 150,
    RelativeVerticalPosition.TopMargin, 150, 200, 200, WrapType.None);
shape.FillColor = Color.LightBlue;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 200, 200, WrapType.None);
shape.FillColor = Color.LightGreen;

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

// La propiedad "ZOrder" de una forma determina su prioridad de apilamiento entre otras formas superpuestas.
// Si dos formas superpuestas tienen diferentes valores "ZOrder",
 // Microsoft Word colocará la forma con un valor mayor sobre la forma con el valor menor.
// Establezca los valores "ZOrder" de nuestras formas para colocar el primer rectángulo naranja sobre el segundo azul claro
// y el segundo rectángulo azul claro sobre el tercer rectángulo verde claro.
// Esto revertirá su orden de apilamiento original.
shapes[0].ZOrder = 3;
shapes[1].ZOrder = 2;
shapes[2].ZOrder = 1;

doc.Save(ArtifactsDir + "Shape.ZOrder.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
