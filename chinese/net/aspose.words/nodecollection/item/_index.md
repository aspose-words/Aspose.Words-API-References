---
title: NodeCollection.Item
second_title: Aspose.Words for .NET API 参考
description: NodeCollection 财产. 检索给定索引处的节点
type: docs
weight: 20
url: /zh/net/aspose.words/nodecollection/item/
---
## NodeCollection indexer

检索给定索引处的节点。

```csharp
public Node this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 节点集合的索引。 |

### 评论

该索引是从零开始的。

允许使用负索引，并指示从集合的后面进行访问。 例如 -1 表示最后一项，-2 表示最后一项，依此类推。

如果索引大于或等于列表中的项目数，则返回空引用。

如果索引为负并且其绝对值大于列表中的项目数，则返回空引用。

### 例子

演示如何遍历复合节点的子节点集合。

```csharp
Document doc = new Document();

// 将两个运行和一个形状作为子节点添加到本文档的第一段。
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// 请注意，“CustomNodeId”不会保存到输出文件中，并且仅在节点生命周期内存在。
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// 遍历该段落的直接子级集合，
// 并打印我们在其中找到的任何运行或形状。
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
    }
```

### 也可以看看

* class [Node](../../node/)
* class [NodeCollection](../)
* 命名空间 [Aspose.Words](../../nodecollection/)
* 部件 [Aspose.Words](../../../)


