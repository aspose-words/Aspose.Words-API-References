---
title: Document.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words for .NET
description: 了解 JoinRunsWithSameFormatting 方法如何无缝合并文档段落中的格式化文本，以获得精美、专业的外观。
type: docs
weight: 660
url: /zh/net/aspose.words/document/joinrunswithsameformatting/
---
## Document.JoinRunsWithSameFormatting method

将文档所有段落中具有相同格式的文本合并。

```csharp
public int JoinRunsWithSameFormatting()
```

### 返回值

执行的连接次数。当**北**相邻的运行被连接起来，它们算作**N-1**加入。

## 评论

这是一种优化方法。有些文档包含格式相同的相邻片段。 通常，如果文档经过大量手动编辑，就会出现这种情况。 您可以通过合并这些片段来减小文档大小，并加快后续处理速度。

操作检查每一个[`Paragraph`](../../paragraph/)文档中相邻节点[`Run`](../../run/)具有相同属性的 节点。它会忽略用于跟踪 run 创建和修改编辑会话的唯一标识符。每个连接序列中的第一个 run 会累积所有文本。剩余的 run 将从文档中删除。

## 例子

展示如何合并文档中的运行以减少不必要的运行。

```csharp
// 打开包含相同格式的相邻文本的文档，
// 如果我们在 Microsoft Word 中多次编辑同一个段落，通常会发生这种情况。
Document doc = new Document(MyDir + "Rendering.docx");

// 如果这些运行中有任意数量的相邻且格式相同，
// 那么文档可能会被简化。
Assert.AreEqual(317, doc.GetChildNodes(NodeType.Run, true).Count);

// 将此方法与此类运行结合起来，并验证将发生的运行连接次数。
Assert.AreEqual(121, doc.JoinRunsWithSameFormatting());

// 连接次数以及连接后的运行次数
// 应该把我们最初的运行次数加起来。
Assert.AreEqual(196, doc.GetChildNodes(NodeType.Run, true).Count);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
