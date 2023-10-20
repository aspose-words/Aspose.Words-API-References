---
title: HeaderFooterCollection Class
linktitle: HeaderFooterCollection
articleTitle: HeaderFooterCollection
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.HeaderFooterCollection 班级. 提供对以下内容的类型化访问HeaderFooter的节点Section 在 C#.
type: docs
weight: 3110
url: /zh/net/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class

提供对以下内容的类型化访问[`HeaderFooter`](../headerfooter/)的节点[`Section`](../section/).

要了解更多信息，请访问[使用页眉和页脚](https://docs.aspose.com/words/net/working-with-headers-and-footers/)文档文章。

```csharp
public class HeaderFooterCollection : NodeCollection
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | 获取集合中的节点数。 |
| [Item](../../aspose.words/headerfootercollection/item/) { get; } | 检索[`HeaderFooter`](../headerfooter/)在给定的索引. (3 indexers) |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | 将节点添加到集合的末尾。 |
| [Clear](../../aspose.words/nodecollection/clear/)() | 从此集合和文档中删除所有节点。 |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | 确定节点是否在集合中。 |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | 在节点集合上提供简单的“foreach”样式迭代。 |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | 返回指定节点的从零开始的索引。 |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | 将节点插入集合中指定索引处。 |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious_1)(*bool*) | 将所有页眉和页脚链接或取消链接到上一节中相应的 页眉和页脚。 |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious)(*[HeaderFooterType](../headerfootertype/), bool*) | 将指定的页眉或页脚链接或取消链接到上一节中相应的 页眉或页脚。 |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | 从集合和文档中删除节点。 |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | 从集合和文档中删除指定索引处的节点。 |
| [ToArray](../../aspose.words/headerfootercollection/toarray/#toarray)() | 复制全部`页眉页脚` 从集合到一个新数组`页眉页脚`s. (2 methods) |

## 评论

最多可以有 1 个[`HeaderFooter`](../headerfooter/)

每个[`HeaderFooterType`](../headerfootertype/)per [`Section`](../section/).

[`HeaderFooter`](../headerfooter/)对象可以按任何顺序出现在集合中。

## 例子

演示如何从文档中删除所有页脚。

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// 遍历每个部分并删除每种页脚。
foreach (Section section in doc.OfType<Section>())
{
    // 页脚和页眉类型分为三种。
    // 1 - “第一”页眉/页脚，仅出现在节的第一页上。
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - “主要”页眉/页脚，出现在奇数页上。
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - “偶数”页眉/页脚，出现在偶数页上。
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

演示如何创建页眉和页脚。

```csharp
Document doc = new Document();

// 创建一个标题并向其附加一个段落。该段落中的文字
// 将出现在本节每个页面的顶部，主体文本上方。
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// 创建一个页脚并向其附加一个段落。该段落中的文字
// 将出现在本节每个页面的底部，主体文本下方。
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### 也可以看看

* class [NodeCollection](../nodecollection/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
