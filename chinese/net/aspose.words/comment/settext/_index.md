---
title: Comment.SetText
second_title: Aspose.Words for .NET API 参考
description: Comment 方法. 这是一种方便的方法可以轻松设置评论文本
type: docs
weight: 180
url: /zh/net/aspose.words/comment/settext/
---
## Comment.SetText method

这是一种方便的方法，可以轻松设置评论文本。

```csharp
public void SetText(string text)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| text | String | 评论的新文本。 |

### 评论

此方法允许快速设置字符串中的评论文本。该字符串可以包含 段落分隔符，这将相应地在注释中创建文本段落。 如果您想在注释中插入更复杂的元素，例如书签 或表格或应用丰富的格式，那么您需要使用适当的节点类 构建评论文本。

### 例子

演示如何向文档添加评论，然后回复它。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// 将注释放置在文档正文中的节点处。
// 该注释将显示在其段落的位置，
// 页面右侧边距之外，并用虚线将其与其段落连接起来。
builder.CurrentParagraph.AppendChild(comment);

// 添加回复，该回复将显示在其父评论下方。
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// 评论和回复都是Comment节点。
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// 不回复其他评论的评论是“顶级”。他们没有祖先的评论。
Assert.Null(comment.Ancestor);

// 回复有一个祖先顶级评论。
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### 也可以看看

* class [Comment](../)
* 命名空间 [Aspose.Words](../../comment/)
* 部件 [Aspose.Words](../../../)


