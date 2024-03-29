---
title: CompositeNode.ChildNodes
second_title: Referencia de API de Aspose.Words para .NET
description: CompositeNode propiedad. Obtiene todos los nodos secundarios inmediatos de este nodo.
type: docs
weight: 10
url: /es/net/aspose.words/compositenode/childnodes/
---
## CompositeNode.ChildNodes property

Obtiene todos los nodos secundarios inmediatos de este nodo.

```csharp
public NodeCollection ChildNodes { get; }
```

### Observaciones

Nota,`ChildNodes` es equivalente a llamar`GetChildNodes(NodeType.Any, false)` y crea y devuelve una nueva colección cada vez que se accede a ella.

Si no hay nodos secundarios, esta propiedad devuelve una colección vacía.

### Ejemplos

Muestra cómo recorrer la colección de nodos secundarios de un nodo compuesto.

```csharp
Document doc = new Document();

// Agregue dos carreras y una forma como nodos secundarios al primer párrafo de este documento.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Tenga en cuenta que el 'CustomNodeId' no se guarda en un archivo de salida y existe solo durante la vida útil del nodo.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Iterar a través de la colección de elementos secundarios inmediatos del párrafo,
// e imprima cualquier ejecución o forma que encontremos dentro.
NodeCollection children = paragraph.ChildNodes;

Assert.AreEqual(3, paragraph.ChildNodes.Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
    }
```

### Ver también

* class [NodeCollection](../../nodecollection/)
* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../compositenode/)
* asamblea [Aspose.Words](../../../)


