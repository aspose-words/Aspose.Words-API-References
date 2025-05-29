---
title: NodeChangingArgs.Action
linktitle: Action
articleTitle: Action
second_title: .NET için Aspose.Words
description: NodeChangingArgs Action özelliğini keşfederek düğüm değişikliği olaylarını zahmetsizce tanımlayın. Bu temel özellik ile kodlama verimliliğinizi artırın!
type: docs
weight: 10
url: /tr/net/aspose.words/nodechangingargs/action/
---
## NodeChangingArgs.Action property

Hangi tür düğüm değişikliği olayının meydana geldiğini belirten bir değer alır.

```csharp
public NodeChangingAction Action { get; }
```

## Örnekler

Düzenleme yaparken belge ağacındaki değişiklikleri gerçek zamanlı olarak izlemek için NodeChangingCallback'in nasıl kullanılacağını gösterir.

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
/// Belgede gerçekleşen her düğüm ekleme/kaldırma işlemini yazdırır.
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

### Ayrıca bakınız

* enum [NodeChangingAction](../../nodechangingaction/)
* class [NodeChangingArgs](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
