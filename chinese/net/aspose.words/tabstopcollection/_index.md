---
title: TabStopCollection Class
linktitle: TabStopCollection
articleTitle: TabStopCollection
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.TabStopCollection 班级. 的集合TabStop代表段落或样式的自定义选项卡的对象 在 C#.
type: docs
weight: 6210
url: /zh/net/aspose.words/tabstopcollection/
---
## TabStopCollection class

的集合[`TabStop`](../tabstop/)代表段落或样式的自定义选项卡的对象。

要了解更多信息，请访问[Aspose.Words 文档对象模型 (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/)文档文章。

```csharp
public class TabStopCollection : InternableComplexAttr
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words/tabstopcollection/count/) { get; } | 获取集合中制表位的数量。 |
| [Item](../../aspose.words/tabstopcollection/item/) { get; } | 获取给定索引处的制表位。 (2 indexers) |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words/tabstopcollection/add/#add)(*[TabStop](../tabstop/)*) | 在集合中添加或替换制表位。 |
| [Add](../../aspose.words/tabstopcollection/add/#add_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | 在集合中添加或替换制表位。 |
| [After](../../aspose.words/tabstopcollection/after/)(*double*) | 获取指定位置右侧的第一个制表位。 |
| [Before](../../aspose.words/tabstopcollection/before/)(*double*) | 获取指定位置左侧的第一个制表位。 |
| [Clear](../../aspose.words/tabstopcollection/clear/)() | 删除所有制表位位置。 |
| override [Equals](../../aspose.words/tabstopcollection/equals/#equals_1)(*object*) | 确定指定对象的值是否等于当前对象。 |
| [Equals](../../aspose.words/tabstopcollection/equals/#equals)(*TabStopCollection*) | 判断是否指定`TabStopCollection`与当前值相等`TabStopCollection`. |
| override [GetHashCode](../../aspose.words/tabstopcollection/gethashcode/)() | 用作此类型的哈希函数。 |
| [GetIndexByPosition](../../aspose.words/tabstopcollection/getindexbyposition/)(*double*) | 获取指定位置的制表位索引（以磅为单位）。 |
| [GetPositionByIndex](../../aspose.words/tabstopcollection/getpositionbyindex/)(*int*) | 获取指定索引处制表位的位置（以磅为单位）。 |
| [RemoveByIndex](../../aspose.words/tabstopcollection/removebyindex/)(*int*) | 从集合中删除指定索引处的制表位。 |
| [RemoveByPosition](../../aspose.words/tabstopcollection/removebyposition/)(*double*) | 从集合中删除指定位置处的制表位。 |

## 评论

在 Microsoft Word 文档中，制表位可以在 paragraph 样式的属性中定义，也可以直接在段落的属性中定义。一个样式可以基于另一个样式。 因此，给定对象的完整制表位集是直接在此对象上定义的制表位 和从父样式继承的制表位的组合。

在 Aspose.Words 中，当您获得`TabStopCollection`对于段落或样式， 它仅包含直接为此段落或样式定义的自定义制表位。 该集合不包括在父样式中定义的制表位或默认制表位。

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

* class [InternableComplexAttr](../internablecomplexattr/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
