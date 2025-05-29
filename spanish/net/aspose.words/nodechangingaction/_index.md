---
title: NodeChangingAction Enum
linktitle: NodeChangingAction
articleTitle: NodeChangingAction
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.NodeChangingAction para gestionar eficientemente los cambios de nodos en sus documentos. ¡Mejore sus capacidades de procesamiento de documentos hoy mismo!
type: docs
weight: 4870
url: /es/net/aspose.words/nodechangingaction/
---
## NodeChangingAction enumeration

Especifica el tipo de cambio de nodo.

```csharp
public enum NodeChangingAction
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Insert | `0` | Se está insertando un nodo en el árbol. |
| Remove | `1` | Se está eliminando un nodo del árbol. |

## Ejemplos

Muestra cómo utilizar un NodeChangingCallback para monitorear los cambios en el árbol del documento en tiempo real mientras lo editamos.

```csharp
public void NodeChangingCallback()
{
    Document doc = new Document();
    doc.NodeChangingCallback = new NodeChangingPrinter();

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world!");
    builder.StartTable();
    builder.InsertCell();
    builder.Write("Cell 1");
    builder.InsertCell();
    builder.Write("Cell 2");
    builder.EndTable();

    builder.InsertImage(ImageDir + "Logo.jpg");

    builder.CurrentParagraph.ParentNode.RemoveAllChildren();
}

/// <summary>
/// Imprime cada inserción/eliminación de nodos a medida que tiene lugar en el documento.
/// </summary>
private class NodeChangingPrinter : INodeChangingCallback
{
    void INodeChangingCallback.NodeInserting(NodeChangingArgs args)
    {
        Assert.AreEqual(NodeChangingAction.Insert, args.Action);
        Assert.AreEqual(null, args.OldParent);
    }

    void INodeChangingCallback.NodeInserted(NodeChangingArgs args)
    {
        Assert.AreEqual(NodeChangingAction.Insert, args.Action);
        Assert.NotNull(args.NewParent);

        Console.WriteLine("Inserted node:");
        Console.WriteLine($"\tType:\t{args.Node.NodeType}");

        if (args.Node.GetText().Trim() != "")
        {
            Console.WriteLine($"\tText:\t\"{args.Node.GetText().Trim()}\"");
        }

        Console.WriteLine($"\tHash:\t{args.Node.GetHashCode()}");
        Console.WriteLine($"\tParent:\t{args.NewParent.NodeType} ({args.NewParent.GetHashCode()})");
    }

    void INodeChangingCallback.NodeRemoving(NodeChangingArgs args)
    {
        Assert.AreEqual(NodeChangingAction.Remove, args.Action);
    }

    void INodeChangingCallback.NodeRemoved(NodeChangingArgs args)
    {
        Assert.AreEqual(NodeChangingAction.Remove, args.Action);
        Assert.Null(args.NewParent);

        Console.WriteLine($"Removed node: {args.Node.NodeType} ({args.Node.GetHashCode()})");
    }
}
```

### Ver también

* class [NodeChangingArgs](../nodechangingargs/)
* property [Action](../nodechangingargs/action/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
