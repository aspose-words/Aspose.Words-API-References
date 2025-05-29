---
title: Node.PreviousSibling
linktitle: PreviousSibling
articleTitle: PreviousSibling
second_title: Aspose.Words for .NET
description: 探索 Node PreviousSibling 属性，轻松访问当前节点之前的节点，增强您的 DOM 操作技能。
type: docs
weight: 70
url: /zh/net/aspose.words/node/previoussibling/
---
## Node.PreviousSibling property

获取此节点前一个节点。

```csharp
public Node PreviousSibling { get; }
```

## 评论

如果没有前一个节点，则`无效的`被返回。

## 例子

展示如何使用 Node 和 CompositeNode 的方法删除文档中最后一节之前的部分。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// 这两个部分互为兄弟。
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// 根据与另一个部分的兄弟关系删除一个部分。
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// 我们删除的是第一部分，文档中只剩下第二部分。
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### 也可以看看

* class [Node](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
