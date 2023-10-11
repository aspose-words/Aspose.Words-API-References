---
title: Interface INodeChangingCallback
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.INodeChangingCallback 界面. 如果您希望在文档中插入或删除节点时收到通知请实现此接口
type: docs
weight: 3200
url: /zh/net/aspose.words/inodechangingcallback/
---
## INodeChangingCallback interface

如果您希望在文档中插入或删除节点时收到通知，请实现此接口。

```csharp
public interface INodeChangingCallback
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [NodeInserted](../../aspose.words/inodechangingcallback/nodeinserted/)(NodeChangingArgs) | 当属于此文档的节点已插入到另一个节点时调用。 |
| [NodeInserting](../../aspose.words/inodechangingcallback/nodeinserting/)(NodeChangingArgs) | 在属于该文档的节点即将插入另一个节点之前调用。 |
| [NodeRemoved](../../aspose.words/inodechangingcallback/noderemoved/)(NodeChangingArgs) | 当属于此文档的节点已从其父节点中删除时调用。 |
| [NodeRemoving](../../aspose.words/inodechangingcallback/noderemoving/)(NodeChangingArgs) | 在属于该文档的节点即将从文档中删除之前调用。 |

### 例子

展示如何通过回调自定义节点更改。

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
/// 为运行节点的文本内容设置自定义字体名称/大小。
/// </summary>
public class HandleNodeChangingFontChanger : INodeChangingCallback
{
    void INodeChangingCallback.NodeInserted(NodeChangingArgs args)
    {
        mLog.AppendLine($"\tType:\t{args.Node.NodeType}");
        mLog.AppendLine($"\tHash:\t{args.Node.GetHashCode()}");

        if (args.Node.NodeType == NodeType.Run)
        {
            Aspose.Words.Font font = ((Run) args.Node).Font;
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


