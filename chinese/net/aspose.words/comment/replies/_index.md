---
title: Comment.Replies
linktitle: Replies
articleTitle: Replies
second_title: Aspose.Words for .NET
description: 发现评论回复。访问直接回复您指定评论的评论对象集合，增强用户参与度和互动性。
type: docs
weight: 110
url: /zh/net/aspose.words/comment/replies/
---
## Comment.Replies property

返回[`Comment`](../)指定注释的直接子对象。

```csharp
public CommentCollection Replies { get; }
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

* class [CommentCollection](../../commentcollection/)
* class [Comment](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
