---
title: Document.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: 用于 .NET 的 Aspose.Words
description: Document JoinRunsWithSameFormatting 方法. 在文档的所有段落中以相同的格式连接运行 在 C#.
type: docs
weight: 620
url: /zh/net/aspose.words/document/joinrunswithsameformatting/
---
## Document.JoinRunsWithSameFormatting method

在文档的所有段落中以相同的格式连接运行。

```csharp
public int JoinRunsWithSameFormatting()
```

### 返回值

执行的连接数。什么时候**氮**相邻的运行被连接起来，它们算作**N-1**加入。

## 评论

这是一种优化方法。某些文档包含具有相同格式的相邻运行。 如果手动对文档进行大量编辑，通常会发生这种情况。 您可以通过合并这些运行来减小文档大小并加快进一步处理速度。

该操作检查每个[`Paragraph`](../../paragraph/)文档中的相邻节点[`Run`](../../run/) 节点具有相同的属性。它忽略用于跟踪 run 创建和修改的编辑会话的唯一标识符。每个连接序列中的第一次运行都会累积所有文本。 Remaining 运行将从文档中删除。

## 例子

演示如何在文档中加入运行以减少不需要的运行。

```csharp
// 打开一个包含具有相同格式的相邻文本行的文档，
// 如果我们在 Microsoft Word 中多次编辑同一段落，通常会发生这种情况。
Document doc = new Document(MyDir + "Rendering.docx");

// 如果任意数量的这些运行相邻并且具有相同的格式，
// 那么文档可能会被简化。
Assert.AreEqual(317, doc.GetChildNodes(NodeType.Run, true).Count);

// 将此类运行与此方法结合起来，并验证将发生的运行连接的数量。
Assert.AreEqual(121, doc.JoinRunsWithSameFormatting());

// 连接次数和连接后的运行次数
// 应该将我们最初的运行次数相加。
Assert.AreEqual(196, doc.GetChildNodes(NodeType.Run, true).Count);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
