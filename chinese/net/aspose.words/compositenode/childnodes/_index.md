---
title: CompositeNode.ChildNodes
second_title: Aspose.Words for .NET API 参考
description: CompositeNode 财产. 获取该节点的所有直接子节点
type: docs
weight: 10
url: /zh/net/aspose.words/compositenode/childnodes/
---
## CompositeNode.ChildNodes property

获取该节点的所有直接子节点。

```csharp
public NodeCollection ChildNodes { get; }
```

### 评论

笔记，`ChildNodes`相当于调用`GetChildNodes(NodeType.Any, false)` 并在每次访问时创建并返回一个新集合。

如果没有子节点，则此属性返回一个空集合。

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

* class [NodeCollection](../../nodecollection/)
* class [CompositeNode](../)
* 命名空间 [Aspose.Words](../../compositenode/)
* 部件 [Aspose.Words](../../../)


