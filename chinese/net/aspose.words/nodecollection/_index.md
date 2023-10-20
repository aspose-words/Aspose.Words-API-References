---
title: NodeCollection Class
linktitle: NodeCollection
articleTitle: NodeCollection
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.NodeCollection 班级. 表示特定类型的节点集合 在 C#.
type: docs
weight: 4200
url: /zh/net/aspose.words/nodecollection/
---
## NodeCollection class

表示特定类型的节点集合。

要了解更多信息，请访问[Aspose.Words 文档对象模型 (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/)文档文章。

```csharp
public class NodeCollection : IEnumerable<Node>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | 获取集合中的节点数。 |
| [Item](../../aspose.words/nodecollection/item/) { get; } | 检索给定索引处的节点。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | 将节点添加到集合的末尾。 |
| [Clear](../../aspose.words/nodecollection/clear/)() | 从此集合和文档中删除所有节点。 |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | 确定节点是否在集合中。 |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | 在节点集合上提供简单的“foreach”样式迭代。 |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | 返回指定节点的从零开始的索引。 |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | 将节点插入集合中指定索引处。 |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | 从集合和文档中删除节点。 |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | 从集合和文档中删除指定索引处的节点。 |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | 将集合中的所有节点复制到新的节点数组。 |

## 评论

`NodeCollection`不拥有它包含的节点，而是只是指定类型的节点 的选择，但节点存储在树中各自的父节点下。

`NodeCollection`支持索引访问、迭代并提供添加和删除方法。

这`NodeCollection`集合是“实时”的，即对创建它的节点 object 的子节点所做的更改会立即反映在由`NodeCollection` 属性和方法。

`NodeCollection`由返回[`GetChildNodes`](../compositenode/getchildnodes/) 并且还用作类型化节点集合的基类，例如[`SectionCollection`](../sectioncollection/), [`ParagraphCollection`](../paragraphcollection/) ETC。

`NodeCollection`可以是“扁平”的并且仅包含其创建的节点 的直接子节点，也可以是“深”的并且包含所有后代子节点。

## 例子

演示如何用图像形状替换所有文本框形状。

```csharp
Document doc = new Document(MyDir + "Textboxes in drawing canvas.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(3, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(1, shapes.Count(s => s.ShapeType == ShapeType.Image));

foreach (Shape shape in shapes)
{
    if (shape.ShapeType == ShapeType.TextBox)
    {
        Shape replacementShape = new Shape(doc, ShapeType.Image);
        replacementShape.ImageData.SetImage(ImageDir + "Logo.jpg");
        replacementShape.Left = shape.Left;
        replacementShape.Top = shape.Top;
        replacementShape.Width = shape.Width;
        replacementShape.Height = shape.Height;
        replacementShape.RelativeHorizontalPosition = shape.RelativeHorizontalPosition;
        replacementShape.RelativeVerticalPosition = shape.RelativeVerticalPosition;
        replacementShape.HorizontalAlignment = shape.HorizontalAlignment;
        replacementShape.VerticalAlignment = shape.VerticalAlignment;
        replacementShape.WrapType = shape.WrapType;
        replacementShape.WrapSide = shape.WrapSide;

        shape.ParentNode.InsertAfter(replacementShape, shape);
        shape.Remove();
    }
}

shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(0, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(4, shapes.Count(s => s.ShapeType == ShapeType.Image));

doc.Save(ArtifactsDir + "Shape.ReplaceTextboxesWithImages.docx");
```

### 也可以看看

* class [Node](../node/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
