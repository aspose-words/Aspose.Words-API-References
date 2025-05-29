---
title: SectionCollection Class
linktitle: SectionCollection
articleTitle: SectionCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.SectionCollection 类——通过强大的功能和灵活性高效管理文档部分的首选解决方案。
type: docs
weight: 6570
url: /zh/net/aspose.words/sectioncollection/
---
## SectionCollection class

的集合[`Section`](../section/)文档中的对象。

要了解更多信息，请访问[使用部分](https://docs.aspose.com/words/net/working-with-sections/)文档文章。

```csharp
public class SectionCollection : NodeCollection
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | 获取集合中的节点数。 |
| [Item](../../aspose.words/sectioncollection/item/) { get; } | 检索给定索引处的部分。 (2 indexers) |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | 在集合末尾添加一个节点。 |
| [Clear](../../aspose.words/nodecollection/clear/)() | 从此集合和文档中删除所有节点。 |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | 确定节点是否在集合中。 |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | 提供对节点集合的简单“foreach”样式迭代。 |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | 返回指定节点的从零开始的索引。 |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | 将节点插入到指定索引的集合中。 |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | 从集合和文档中删除节点。 |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | 从集合和文档中删除指定索引处的节点。 |
| [ToArray](../../aspose.words/sectioncollection/toarray/#toarray_1)() | 将集合中的所有部分复制到新的部分数组中。 (2 methods) |

## 评论

Microsoft Word 文档可以包含多个节。要在 Microsoft Word 中创建节，请选择“插入/分隔符”命令并选择分隔符类型。分隔符指定节是从新页面开始还是从同一页面开始。

邮件合并期间，您可以通过编程方式插入和删除部分来自定义生成的文档。如果某个文档需要根据某些条件包含不同的内容或部分内容，您可以创建一个包含多个部分的“主”文档，并在邮件合并之前或之后删除其中的部分内容。

## 例子

展示如何在文档中添加和删除章节。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// 从文档中删除第一部分。
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// 将现在第一部分的副本附加到文档末尾。
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### 也可以看看

* class [NodeCollection](../nodecollection/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
