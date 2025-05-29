---
title: CompositeNode.RemoveChild
linktitle: RemoveChild
articleTitle: RemoveChild
second_title: Aspose.Words for .NET
description: 使用 RemoveChild 方法轻松管理您的 CompositeNode，旨在简化节点删除，从而提高性能和效率。
type: docs
weight: 190
url: /zh/net/aspose.words/compositenode/removechild/
---
## CompositeNode.RemoveChild&lt;T&gt; method

删除指定的子节点。

```csharp
public T RemoveChild<T>(T oldChild)
    where T : Node
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| oldChild | T | 要移除的节点。 |

### 返回值

被移除的节点。

## 评论

的父母*oldChild*设置为`无效的`节点被移除后。

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

* class [Node](../../node/)
* class [CompositeNode](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
