---
title: NodeChangingArgs.OldParent
linktitle: OldParent
articleTitle: OldParent
second_title: Aspose.Words per .NET
description: Scopri la proprietà OldParent di NodeChangingArgs, che recupera il nodo padre prima delle modifiche, garantendo operazioni fluide e una gestione dei dati migliorata.
type: docs
weight: 40
url: /it/net/aspose.words/nodechangingargs/oldparent/
---
## NodeChangingArgs.OldParent property

Ottiene il nodo padre prima dell'inizio dell'operazione.

```csharp
public Node OldParent { get; }
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

* class [Node](../../node/)
* class [NodeChangingArgs](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
