---
title: WarningInfoCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: 通过索引轻松访问特定的WarningInfoCollection项目。使用我们直观的属性功能简化您的数据管理！
type: docs
weight: 30
url: /zh/net/aspose.words/warninginfocollection/item/
---
## WarningInfoCollection indexer

获取指定索引处的项目。

```csharp
public WarningInfo this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 该项目的从零开始的索引。 |

## 例子

展示如何获取有关不支持格式的警告。

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.AreEqual("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings[0].Description);
Assert.AreEqual(1, warnings.Count);
```

### 也可以看看

* class [WarningInfo](../../warninginfo/)
* class [WarningInfoCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
