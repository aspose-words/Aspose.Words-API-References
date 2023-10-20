---
title: HeaderFooter Class
linktitle: HeaderFooter
articleTitle: HeaderFooter
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.HeaderFooter 班级. 表示节的页眉或页脚文本的容器 在 C#.
type: docs
weight: 3100
url: /zh/net/aspose.words/headerfooter/
---
## HeaderFooter class

表示节的页眉或页脚文本的容器。

要了解更多信息，请访问[使用页眉和页脚](https://docs.aspose.com/words/net/working-with-headers-and-footers/)文档文章。

```csharp
public class HeaderFooter : Story
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [HeaderFooter](headerfooter/)(*[DocumentBase](../documentbase/), [HeaderFooterType](../headerfootertype/)*) | 创建指定类型的新页眉或页脚。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直接子节点的数量。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取该节点所属的文档。 |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | 获取故事中的第一段。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果该节点有任何子节点. |
| [HeaderFooterType](../../aspose.words/headerfooter/headerfootertype/) { get; } | 获取此页眉/页脚的类型。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为该节点可以有子节点。 |
| [IsHeader](../../aspose.words/headerfooter/isheader/) { get; } | 如果是这样则为真`HeaderFooter`对象是一个标头。 |
| [IsLinkedToPrevious](../../aspose.words/headerfooter/islinkedtoprevious/) { get; set; } | 如果此页眉或页脚链接到上一节中相应的页眉或页脚 ，则为 True。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | 获取故事的最后一段。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随该节点的下一个节点。 |
| override [NodeType](../../aspose.words/headerfooter/nodetype/) { get; } | 返回HeaderFooter. |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | 获取故事直接子级的段落集合。 |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentSection](../../aspose.words/headerfooter/parentsection/) { get; } | 获取此故事的父部分。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取紧邻此节点之前的节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回一个[`Range`](../range/)表示此节点中包含的文档部分的对象。 |
| [StoryType](../../aspose.words/story/storytype/) { get; } | 获取此故事的类型。 |
| [Tables](../../aspose.words/story/tables/) { get; } | 获取作为故事的直接子级的表的集合。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words/headerfooter/accept/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访客。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | 将指定节点添加到该节点的子节点列表的末尾。 |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(*string*) | 创建一个快捷方法[`Paragraph`](../paragraph/)具有可选文本的对象并将其附加到该对象的末尾。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | 删除此故事文本中的所有形状。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点上的每个样式迭代提供支持。 |
| override [GetText](../../aspose.words/compositenode/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../node/), [Node](../node/)*) | 在指定的引用节点之后立即插入指定的节点。 |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../node/), [Node](../node/)*) | 在指定的引用节点之前插入指定的节点。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | 根据先序树遍历算法获取下一个节点。 |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../node/)*) | 将指定节点添加到该节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | 根据先序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中删除。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 删除当前节点的所有子节点。 |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../node/)*) | 删除指定的子节点。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 删除所有[`SmartTag`](../../aspose.words.markup/smarttag/)当前节点的后代节点. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | 选择第一个[`Node`](../node/)与 XPath 表达式匹配。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点的内容导出到字符串中。 |

## 评论

`HeaderFooter`可以包含[`Paragraph`](../paragraph/)和[`桌子`](../../aspose.words.tables/table/)子节点。

`HeaderFooter`是一个节级节点并且只能是[`Section`](../section/). 只能有一个`HeaderFooter`每个[`HeaderFooterType`](./headerfootertype/)在一个[`Section`](../section/)。

如果[`Section`](../section/)没有`HeaderFooter`特定类型 or 的`HeaderFooter`没有子节点，则此页眉/页脚被视为链接到 Microsoft Word 中与上一节相同类型的页眉/页脚。

什么时候`HeaderFooter`至少包含一个[`Paragraph`](../paragraph/)，它不再 被视为与 Microsoft Word 中的上一个链接。

## 例子

演示如何替换文档页脚中的文本。

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

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

* class [Story](../story/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
