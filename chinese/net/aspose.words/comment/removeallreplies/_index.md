---
title: Comment.RemoveAllReplies
linktitle: RemoveAllReplies
articleTitle: RemoveAllReplies
second_title: Aspose.Words for .NET
description: 使用 RemoveAllReplies 方法轻松清除对您评论的所有回复，确保讨论整洁并增强用户体验。
type: docs
weight: 170
url: /zh/net/aspose.words/comment/removeallreplies/
---
## Comment.RemoveAllReplies method

删除对此评论的所有回复。

```csharp
public void RemoveAllReplies()
```

## 评论

回复的所有组成节点都将从文档中删除。

## 例子

展示如何删除评论回复。

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count); 

// 以下是两种从评论中删除回复的方法。
// 1 - 使用“RemoveReply”方法从评论中单独删除回复：
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count);

// 2 - 使用“RemoveAllReplies”方法一次性删除评论中的所有回复：
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count);
```

### 也可以看看

* class [Comment](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
