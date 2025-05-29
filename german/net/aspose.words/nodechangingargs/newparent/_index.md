---
title: NodeChangingArgs.NewParent
linktitle: NewParent
articleTitle: NewParent
second_title: Aspose.Words für .NET
description: Entdecken Sie die NewParent-Eigenschaft von NodeChangingArgs, um nach Abschluss von Operationen effizient auf den zukünftigen übergeordneten Knoten eines Knotens zuzugreifen. Verbessern Sie Ihren Code mühelos!
type: docs
weight: 20
url: /de/net/aspose.words/nodechangingargs/newparent/
---
## NodeChangingArgs.NewParent property

Ruft das übergeordnete Element des Knotens ab, das nach Abschluss des Vorgangs festgelegt wird.

```csharp
public Node NewParent { get; }
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

* class [Node](../../node/)
* class [NodeChangingArgs](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
