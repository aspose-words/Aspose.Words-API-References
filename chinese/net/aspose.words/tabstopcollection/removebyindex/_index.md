---
title: TabStopCollection.RemoveByIndex
linktitle: RemoveByIndex
articleTitle: RemoveByIndex
second_title: Aspose.Words for .NET
description: 使用 RemoveByIndex 方法轻松管理制表位。快速从集合中移除任何制表位，简化设计。
type: docs
weight: 110
url: /zh/net/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection.RemoveByIndex method

从集合中删除指定索引处的制表位。

```csharp
public void RemoveByIndex(int index)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | Int32 | 制表位集合的索引。 |

## 例子

展示如何通过索引选择文档中的制表位并将其删除。

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

Assert.AreEqual(2, tabStops.Count);

// 删除第一个制表位。
tabStops.RemoveByIndex(0);

Assert.AreEqual(1, tabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.RemoveByIndex.docx");
```

### 也可以看看

* class [TabStopCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
