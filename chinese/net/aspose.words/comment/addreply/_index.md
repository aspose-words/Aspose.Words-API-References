---
title: Comment.AddReply
linktitle: AddReply
articleTitle: AddReply
second_title: Aspose.Words for .NET
description: 使用 Comment AddReply 方法增强您的讨论 - 轻松添加对评论的回复并提高您平台上的参与度！
type: docs
weight: 160
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
| initial | String | 作者在回复中签上姓名首字母。 |
| dateTime | DateTime | 回复的日期和时间。 |
| text | String | 回复文本。 |

### 返回值

所创造的[`Comment`](../)节点进行回复。

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| InvalidOperationException | 如果在现有的回复评论上调用此方法，则抛出。 |

## 评论

由于现有的 MS Office 限制，文档中仅允许 1 级回复。

## 例子

展示如何向文档添加评论，然后对其进行回复。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// 将注释放置在文档正文中的某个节点处。
// 此评论将显示在其段落的位置，
// 位于页面右侧边距之外，并用虚线将其与段落连接起来。
builder.CurrentParagraph.AppendChild(comment);

// 添加回复，它将显示在其父评论下。
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// 评论和回复都是评论节点。
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// 不回复其他评论的评论是“顶级”评论。它们没有祖先评论。
Assert.Null(comment.Ancestor);

// 回复有一个祖先顶级评论。
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### 也可以看看

* class [Comment](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
