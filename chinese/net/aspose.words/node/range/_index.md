---
title: Node.Range
linktitle: Range
articleTitle: Range
second_title: Aspose.Words for .NET
description: 发现节点范围属性，轻松访问定义节点内的文档段的范围对象，以增强内容管理。
type: docs
weight: 80
url: /zh/net/aspose.words/node/range/
---
## Node.Range property

返回[`Range`](../../range/)表示此节点中包含的文档部分的对象。

```csharp
public Range Range { get; }
```

## 例子

显示如何删除某个范围内的所有节点。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 在文档的第一部分添加文本，然后添加另一部分。
builder.Write("Section 1. ");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Write("Section 2.");

Assert.AreEqual("Section 1. \fSection 2.", doc.GetText().Trim());

// 通过删除所有节点来完全删除第一部分
// 在其范围内，包括该部分本身。
doc.Sections[0].Range.Delete();

Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual("Section 2.", doc.GetText().Trim());
```

### 也可以看看

* class [Range](../../range/)
* class [Node](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
