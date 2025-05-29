---
title: CompositeNode.GetChild
linktitle: GetChild
articleTitle: GetChild
second_title: Aspose.Words for .NET
description: 探索 CompositeNode GetChild 方法，轻松检索特定类型的第 N 个子节点，提高数据管理效率。
type: docs
weight: 100
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
| index | Int32 | 要选择的子节点的从零开始的索引。 也允许负索引，表示从末尾访问， 即 -1 表示最后一个节点。 |
| isDeep | Boolean | `真的`递归地从所有子节点中选择； `错误的`仅在直属子级中进行选择。有关更多信息，请参阅备注。 |

### 返回值

符合条件的子节点或`无效的`如果没有找到匹配的节点。

## 评论

如果索引超出范围，则`无效的`被退回。

请注意，标记节点 (StructuredDocumentTag和SmartTag ) 即使在*isDeep*=`错误的`和`GetChild`用于非标记节点类型。例如，如果 para 中的第一个运行被包装在[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)，它仍然会被返回`GetChild`(Run ，0，`错误的`）。

## 例子

展示如何将表格样式的属性直接应用于表格的元素。

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

// 此方法涉及表格样式属性，例如我们上面设置的属性。
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

展示如何遍历复合节点的子节点集合。

```csharp
Document doc = new Document();

// 将两个运行和一个形状作为子节点添加到此文档的第一段。
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

// 遍历段落的直接子段落集合，
// 并打印我们在其中发现的任何运行或形状。
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
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
