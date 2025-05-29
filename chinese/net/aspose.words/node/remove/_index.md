---
title: Node.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: 发现 Node Remove 方法可以轻松地将节点与其父节点分离，从而提高代码的效率和结构。
type: docs
weight: 150
url: /zh/net/aspose.words/node/remove/
---
## Node.Remove method

将自身从父级中移除。

```csharp
public void Remove()
```

## 例子

展示如何从文档中删除所有带有图像的形状。

```csharp
Document doc = new Document(MyDir + "Images.docx");
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.OfType<Shape>().Count(s => s.HasImage));

foreach (Shape shape in shapes.OfType<Shape>())
    if (shape.HasImage) 
        shape.Remove();

Assert.AreEqual(0, shapes.OfType<Shape>().Count(s => s.HasImage));
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

### 也可以看看

* class [Node](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
