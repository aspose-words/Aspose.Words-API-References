---
title: WarningInfoCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: 探索WarningInfoCollection Count属性，轻松访问集合中的元素总数，实现高效的数据管理。
type: docs
weight: 20
url: /zh/net/aspose.words/warninginfocollection/count/
---
## WarningInfoCollection.Count property

获取集合中包含的元素数量。

```csharp
public int Count { get; }
```

## 例子

展示如何获取有关不支持格式的警告。

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.AreEqual("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings[0].Description);
Assert.AreEqual(1, warnings.Count);
```

### 也可以看看

* class [WarningInfoCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
