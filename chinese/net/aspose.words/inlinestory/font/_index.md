---
title: InlineStory.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words for .NET
description: 探索 InlineStory 字体属性，实现锚字符的无缝字体格式，并通过独特的排版选项增强您的设计。
type: docs
weight: 20
url: /zh/net/aspose.words/inlinestory/font/
---
## InlineStory.Font property

提供对此对象的锚字符的字体格式的访问。

```csharp
public Font Font { get; }
```

## 例子

展示如何插入 InlineStory 节点。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, null);

// 表格节点有一个“EnsureMinimum()”方法，用于确保表格至少有一个单元格。
Table table = new Table(doc);
table.EnsureMinimum();

// 我们可以在脚注中放置一个表格，这将使其出现在引用页面的页脚中。
Assert.AreEqual(0, footnote.Tables.Count);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// InlineStory 也有一个“EnsureMinimum()”方法，但在这种情况下，
// 它确保节点的最后一个子节点是一个段落，
// 让我们能够在 Microsoft Word 中轻松单击并编写文本。
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// 编辑锚点的外观，即小上标数字
// 在指向脚注的正文中。
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// 所有内联故事节点都有各自的故事类型。
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

// 评论是另一种类型的内联故事。
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// 内联故事节点的父段落将是主文档主体中的段落。
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// 但是，最后一段是来自评论文本内容的一段，
// 它将位于文档主体外部的对话气泡中。
// 默认情况下，评论不会有任何子节点，
// 因此我们也可以应用 EnsureMinimum() 方法在这里放置一个段落。
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

// 一旦我们有了段落，我们就可以移动构建器来执行它并写下我们的评论。
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.AreEqual(StoryType.Comments, comment.StoryType);

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### 也可以看看

* class [Font](../../font/)
* class [InlineStory](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
