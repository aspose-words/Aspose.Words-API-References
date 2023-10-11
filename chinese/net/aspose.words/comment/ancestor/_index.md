---
title: Comment.Ancestor
second_title: Aspose.Words for .NET API 参考
description: Comment 财产. 返回父级Comment目的退货无效的获取顶级评论
type: docs
weight: 20
url: /zh/net/aspose.words/comment/ancestor/
---
## Comment.Ancestor property

返回父级[`Comment`](../)目的。退货`无效的`获取顶级评论。

```csharp
public Comment Ancestor { get; }
```

### 例子

演示如何打印文档的所有注释及其回复。

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// 如果评论没有祖先，则它是“顶级”评论，而不是回复类型评论。
// 打印所有顶级评论以及他们可能有的任何回复。
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null))
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
* 命名空间 [Aspose.Words](../../comment/)
* 部件 [Aspose.Words](../../../)


