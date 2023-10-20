---
title: CompositeNode.InsertBefore
linktitle: InsertBefore
articleTitle: InsertBefore
second_title: 用于 .NET 的 Aspose.Words
description: CompositeNode InsertBefore 方法. 在指定的引用节点之前插入指定的节点 在 C#.
type: docs
weight: 140
url: /zh/net/aspose.words/compositenode/insertbefore/
---
## CompositeNode.InsertBefore method

在指定的引用节点之前插入指定的节点。

```csharp
public Node InsertBefore(Node newChild, Node refChild)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | Node | 这[`Node`](../../node/)插入。 |
| refChild | Node | 这[`Node`](../../node/)那是参考节点。这*newChild*放置在该节点之前。 |

### 返回值

插入的节点。

## 评论

如果*refChild*是`无效的` , 插入*newChild*位于子节点列表的末尾。

如果*newChild*已经在树中，首先将其删除。

如果插入的节点是从另一个文档创建的，则应使用 [`ImportNode`](../../documentbase/importnode/)将节点导入到当前文档。 然后可以将导入的节点插入到当前文档中。

## 例子

演示如何在 CompositeNode 的子节点集合中添加、更新和删除子节点。

```csharp
Document doc = new Document();

// 默认情况下，一个空文档只有一个段落。
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// 复合节点（例如我们的段落）可以包含其他复合节点和内联节点作为子节点。
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// 再创建三个运行节点。
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// 文档主体不会显示这些运行，直到我们将它们插入到复合节点中
// 它本身是文档节点树的一部分，就像我们在第一次运行时所做的那样。
// 我们可以确定我们插入的节点的文本内容在哪里
// 通过指定相对于段落中另一个节点的插入位置来出现在文档中。
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// 将第二个运行插入到第一个运行前面的段落中。
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// 在初始运行之后插入第三次运行。
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// 将第一行插入到段落子节点集合的开头。
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// 我们可以通过编辑和删除现有的子节点来修改运行的内容。
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### 也可以看看

* class [Node](../../node/)
* class [CompositeNode](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
