---
title: NodeChangingArgs.Action
linktitle: Action
articleTitle: Action
second_title: Aspose.Words per .NET
description: Scopri la proprietà Action di NodeChangingArgs per identificare facilmente gli eventi di modifica dei nodi. Migliora l'efficienza del tuo codice con questa funzionalità essenziale!
type: docs
weight: 10
url: /it/net/aspose.words/nodechangingargs/action/
---
## NodeChangingArgs.Action property

Ottiene un valore che indica quale tipo di evento di modifica del nodo si sta verificando.

```csharp
public NodeChangingAction Action { get; }
```

## Esempi

Mostra come utilizzare un NodeChangingCallback per monitorare in tempo reale le modifiche apportate all'albero del documento durante la modifica.

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
/// Stampa ogni inserimento/rimozione di nodo non appena avviene nel documento.
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

### Guarda anche

* enum [NodeChangingAction](../../nodechangingaction/)
* class [NodeChangingArgs](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
