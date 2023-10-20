---
title: TabStopCollection.Item
linktitle: Item
articleTitle: Item
second_title: 用于 .NET 的 Aspose.Words
description: TabStopCollection Item 财产. 获取给定索引处的制表位 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words/tabstopcollection/item/
---
## TabStopCollection indexer (1 of 2)

获取给定索引处的制表位。

```csharp
public TabStop this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 制表位集合的索引。 |

## 例子

展示如何使用文档的制表位集合。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 点是 Microsoft Word 制表位标尺上的一“英寸”。
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// 每个“制表符”字符都会将构建器的光标移动到下一个制表位的位置。
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// 每个段落都获取其制表位集合，该集合从文档构建器的制表位集合克隆其值。
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// 制表位集合可以将我们指向某些位置之前和之后的制表位。
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// 我们可以清除段落的制表位集合以恢复默认的制表行为。
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### 也可以看看

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## TabStopCollection indexer (2 of 2)

获取指定位置处的制表位。

```csharp
public TabStop this[double position] { get; }
```

| 范围 | 描述 |
| --- | --- |
| position | 制表位的位置（以磅为单位）。 |

## 评论

返回`无效的`如果在指定位置没有找到制表位。

## 例子

展示如何使用文档的制表位集合。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 点是 Microsoft Word 制表位标尺上的一“英寸”。
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// 每个“制表符”字符都会将构建器的光标移动到下一个制表位的位置。
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// 每个段落都获取其制表位集合，该集合从文档构建器的制表位集合克隆其值。
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// 制表位集合可以将我们指向某些位置之前和之后的制表位。
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// 我们可以清除段落的制表位集合以恢复默认的制表行为。
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### 也可以看看

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
