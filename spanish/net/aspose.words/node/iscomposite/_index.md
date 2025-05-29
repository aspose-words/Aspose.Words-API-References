---
title: Node.IsComposite
linktitle: IsComposite
articleTitle: IsComposite
second_title: Aspose.Words para .NET
description: Descubra la propiedad "Node IsComposite". Identifique fácilmente si un nodo puede albergar otros nodos, mejorando así la gestión y la flexibilidad de su estructura de datos.
type: docs
weight: 30
url: /es/net/aspose.words/node/iscomposite/
---
## Node.IsComposite property

Devuelve`verdadero` si este nodo puede contener otros nodos.

```csharp
public virtual bool IsComposite { get; }
```

### El valor de la propiedad

Este método retorna`FALSO` como[`Node`](../) no puede tener nodos secundarios.

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

* class [Node](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
