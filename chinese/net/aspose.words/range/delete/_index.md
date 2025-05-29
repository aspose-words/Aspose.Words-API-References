---
title: Range.Delete
linktitle: Delete
articleTitle: Delete
second_title: Aspose.Words for .NET
description: 使用“范围删除”方法高效删除指定范围内的所有字符。轻松简化您的文本编辑任务！
type: docs
weight: 70
url: /zh/net/aspose.words/range/delete/
---
## Range.Delete method

删除范围内的所有字符。

```csharp
public void Delete()
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

* class [Range](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
