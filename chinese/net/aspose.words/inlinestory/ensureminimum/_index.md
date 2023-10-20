---
title: InlineStory.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: 用于 .NET 的 Aspose.Words
description: InlineStory EnsureMinimum 方法. 如果最后一个子级不是段落则创建并附加一个空段落 在 C#.
type: docs
weight: 120
url: /zh/net/aspose.words/inlinestory/ensureminimum/
---
## InlineStory.EnsureMinimum method

如果最后一个子级不是段落，则创建并附加一个空段落。

```csharp
public void EnsureMinimum()
```

## 例子

演示如何插入 InlineStory 节点。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, null);

// 表节点有一个“EnsureMinimum()”方法，可确保表至少有一个单元格。
Table table = new Table(doc);
table.EnsureMinimum();

// 我们可以将表格放在脚注内，这将使其出现在引用页面的页脚处。
Assert.That(footnote.Tables, Is.Empty);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// InlineStory 也有一个“EnsureMinimum()”方法，但在本例中，
// 它确保节点的最后一个子节点是一个段落，
// 让我们能够在 Microsoft Word 中轻松单击并编写文本。
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// 编辑锚点的外观，即小上标数字
// 在正文中指向脚注。
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// 所有内联故事节点都有各自的故事类型。
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

// 评论是另一种类型的内联故事。
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// 内联故事节点的父段落将是主文档正文中的段落。
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// 然而，最后一段是评论文本内容中的一段，
// 这将位于主文档正文之外的对话气泡中。
// 默认情况下，注释不会有任何子节点，
// 因此我们也可以应用 EnsureMinimum() 方法在此处放置一个段落。
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

// 一旦我们有了一个段落，我们就可以移动构建器来完成它并写下我们的评论。
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.AreEqual(StoryType.Comments, comment.StoryType);

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### 也可以看看

* class [InlineStory](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
