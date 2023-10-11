---
title: TabStopCollection.GetIndexByPosition
second_title: Aspose.Words for .NET API 参考
description: TabStopCollection 方法. 获取指定位置的制表位索引以磅为单位
type: docs
weight: 90
url: /zh/net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

获取指定位置的制表位索引（以磅为单位）。

```csharp
public int GetIndexByPosition(double position)
```

### 例子

演示如何查找位置以查看该位置是否存在制表位并获取其索引。

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// 在 30mm 的位置添加制表位。
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// “GetIndexByPosition”返回的结果“0”确认制表位
// 该集合中存在 30mm 处的位置，并且它位于索引 0 处。
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

// “GetIndexByPosition”返回的“-1”确认
// 该集合中没有位置为 60mm 的制表位。
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### 也可以看看

* class [TabStopCollection](../)
* 命名空间 [Aspose.Words](../../tabstopcollection/)
* 部件 [Aspose.Words](../../../)


