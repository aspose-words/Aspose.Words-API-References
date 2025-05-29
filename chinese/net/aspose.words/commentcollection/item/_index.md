---
title: CommentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: 使用 CommentCollection Item 属性轻松访问特定评论。通过索引检索评论，简化内容管理。
type: docs
weight: 10
url: /zh/net/aspose.words/commentcollection/item/
---
## CommentCollection indexer

检索[`Comment`](../../comment/)在给定的索引处。

```csharp
public Comment this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 集合的索引。 |

## 评论

该索引从零开始。

允许使用负索引，表示从集合的后面进行访问。 例如 -1 表示最后一项，-2 表示倒数第二项，依此类推。

如果索引大于或等于列表中的项目数，则返回空引用。

如果索引为负数并且其绝对值大于列表中的项目数，则返回空引用。

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

* class [Comment](../../comment/)
* class [CommentCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
