---
title: CompareOptions.AdvancedOptions
linktitle: AdvancedOptions
articleTitle: AdvancedOptions
second_title: Aspose.Words for .NET
description: 探索 CompareOptions 高级选项，增强您的比较功能。通过定制设置获得精准结果，实现最佳输出。
type: docs
weight: 20
url: /zh/net/aspose.words.comparing/compareoptions/advancedoptions/
---
## CompareOptions.AdvancedOptions property

指定高级比较选项，可能有助于产生更精确的比较输出。

```csharp
public AdvancedCompareOptions AdvancedOptions { get; }
```

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

* class [AdvancedCompareOptions](../../advancedcompareoptions/)
* class [CompareOptions](../)
* 命名空间 [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* 部件 [Aspose.Words](../../../)
