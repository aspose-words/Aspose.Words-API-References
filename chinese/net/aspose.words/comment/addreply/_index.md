---
title: Comment.AddReply
linktitle: AddReply
articleTitle: AddReply
second_title: 用于 .NET 的 Aspose.Words
description: Comment AddReply 方法. 添加对此评论的回复 在 C#.
type: docs
weight: 120
url: /zh/net/aspose.words/comment/addreply/
---
## Comment.AddReply method

添加对此评论的回复。

```csharp
public Comment AddReply(string author, string initial, DateTime dateTime, string text)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| author | String | 回复的作者姓名。 |
| initial | String | 回复的作者姓名缩写。 |
| dateTime | DateTime | 回复的日期和时间。 |
| text | String | 回复文本。 |

### 返回值

所创建的[`Comment`](../)用于回复的节点。

## 评论

由于现有的 MS Office 限制，文档中仅允许 1 级回复。 类型例外InvalidOperationException如果在现有回复评论上 调用此方法，则会引发该问题。

## 例子

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
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
