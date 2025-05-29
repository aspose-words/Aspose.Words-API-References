---
title: NodeChangingArgs.NewParent
linktitle: NewParent
articleTitle: NewParent
second_title: Aspose.Words för .NET
description: Upptäck egenskapen NodeChangingArgs NewParent för att effektivt komma åt en nods framtida förälder efter att operationerna är klara. Förbättra din kodning med lätthet!
type: docs
weight: 20
url: /sv/net/aspose.words/nodechangingargs/newparent/
---
## NodeChangingArgs.NewParent property

Hämtar nodens förälder som kommer att ställas in efter att operationen är klar.

```csharp
public Node NewParent { get; }
```

## Exempel

Visar hur man använder en NodeChangingCallback för att övervaka ändringar i dokumentträdet i realtid medan vi redigerar det.

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
/// Skriver ut varje nodinsättning/borttagning allt eftersom den sker i dokumentet.
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

### Se även

* class [Node](../../node/)
* class [NodeChangingArgs](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
