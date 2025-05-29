---
title: Comment.RemoveReply
linktitle: RemoveReply
articleTitle: RemoveReply
second_title: Aspose.Words for .NET
description: 使用 Comment RemoveReply 方法轻松移除不需要的回复，确保您的讨论清晰且相关。立即增强您的评论管理！
type: docs
weight: 180
url: /zh/net/aspose.words/comment/removereply/
---
## Comment.RemoveReply method

删除对此评论的指定回复。

```csharp
public void RemoveReply(Comment reply)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| reply | Comment | 删除回复的评论节点。 |

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
