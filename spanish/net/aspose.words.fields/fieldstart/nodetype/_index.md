---
title: FieldStart.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldStart NodeType que mejora la gestión de sus datos al devolver FieldStart de manera eficiente para un rendimiento óptimo.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldstart/nodetype/
---
## FieldStart.NodeType property

DevuelveFieldStart .

```csharp
public override NodeType NodeType { get; }
```

## Ejemplos

Muestra cómo recorrer el árbol de nodos secundarios de un nodo compuesto.

```csharp
public void RecurseChildren()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Cualquier nodo que pueda contener nodos secundarios, como el propio documento, es compuesto.
    Assert.True(doc.IsComposite);

    // Invoca la función recursiva que recorrerá e imprimirá todos los nodos secundarios de un nodo compuesto.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Recorre recursivamente un árbol de nodos mientras imprime el tipo de cada nodo
/// con una sangría dependiendo de la profundidad así como del contenido de todos los nodos en línea.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Recurse al nodo si es compuesto. De lo contrario, imprima su contenido si es un nodo en línea.
        if (childNode.IsComposite)
        {
            Console.WriteLine();
            TraverseAllNodes((CompositeNode)childNode, depth + 1);
        }
        else if (childNode is Inline)
        {
            Console.WriteLine($" - \"{childNode.GetText().Trim()}\"");
        }
        else
        {
            Console.WriteLine();
        }
    }
}
```

### Ver también

* enum [NodeType](../../../aspose.words/nodetype/)
* class [FieldStart](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
