---
title: Node.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words for .NET
description: 发现 Node 的 NodeType 属性可以轻松识别应用程序中的节点类型，从而提高开发效率和代码清晰度。
type: docs
weight: 50
url: /zh/net/aspose.words/node/nodetype/
---
## Node.NodeType property

获取此节点的类型。

```csharp
public abstract NodeType NodeType { get; }
```

## 例子

演示如何使用节点的 NextSibling 属性来枚举其直属子节点。

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

for (Node node = doc.FirstSection.Body.FirstChild; node != null; node = node.NextSibling)
{
    Console.WriteLine();
    Console.WriteLine($"Node type: {Node.NodeTypeToString(node.NodeType)}");

    string contents = node.GetText().Trim();
    Console.WriteLine(contents == string.Empty ? "This node contains no text" : $"Contents: \"{node.GetText().Trim()}\"");
}
```

展示如何从复合节点中删除特定类型的所有子节点。

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // 将下一个同级节点保存为变量，以便我们删除此节点后移动到该节点。
    Node nextNode = curNode.NextSibling;

    // 一个节体可以包含段落和表格节点。
    // 如果该节点是一个表，则将其从父节点中移除。
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
```

展示如何遍历复合节点的子节点树。

```csharp
public void RecurseChildren()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // 任何可以包含子节点的节点（例如文档本身）都是复合节点。
    Assert.True(doc.IsComposite);

    // 调用递归函数，遍历并打印复合节点的所有子节点。
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// 递归遍历节点树，同时打印每个节点的类型
/// 缩进取决于深度以及所有内联节点的内容。
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // 如果该节点是复合节点，则递归进入该节点。否则，如果该节点是内联节点，则打印其内容。
        if (childNode.IsComposite)
        {
            Console.WriteLine();
            TraverseAllNodes((CompositeNode)childNode, depth + 1);
        }
        else if (childNode is Inline)
        {
            Console.WriteLine($" - \"{childNode.GetText().Trim()}\"");
        }
        else
        {
            Console.WriteLine();
        }
    }
}
```

### 也可以看看

* enum [NodeType](../../nodetype/)
* class [Node](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
