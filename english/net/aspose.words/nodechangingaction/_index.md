---
title: NodeChangingAction Enum
linktitle: NodeChangingAction
articleTitle: NodeChangingAction
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.NodeChangingAction enum to efficiently manage node changes in your documents. Enhance your document processing capabilities today!
type: docs
weight: 4900
url: /net/aspose.words/nodechangingaction/
---
## NodeChangingAction enumeration

Specifies the type of node change.

```csharp
public enum NodeChangingAction
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Insert | `0` | A node is being inserted in the tree. |
| Remove | `1` | A node is being removed from the tree. |

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

* class [NodeChangingArgs](../nodechangingargs/)
* property [Action](../nodechangingargs/action/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
