---
title: Node.PreviousSibling
second_title: Aspose.Words for .NET API 参考
description: Node 财产. 获取紧接在此节点之前的节点
type: docs
weight: 70
url: /zh/net/aspose.words/node/previoussibling/
---
## Node.PreviousSibling property

获取紧接在此节点之前的节点。

```csharp
public Node PreviousSibling { get; }
```

### 评论

如果没有前面的节点，则返回null。

### 例子

演示如何使用 Node 和 CompositeNode 的方法来删除文档中最后一个部分之前的部分。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// 两个部分是彼此的兄弟。
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// 根据与另一个部分的兄弟关系删除一个部分。
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// 我们删除的部分是第一个，文档只剩下第二个。
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### 也可以看看

* class [Node](../)
* 命名空间 [Aspose.Words](../../node/)
* 部件 [Aspose.Words](../../../)


