---
title: Node.PreviousSibling
linktitle: PreviousSibling
articleTitle: PreviousSibling
second_title: 用于 .NET 的 Aspose.Words
description: Node PreviousSibling 财产. 获取紧邻此节点之前的节点 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words/node/previoussibling/
---
## Node.PreviousSibling property

获取紧邻此节点之前的节点。

```csharp
public Node PreviousSibling { get; }
```

## 评论

如果没有前面的节点，则`无效的`返回。

## 例子

演示如何使用 Node 和 CompositeNode 的方法删除文档中最后一部分之前的部分。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// 两个部分互为兄弟部分。
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// 根据与另一个部分的兄弟关系删除一个部分。
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// 我们删除的部分是第一个部分，文档中只剩下第二个部分。
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### 也可以看看

* class [Node](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
