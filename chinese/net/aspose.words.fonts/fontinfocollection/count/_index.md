---
title: FontInfoCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: 发现 FontInfoCollection Count 属性，轻松检索集合中的元素总数，实现无缝数据管理。
type: docs
weight: 10
url: /zh/net/aspose.words.fonts/fontinfocollection/count/
---
## FontInfoCollection.Count property

获取集合中包含的元素数量。

```csharp
public int Count { get; }
```

## 例子

显示有关空白文档中存在的字体的信息。

```csharp
Document doc = new Document();

// 一个空白文档包含 3 种默认字体。文档中的每种字体
// 将有一个相应的 FontInfo 对象，其中包含有关该字体的详细信息。
Assert.AreEqual(3, doc.FontInfos.Count);

Assert.True(doc.FontInfos.Contains("Times New Roman"));
Assert.AreEqual(204, doc.FontInfos["Times New Roman"].Charset);

Assert.True(doc.FontInfos.Contains("Symbol"));
Assert.True(doc.FontInfos.Contains("Arial"));
```

### 也可以看看

* class [FontInfoCollection](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
