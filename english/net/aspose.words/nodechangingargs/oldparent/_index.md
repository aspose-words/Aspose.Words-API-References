---
title: NodeChangingArgs.OldParent
linktitle: OldParent
articleTitle: OldParent
second_title: Aspose.Words for .NET
description: Discover the NodeChangingArgs OldParent property, which retrieves the parent node prior to changes, ensuring seamless operations and enhanced data management.
type: docs
weight: 40
url: /net/aspose.words/nodechangingargs/oldparent/
---
## NodeChangingArgs.OldParent property

Gets the node's parent before the operation began.

```csharp
public Node OldParent { get; }
```

## Examples

Shows how to use a NodeChangingCallback to monitor changes to the document tree in real-time as we edit it.

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
/// Prints every node insertion/removal as it takes place in the document.
/// </summary>
private class NodeChangingPrinter : INodeChangingCallback
{
    void INodeChangingCallback.NodeInserting(NodeChangingArgs args)
    {
        Assert.That(args.Action, Is.EqualTo(NodeChangingAction.Insert));
        Assert.That(args.OldParent, Is.EqualTo(null));
    }

    void INodeChangingCallback.NodeInserted(NodeChangingArgs args)
    {
        Assert.That(args.Action, Is.EqualTo(NodeChangingAction.Insert));
        Assert.That(args.NewParent, Is.Not.Null);

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
        Assert.That(args.Action, Is.EqualTo(NodeChangingAction.Remove));
    }

    void INodeChangingCallback.NodeRemoved(NodeChangingArgs args)
    {
        Assert.That(args.Action, Is.EqualTo(NodeChangingAction.Remove));
        Assert.That(args.NewParent, Is.Null);

        Console.WriteLine($"Removed node: {args.Node.NodeType} ({args.Node.GetHashCode()})");
    }
}
```

### See Also

* class [Node](../../node/)
* class [NodeChangingArgs](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
