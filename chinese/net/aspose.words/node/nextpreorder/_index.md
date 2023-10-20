---
title: Node.NextPreOrder
linktitle: NextPreOrder
articleTitle: NextPreOrder
second_title: 用于 .NET 的 Aspose.Words
description: Node NextPreOrder 方法. 根据前序树遍历算法获取下一个节点 在 C#.
type: docs
weight: 130
url: /zh/net/aspose.words/node/nextpreorder/
---
## Node.NextPreOrder method

根据前序树遍历算法获取下一个节点。

```csharp
public Node NextPreOrder(Node rootNode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| rootNode | Node | 遍历的顶部节点（极限）。 |

### 返回值

预购订单中的下一个节点。如果到达 rootNode，则为 Null。

## 例子

展示如何使用前序遍历算法遍历文档的节点树，并使用图像删除任何遇到的形状。

```csharp
Document doc = new Document(MyDir + "Images.docx");

Assert.AreEqual(9, 
    doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().Count(s => s.HasImage));

Node curNode = doc;
while (curNode != null)
{
    Node nextNode = curNode.NextPreOrder(doc);

    if (curNode.PreviousPreOrder(doc) != null && nextNode != null)
        Assert.AreEqual(curNode, nextNode.PreviousPreOrder(doc));

    if (curNode.NodeType == NodeType.Shape && ((Shape)curNode).HasImage)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0,
    doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().Count(s => s.HasImage));
```

### 也可以看看

* class [Node](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
