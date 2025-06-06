---
title: NodeChangingArgs Class
linktitle: NodeChangingArgs
articleTitle: NodeChangingArgs
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.NodeChangingArgs 类，它旨在通过无缝集成 INodeChangingCallback 来增强您的文档处理能力。立即提升您的工作流程！
type: docs
weight: 4880
url: /zh/net/aspose.words/nodechangingargs/
---
## NodeChangingArgs class

为[`INodeChangingCallback`](../inodechangingcallback/)接口.

要了解更多信息，请访问[Aspose.Words 文档对象模型（DOM）](https://docs.aspose.com/words/net/aspose-words-document-object-model/)文档文章。

```csharp
public class NodeChangingArgs
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Action](../../aspose.words/nodechangingargs/action/) { get; } | 获取一个值，指示正在发生的节点变化事件的类型。 |
| [NewParent](../../aspose.words/nodechangingargs/newparent/) { get; } | 获取操作完成后将设置的节点的父节点。 |
| [Node](../../aspose.words/nodechangingargs/node/) { get; } | 获取[`Node`](./node/)正在添加或删除。 |
| [OldParent](../../aspose.words/nodechangingargs/oldparent/) { get; } | 在操作开始之前获取节点的父节点。 |

## 例子

展示如何使用回调自定义节点变化。

```csharp
public void FontChangeViaCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 将节点更改回调设置为自定义实现，
    // 然后添加/删除节点以使其生成日志。
    HandleNodeChangingFontChanger callback = new HandleNodeChangingFontChanger();
    doc.NodeChangingCallback = callback;

    builder.Writeln("Hello world!");
    builder.Writeln("Hello again!");
    builder.InsertField(" HYPERLINK \"https://www.google.com/\" ");
    builder.InsertShape(ShapeType.Rectangle, 300, 300);

    doc.Range.Fields[0].Remove();

    Console.WriteLine(callback.GetLog());
}

/// <summary>
/// 记录每个节点插入和删除的日期和时间。
/// 为 Run 节点的文本内容设置自定义字体名称/大小。
/// </summary>
public class HandleNodeChangingFontChanger : INodeChangingCallback
{
    void INodeChangingCallback.NodeInserted(NodeChangingArgs args)
    {
        mLog.AppendLine($"\tType:\t{args.Node.NodeType}");
        mLog.AppendLine($"\tHash:\t{args.Node.GetHashCode()}");

        if (args.Node.NodeType == NodeType.Run)
        {
            Aspose.Words.Font font = ((Run)args.Node).Font;
            mLog.Append($"\tFont:\tChanged from \"{font.Name}\" {font.Size}pt");

            font.Size = 24;
            font.Name = "Arial";

            mLog.AppendLine($" to \"{font.Name}\" {font.Size}pt");
            mLog.AppendLine($"\tContents:\n\t\t\"{args.Node.GetText()}\"");
        }
    }

    void INodeChangingCallback.NodeInserting(NodeChangingArgs args)
    {
        mLog.AppendLine($"\n{DateTime.Now:dd/MM/yyyy HH:mm:ss:fff}\tNode insertion:");
    }

    void INodeChangingCallback.NodeRemoved(NodeChangingArgs args)
    {
        mLog.AppendLine($"\tType:\t{args.Node.NodeType}");
        mLog.AppendLine($"\tHash code:\t{args.Node.GetHashCode()}");
    }

    void INodeChangingCallback.NodeRemoving(NodeChangingArgs args)
    {
        mLog.AppendLine($"\n{DateTime.Now:dd/MM/yyyy HH:mm:ss:fff}\tNode removal:");
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
