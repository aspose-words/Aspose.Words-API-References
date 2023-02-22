---
title: CompositeNode.InsertAfter
second_title: Aspose.Words for .NET API 参考
description: CompositeNode 方法. 在指定参考节点之后立即插入指定节点
type: docs
weight: 140
url: /zh/net/aspose.words/compositenode/insertafter/
---
## CompositeNode.InsertAfter method

在指定参考节点之后立即插入指定节点。

```csharp
public Node InsertAfter(Node newChild, Node refChild)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | Node | 要插入的节点。 |
| refChild | Node | 作为参考节点的节点。 newNode 放在 refNode 之后。 |

### 返回值

插入的节点。

### 评论

如果 refChild 为 null，则在子节点列表的开头插入 newChild。

如果 newChild 已经在树中，则首先将其移除。

如果要插入的节点是从另一个文档创建的，则应使用 [`ImportNode`](../../documentbase/importnode/)将节点导入当前文档。 然后可以将导入的节点插入到当前文档中。

### 例子

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

展示如何在 CompositeNode 的子节点集合中添加、更新和删除子节点。

```csharp
Document doc = new Document();

// 默认情况下，一个空文档有一个段落。
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// 像我们的段落这样的复合节点可以包含其他复合和内联节点作为子节点。
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

//再创建三个运行节点。
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// 文档正文不会显示这些运行，直到我们将它们插入到复合节点中
// 它本身就是文档节点树的一部分，就像我们在第一次运行时所做的那样。
// 我们可以确定我们插入的节点的文本内容在哪里
// 通过指定相对于段落中另一个节点的插入位置出现在文档中。
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// 将第二次运行插入到第一次运行之前的段落中。
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// 在初始运行之后插入第三次运行。
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// 将第一次运行插入段落子节点集合的开头。
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// 我们可以通过编辑删除已有的子节点来修改run的内容。
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### 也可以看看

* class [Node](../../node/)
* class [CompositeNode](../)
* 命名空间 [Aspose.Words](../../compositenode/)
* 部件 [Aspose.Words](../../../)


