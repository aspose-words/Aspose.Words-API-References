---
title: Node.IsComposite
second_title: Aspose.Words for .NET API 参考
description: Node 财产. 如果此节点可以包含其他节点则返回 true
type: docs
weight: 30
url: /zh/net/aspose.words/node/iscomposite/
---
## Node.IsComposite property

如果此节点可以包含其他节点，则返回 true。

```csharp
public virtual bool IsComposite { get; }
```

### 适当的价值

此方法返回 false，因为 Node 不能有子节点。

### 例子

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

* class [Node](../)
* 命名空间 [Aspose.Words](../../node/)
* 部件 [Aspose.Words](../../../)


