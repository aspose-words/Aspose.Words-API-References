---
title: NodeChangingArgs.NewParent
linktitle: NewParent
articleTitle: NewParent
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية NodeChangingArgs NewParent للوصول بكفاءة إلى الأصل المستقبلي للعقدة بعد اكتمال العمليات. حسّن مهاراتك البرمجية بسهولة!
type: docs
weight: 20
url: /ar/net/aspose.words/nodechangingargs/newparent/
---
## NodeChangingArgs.NewParent property

يحصل على العقدة الأصلية التي سيتم تعيينها بعد اكتمال العملية.

```csharp
public Node NewParent { get; }
```

## أمثلة

يوضح كيفية استخدام NodeChangingCallback لمراقبة التغييرات في شجرة المستند في الوقت الفعلي أثناء تحريرها.

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
/// يطبع كل عملية إدخال/إزالة للعقدة أثناء حدوثها في المستند.
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

### أنظر أيضا

* class [Node](../../node/)
* class [NodeChangingArgs](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
