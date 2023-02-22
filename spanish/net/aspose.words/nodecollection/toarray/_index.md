---
title: NodeCollection.ToArray
second_title: Referencia de API de Aspose.Words para .NET
description: NodeCollection método. Copia todos los nodos de la colección a una nueva matriz de nodos.
type: docs
weight: 110
url: /es/net/aspose.words/nodecollection/toarray/
---
## NodeCollection.ToArray method

Copia todos los nodos de la colección a una nueva matriz de nodos.

```csharp
public Node[] ToArray()
```

### Valor_devuelto

Una matriz de nodos.

### Observaciones

No debe agregar/eliminar nodos mientras itera sobre una colección de nodos porque invalida el iterador y requiere actualizaciones para colecciones en vivo.

Para poder agregar/eliminar nodos durante la iteración, use este método para copiar nodos en una matriz de tamaño fijo y luego iterar sobre la matriz.

### Ejemplos

Muestra cómo reemplazar todas las formas de cuadro de texto con formas de imagen.

```csharp
Document doc = new Document(MyDir + "Textboxes in drawing canvas.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(3, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(1, shapes.Count(s => s.ShapeType == ShapeType.Image));

foreach (Shape shape in shapes)
{
    if (shape.ShapeType == ShapeType.TextBox)
    {
        Shape replacementShape = new Shape(doc, ShapeType.Image);
        replacementShape.ImageData.SetImage(ImageDir + "Logo.jpg");
        replacementShape.Left = shape.Left;
        replacementShape.Top = shape.Top;
        replacementShape.Width = shape.Width;
        replacementShape.Height = shape.Height;
        replacementShape.RelativeHorizontalPosition = shape.RelativeHorizontalPosition;
        replacementShape.RelativeVerticalPosition = shape.RelativeVerticalPosition;
        replacementShape.HorizontalAlignment = shape.HorizontalAlignment;
        replacementShape.VerticalAlignment = shape.VerticalAlignment;
        replacementShape.WrapType = shape.WrapType;
        replacementShape.WrapSide = shape.WrapSide;

        shape.ParentNode.InsertAfter(replacementShape, shape);
        shape.Remove();
    }
}

shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(0, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(4, shapes.Count(s => s.ShapeType == ShapeType.Image));

doc.Save(ArtifactsDir + "Shape.ReplaceTextboxesWithImages.docx");
```

### Ver también

* class [Node](../../node/)
* class [NodeCollection](../)
* espacio de nombres [Aspose.Words](../../nodecollection/)
* asamblea [Aspose.Words](../../../)


