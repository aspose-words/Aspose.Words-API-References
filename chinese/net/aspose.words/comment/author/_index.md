---
title: Comment.Author
linktitle: Author
articleTitle: Author
second_title: 用于 .NET 的 Aspose.Words
description: Comment Author 财产. 返回或设置评论的作者姓名 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words/comment/author/
---
## Comment.Author property

返回或设置评论的作者姓名。

```csharp
public string Author { get; set; }
```

## 评论

不可能是`无效的`。

默认为空字符串。

## 例子

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
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
