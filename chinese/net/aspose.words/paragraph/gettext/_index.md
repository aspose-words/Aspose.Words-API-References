---
title: Paragraph.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words for .NET
description: 发现 Paragraph GetText 方法可以轻松检索文本（包括段落结尾），从而提高文本处理效率。
type: docs
weight: 280
url: /zh/net/aspose.words/paragraph/gettext/
---
## Paragraph.GetText method

获取此段落的文本（包括段落结束字符）。

```csharp
public override string GetText()
```

## 评论

所有子节点的文本被连接起来，并附加段落结束字符，如下所示：

* 如果该段落是[`Body`](../../body/)，然后 [`SectionBreak`](../../controlchar/sectionbreak/) （\x000c）被附加。
* 如果该段落是[`Cell`](../../../aspose.words.tables/cell/)，然后 [`Cell`](../../controlchar/cell/) （\x0007）被附加。
* 对于所有其他段落 [`ParagraphBreak`](../../controlchar/paragraphbreak/) （\r）被附加。

返回的字符串包括所有控制字符和特殊字符，如中所述[`ControlChar`](../../controlchar/)。

## 例子

展示如何在 CompositeNode 的子节点集合中添加、更新和删除子节点。

```csharp
Document doc = new Document();

// 默认情况下，空文档有一个段落。
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// 复合节点（例如我们的段落）可以包含其他复合节点和内联节点作为子节点。
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// 再创建三个运行节点。
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// 在我们将它们插入到复合节点之前，文档主体不会显示这些运行
// 它本身是文档节点树的一部分，就像我们第一次运行一样。
// 我们可以确定插入节点的文本内容
// 通过指定相对于段落中另一个节点的插入位置出现在文档中。
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// 将第二个运行插入到第一个运行前面的段落中。
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// 在初次运行后插入第三次运行。
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// 将第一个运行插入到段落子节点集合的开头。
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

* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
