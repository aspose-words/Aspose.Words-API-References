---
title: TabStopCollection.Before
linktitle: Before
articleTitle: Before
second_title: Aspose.Words for .NET
description: 发现 TabStopCollection Before 方法，高效检索最近的左侧制表位，以便在应用程序中进行无缝导航。
type: docs
weight: 50
url: /zh/net/aspose.words/tabstopcollection/before/
---
## TabStopCollection.Before method

获取指定位置左侧的第一个制表位。

```csharp
public TabStop Before(double position)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| position | Double | 参考位置（以点为单位）。 |

### 返回值

制表位对象或`无效的`如果没有找到合适的制表位。

## 评论

跳过制表位[`Alignment`](../../tabstop/alignment/)设置为Bar。

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

// 每个“制表符”都会将构建器的光标移动到下一个制表位的位置。
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// 每个段落都会获得其制表位集合，该集合从文档构建器的制表位集合中克隆其值。
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// 制表位集合可以指向某些位置之前和之后的制表位。
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
