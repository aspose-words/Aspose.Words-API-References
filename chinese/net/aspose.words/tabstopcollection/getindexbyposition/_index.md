---
title: TabStopCollection.GetIndexByPosition
linktitle: GetIndexByPosition
articleTitle: GetIndexByPosition
second_title: Aspose.Words for .NET
description: 探索 TabStopCollection 的 GetIndexByPosition 方法，轻松查找任意指定点位置的制表位索引。非常适合精准的布局控制！
type: docs
weight: 90
url: /zh/net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

获取指定位置的制表位索引（以磅为单位）。

```csharp
public int GetIndexByPosition(double position)
```

## 例子

展示如何查找某个位置以查看该位置是否存在制表位并获取其索引。

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// 在 30 毫米的位置添加一个制表位。
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

//“GetIndexByPosition”返回的结果为“0”，确认制表位
// 此集合中存在 30mm 处，其位于索引 0 处。
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

//“GetIndexByPosition”返回“-1”证实
// 此集合中没有位置为 60mm 的制表位。
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### 也可以看看

* class [TabStopCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
