---
title: InsertAfter
second_title: Referencia de API de Aspose.Words para .NET
description: Inserta el nodo especificado inmediatamente después del nodo de referencia especificado.
type: docs
weight: 140
url: /es/net/aspose.words/compositenode/insertafter/
---
## CompositeNode.InsertAfter method

Inserta el nodo especificado inmediatamente después del nodo de referencia especificado.

```csharp
public Node InsertAfter(Node newChild, Node refChild)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| newChild | Node | El nodo a insertar. |
| refChild | Node | El nodo que es el nodo de referencia. El newNode se coloca después del refNode. |

### Valor_devuelto

El nodo insertado.

### Observaciones

Si refChild es nulo, inserta newChild al principio de la lista de nodos secundarios.

Si newChild ya está en el árbol, primero se elimina.

Si el nodo que se está insertando se creó a partir de otro documento, debe usar [`ImportNode`](../../documentbase/importnode) para importar el nodo al documento actual. El nodo importado se puede insertar en el documento actual.

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

Muestra cómo agregar, actualizar y eliminar nodos secundarios en la colección de elementos secundarios de CompositeNode.

```csharp
Document doc = new Document();

// Un documento vacío, por defecto, tiene un párrafo.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Los nodos compuestos como nuestro párrafo pueden contener otros nodos compuestos y en línea como elementos secundarios.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Crea tres nodos de ejecución más.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// El cuerpo del documento no mostrará estas ejecuciones hasta que las insertemos en un nodo compuesto
// eso en sí mismo es parte del árbol de nodos del documento, como hicimos con la primera ejecución.
// Podemos determinar donde esta el contenido de texto de los nodos que insertamos
// aparece en el documento especificando una ubicación de inserción relativa a otro nodo en el párrafo.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Inserta la segunda ejecución en el párrafo delante de la ejecución inicial.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Inserta la tercera ejecución después de la ejecución inicial.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Inserta la primera ejecución al comienzo de la colección de nodos secundarios del párrafo.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Podemos modificar el contenido de la ejecución editando y eliminando los nodos secundarios existentes.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Ver también

* class [Node](../../node)
* class [CompositeNode](../../compositenode)
* espacio de nombres [Aspose.Words](../../compositenode)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
