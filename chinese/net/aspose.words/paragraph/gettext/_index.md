---
title: Paragraph.GetText
second_title: Aspose.Words for .NET API 参考
description: Paragraph 方法. 获取该段落的文本包括段落结尾字符
type: docs
weight: 260
url: /zh/net/aspose.words/paragraph/gettext/
---
## Paragraph.GetText method

获取该段落的文本，包括段落结尾字符。

```csharp
public override string GetText()
```

### 评论

连接所有子节点的文本，并附加段落结尾字符，如下所示：

* 如果段落是最后一段[`Body`](../../body/) 那么 [`ControlChar.SectionBreak`](../../controlchar/sectionbreak/) (\x000c) 被附加。
* 如果段落是最后一段[`Cell`](../../../aspose.words.tables/cell/) 那么 [`控制字符单元`](../../controlchar/cell/) (\x0007) 被附加。
* 对于所有其他段落 [`ControlChar.ParagraphBreak`](../../controlchar/paragraphbreak/) (\r) 附加。

返回的字符串包括所有控制和特殊字符，如[`ControlChar`](../../controlchar/).

### 例子

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

* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../paragraph/)
* 部件 [Aspose.Words](../../../)


