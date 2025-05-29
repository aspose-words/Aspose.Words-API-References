---
title: Comment.Ancestor
linktitle: Ancestor
articleTitle: Ancestor
second_title: Aspose.Words for .NET
description: 使用 Ancestor 属性检索父评论对象。非常适合导航评论线程并增强用户参与度。
type: docs
weight: 20
url: /zh/net/aspose.words/comment/ancestor/
---
## Comment.Ancestor property

返回父级[`Comment`](../)对象。返回`无效的`用于顶级评论。

```csharp
public Comment Ancestor { get; }
```

## 例子

展示如何打印文档的所有评论及其回复。

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// 如果评论没有祖先，它就是“顶级”评论，而不是回复类型的评论。
// 打印所有顶级评论及其可能有的任何回复。
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null).ToList())
{
    Console.WriteLine("Top-level comment:");
    Console.WriteLine($"\t\"{comment.GetText().Trim()}\", by {comment.Author}");
    Console.WriteLine($"Has {comment.Replies.Count} replies");
    foreach (Comment commentReply in comment.Replies)
    {
        Console.WriteLine($"\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
    }
    Console.WriteLine();
}
```

### 也可以看看

* class [Comment](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
