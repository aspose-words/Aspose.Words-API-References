---
title: Enum NodeChangingAction
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.NodeChangingAction تعداد. يحدد نوع تغيير العقدة.
type: docs
weight: 3940
url: /ar/net/aspose.words/nodechangingaction/
---
## NodeChangingAction enumeration

يحدد نوع تغيير العقدة.

```csharp
public enum NodeChangingAction
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Insert | `0` | يتم إدخال عقدة في الشجرة . |
| Remove | `1` | تتم إزالة عقدة من الشجرة . |

### أمثلة

يوضح كيفية استخدام NodeChangingCallback لمراقبة التغييرات في شجرة المستند في الوقت الفعلي أثناء تحريرها.

```csharp
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
/// يطبع كل إدخال / إزالة عقدة كما يحدث في المستند.
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

* class [NodeChangingArgs](../nodechangingargs/)
* property [Action](../nodechangingargs/action/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


