---
title: AdvancedCompareOptions.IgnoreDmlUniqueId
linktitle: IgnoreDmlUniqueId
articleTitle: IgnoreDmlUniqueId
second_title: Aspose.Words for .NET
description: 探索 AdvancedCompareOptions IgnoreDmlUniqueId 属性，高效管理唯一 ID，增强您的 DrawingML 处理能力。优化您的工作流程！
type: docs
weight: 20
url: /zh/net/aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/
---
## AdvancedCompareOptions.IgnoreDmlUniqueId property

指定是否忽略 DrawingML 唯一 ID 的差异。

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

## 评论

默认值为`错误的`.

## 例子

展示如何忽略 DML 唯一 ID 来比较文档。

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// 默认情况下，Aspose.Words 不会忽略 DML 的唯一 ID，并且修订计数为 2。
// 如果我们忽略 DML 的唯一 ID，修订计数为 0。
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### 也可以看看

* class [AdvancedCompareOptions](../)
* 命名空间 [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* 部件 [Aspose.Words](../../../)
