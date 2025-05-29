---
title: CompositeNode.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words for .NET
description: 探索 CompositeNode 的 GetEnumerator 方法，实现对子节点的无缝迭代。这项强大的功能将提升您的编码效率！
type: docs
weight: 120
url: /zh/net/aspose.words/compositenode/getenumerator/
---
## CompositeNode.GetEnumerator method

为该节点的子节点提供对每个样式迭代的支持。

```csharp
public IEnumerator<Node> GetEnumerator()
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

* class [Node](../../node/)
* class [CompositeNode](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
