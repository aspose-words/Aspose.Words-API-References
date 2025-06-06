---
title: NodeChangingArgs.Action
linktitle: Action
articleTitle: Action
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aktionseigenschaft NodeChangingArgs, um Knotenänderungsereignisse mühelos zu identifizieren. Steigern Sie Ihre Programmiereffizienz mit dieser wichtigen Funktion!
type: docs
weight: 10
url: /de/net/aspose.words/nodechangingargs/action/
---
## NodeChangingArgs.Action property

Ruft einen Wert ab, der angibt, welche Art von Knotenänderungsereignis auftritt.

```csharp
public NodeChangingAction Action { get; }
```

## Beispiele

Zeigt, wie ein NodeChangingCallback verwendet wird, um Änderungen am Dokumentbaum während der Bearbeitung in Echtzeit zu überwachen.

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
/// Druckt jedes Einfügen/Entfernen von Knoten, während es im Dokument stattfindet.
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

### Siehe auch

* enum [NodeChangingAction](../../nodechangingaction/)
* class [NodeChangingArgs](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
