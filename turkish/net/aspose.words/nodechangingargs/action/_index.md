---
title: NodeChangingArgs.Action
second_title: Aspose.Words for .NET API Referansı
description: NodeChangingArgs mülk. Ne tür bir düğüm değişikliği olayının meydana geldiğini gösteren bir değer alır.
type: docs
weight: 10
url: /tr/net/aspose.words/nodechangingargs/action/
---
## NodeChangingArgs.Action property

Ne tür bir düğüm değişikliği olayının meydana geldiğini gösteren bir değer alır.

```csharp
public NodeChangingAction Action { get; }
```

### Örnekler

Belge ağacını düzenlerken gerçek zamanlı olarak yapılan değişiklikleri izlemek için NodeChangingCallback'in nasıl kullanılacağını gösterir.

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

    #if NET48 || JAVA
    builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
    #elif NET5_0_OR_GREATER || __MOBILE__
    using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
        builder.InsertImage(image);
    #endif

    builder.CurrentParagraph.ParentNode.RemoveAllChildren();
}

/// <summary>
/// Her düğüm ekleme/çıkarma işlemini belgede gerçekleştiği gibi yazdırır.
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
* ad alanı [Aspose.Words](../../nodechangingargs/)
* toplantı [Aspose.Words](../../../)


