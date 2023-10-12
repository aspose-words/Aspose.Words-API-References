---
title: Node.CustomNodeId
second_title: Aspose.Words for .NET API 参考
description: Node 财产. 指定自定义节点标识符
type: docs
weight: 10
url: /zh/net/aspose.words/node/customnodeid/
---
## Node.CustomNodeId property

指定自定义节点标识符。

```csharp
public int CustomNodeId { get; set; }
```

### 评论

默认为零。

该标识符可以任意设置和使用。例如，作为获取外部数据的密钥。

重要提示，指定的值不会保存到输出文件中，并且仅在节点生命周期内存在。

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

* class [Node](../)
* 命名空间 [Aspose.Words](../../node/)
* 部件 [Aspose.Words](../../../)


