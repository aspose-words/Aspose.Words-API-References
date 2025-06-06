---
title: NodeChangingAction Enum
linktitle: NodeChangingAction
articleTitle: NodeChangingAction
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.NodeChangingAction 枚举，高效管理文档中的节点更改。立即提升您的文档处理能力！
type: docs
weight: 4870
url: /zh/net/aspose.words/nodechangingaction/
---
## NodeChangingAction enumeration

指定节点更改的类型。

```csharp
public enum NodeChangingAction
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Insert | `0` | 正在将节点插入树中。 |
| Remove | `1` | 正在从树中删除一个节点。 |

## 例子

展示如何在编辑文档树时使用 NodeChangingCallback 实时监控文档树的变化。

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
/// 打印文档中发生的每个节点插入/删除。
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

### 也可以看看

* class [NodeChangingArgs](../nodechangingargs/)
* property [Action](../nodechangingargs/action/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
