---
title: TabStopCollection.GetPositionByIndex
linktitle: GetPositionByIndex
articleTitle: GetPositionByIndex
second_title: 用于 .NET 的 Aspose.Words
description: TabStopCollection GetPositionByIndex 方法. 获取指定索引处制表位的位置以磅为单位 在 C#.
type: docs
weight: 100
url: /zh/net/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection.GetPositionByIndex method

获取指定索引处制表位的位置（以磅为单位）。

```csharp
public double GetPositionByIndex(int index)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | Int32 | 制表位集合的索引。 |

### 返回值

制表位的位置。

## 例子

显示如何查找选项卡、按其索引停止并验证其位置。

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

// 验证集合中第二个制表位的位置。
Assert.AreEqual(ConvertUtil.MillimeterToPoint(60), tabStops.GetPositionByIndex(1), 0.1d);
```

### 也可以看看

* class [TabStopCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
