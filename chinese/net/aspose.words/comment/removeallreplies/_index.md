---
title: Comment.RemoveAllReplies
linktitle: RemoveAllReplies
articleTitle: RemoveAllReplies
second_title: 用于 .NET 的 Aspose.Words
description: Comment RemoveAllReplies 方法. 删除对此评论的所有回复 在 C#.
type: docs
weight: 130
url: /zh/net/aspose.words/comment/removeallreplies/
---
## Comment.RemoveAllReplies method

删除对此评论的所有回复。

```csharp
public void RemoveAllReplies()
```

## 评论

回复的所有组成节点将从文档中删除。

## 例子

显示如何删除评论回复。

```csharp
Document doc = new Document();

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "Another reply");

Assert.AreEqual(2, comment.Replies.Count()); 

// 下面是从评论中删除回复的两种方法。
// 1 - 使用“RemoveReply”方法从评论中单独删除回复：
comment.RemoveReply(comment.Replies[0]);

Assert.AreEqual(1, comment.Replies.Count());

// 2 - 使用“RemoveAllReplies”方法一次删除评论中的所有回复：
comment.RemoveAllReplies();

Assert.AreEqual(0, comment.Replies.Count());
```

### 也可以看看

* class [Comment](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
