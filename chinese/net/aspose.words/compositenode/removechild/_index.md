---
title: CompositeNode.RemoveChild
linktitle: RemoveChild
articleTitle: RemoveChild
second_title: 用于 .NET 的 Aspose.Words
description: CompositeNode RemoveChild 方法. 删除指定的子节点 在 C#.
type: docs
weight: 170
url: /zh/net/aspose.words/compositenode/removechild/
---
## CompositeNode.RemoveChild method

删除指定的子节点。

```csharp
public Node RemoveChild(Node oldChild)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| oldChild | Node | 要删除的节点。 |

### 返回值

删除的节点。

## 评论

的父母*oldChild*被设定为`无效的`节点被删除后。

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

* class [Node](../../node/)
* class [CompositeNode](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
