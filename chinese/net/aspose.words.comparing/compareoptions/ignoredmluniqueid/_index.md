---
title: CompareOptions.IgnoreDmlUniqueId
linktitle: IgnoreDmlUniqueId
articleTitle: IgnoreDmlUniqueId
second_title: 用于 .NET 的 Aspose.Words
description: CompareOptions IgnoreDmlUniqueId 财产. 指定是否忽略 DrawingML 唯一 ID 中的差异 默认值为错误的 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words.comparing/compareoptions/ignoredmluniqueid/
---
## CompareOptions.IgnoreDmlUniqueId property

指定是否忽略 DrawingML 唯一 ID 中的差异。 默认值为`错误的`.

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

## 例子

演示如何比较文档而忽略 DML 唯一 ID。

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// 默认情况下，Aspose.Words 不会忽略 DML 的唯一 ID，并且修订计数为 2。
// 如果我们忽略 DML 的唯一 ID，则修订计数为 0。
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### 也可以看看

* class [CompareOptions](../)
* 命名空间 [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* 部件 [Aspose.Words](../../../)
