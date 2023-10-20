---
title: Shape.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: 用于 .NET 的 Aspose.Words
description: Shape NodeType 财产. 返回Shape 在 C#.
type: docs
weight: 130
url: /zh/net/aspose.words.drawing/shape/nodetype/
---
## Shape.NodeType property

返回Shape.

```csharp
public override NodeType NodeType { get; }
```

## 例子

显示如何遍历复合节点的子节点树。

```csharp
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // 任何可以包含子节点的节点，例如文档本身，都是复合的。
    Assert.True(doc.IsComposite);

    // 调用将遍历并打印复合节点的所有子节点的递归函数。
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// 递归遍历一个节点树，同时打印每个节点的类型
/// 缩进取决于深度以及所有内联节点的内容。
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // 如果是复合节点，则递归到该节点。否则，如果它是内联节点，则打印其内容。
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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [Shape](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
