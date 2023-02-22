---
title: CompositeNode.GetEnumerator
second_title: Aspose.Words for .NET API 参考
description: CompositeNode 方法. 为在该节点的子节点上的每个样式迭代提供支持
type: docs
weight: 110
url: /zh/net/aspose.words/compositenode/getenumerator/
---
## CompositeNode.GetEnumerator method

为在该节点的子节点上的每个样式迭代提供支持。

```csharp
public IEnumerator<Node> GetEnumerator()
```

### 例子

显示如何遍历复合节点的子节点集合。

```csharp
Document doc = new Document();

// 将两个运行和一个形状作为子节点添加到该文档的第一段。
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// 请注意，'CustomNodeId' 不会保存到输出文件中，并且仅在节点生命周期内存在。
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// 遍历段落的直接子元素集合，
// 并打印我们在其中找到的任何运行或形状。
NodeCollection children = paragraph.ChildNodes;

Assert.AreEqual(3, paragraph.ChildNodes.Count);

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
    }
```

### 也可以看看

* class [Node](../../node/)
* class [CompositeNode](../)
* 命名空间 [Aspose.Words](../../compositenode/)
* 部件 [Aspose.Words](../../../)


