---
title: CompositeNode.GetChild
linktitle: GetChild
articleTitle: GetChild
second_title: 用于 .NET 的 Aspose.Words
description: CompositeNode GetChild 方法. 返回与指定类型匹配的第 N 个子节点 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words/compositenode/getchild/
---
## CompositeNode.GetChild method

返回与指定类型匹配的第 N 个子节点。

```csharp
public Node GetChild(NodeType nodeType, int index, bool isDeep)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| nodeType | NodeType | 指定子节点的类型。 |
| index | Int32 | 要选择的子节点的从零开始的索引。 也允许负索引并指示从末尾访问， 即 -1 表示最后一个节点。 |
| isDeep | Boolean | True 以递归方式从所有子节点中选择。 False 仅在直接子节点中选择。有关更多信息，请参阅备注。 |

### 返回值

匹配条件的子节点，如果没有找到匹配的节点，则返回 null。

## 评论

如果 index 超出范围，则返回 null。

请注意，标记节点 (StructuredDocumentTag和SmartTag) 即使在 isDeep = false 并且为非标记节点类型调用 GetChild 时也会被遍历。例如，如果 para 中的第一次运行包装在 StructuredDocumentTag 中，它仍将由 GetChild(NodeType.Run, 0, false) 返回。

## 例子

演示如何将表格样式的属性直接应用于表格元素。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.RowStripe = 3;
tableStyle.CellSpacing = 5;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;

table.Style = tableStyle;

// 此方法涉及表格样式属性，例如我们上面设置的那些。
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

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
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
