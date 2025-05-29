---
title: HeaderFooter Class
linktitle: HeaderFooter
articleTitle: HeaderFooter
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.HeaderFooter 类，轻松管理节页眉和页脚的解决方案。立即增强文档格式！
type: docs
weight: 3530
url: /zh/net/aspose.words/headerfooter/
---
## HeaderFooter class

表示某个部分的页眉或页脚文本的容器。

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
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直属子节点的数量。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取此节点所属的文档。 |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | 获取故事的第一段。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果此节点有任何子节点。 |
| [HeaderFooterType](../../aspose.words/headerfooter/headerfootertype/) { get; } | 获取此页眉/页脚的类型。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为这个节点可以有子节点。 |
| [IsHeader](../../aspose.words/headerfooter/isheader/) { get; } | 如果`HeaderFooter`对象是一个标题。 |
| [IsLinkedToPrevious](../../aspose.words/headerfooter/islinkedtoprevious/) { get; set; } | 如果此页眉或页脚链接到上一节中相应的页眉或页脚，则为真。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | 获取故事的最后一段。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随此节点之后的节点。 |
| override [NodeType](../../aspose.words/headerfooter/nodetype/) { get; } | 返回HeaderFooter. |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | 获取故事的直接子段落集合。 |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentSection](../../aspose.words/headerfooter/parentsection/) { get; } | 获取此故事的父部分。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取此节点前一个节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回[`Range`](../range/)表示此节点中包含的文档部分的对象。 |
| [StoryType](../../aspose.words/story/storytype/) { get; } | 获取该故事的类型。 |
| [Tables](../../aspose.words/story/tables/) { get; } | 获取故事的直接子表集合。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words/headerfooter/accept/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访客。 |
| override [AcceptEnd](../../aspose.words/headerfooter/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访问者访问标题的末尾。 |
| override [AcceptStart](../../aspose.words/headerfooter/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访问者访问标题的开头。 |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(*string*) | 创建[`Paragraph`](../paragraph/)带有可选文本的对象并将其附加到此对象的末尾。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | 从该故事的文本中删除所有形状。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点提供对每个样式迭代的支持。 |
| override [GetText](../../aspose.words/compositenode/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | 在指定的参考节点后立即插入指定的节点。 |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | 在指定的参考节点之前立即插入指定的节点。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | 根据前序树遍历算法获取下一个节点。 |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | 将指定节点添加到此节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | 根据前序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中移除。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 删除当前节点的所有子节点。 |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | 删除指定的子节点。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 删除所有[`SmartTag`](../../aspose.words.markup/smarttag/)当前节点的后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | 选择第一个[`Node`](../node/)与 XPath 表达式匹配。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点内容导出为字符串。 |

## 评论

`HeaderFooter`可以包含[`Paragraph`](../paragraph/)和[`桌子`](../../aspose.words.tables/table/)子节点。

`HeaderFooter`是节级节点，并且只能是[`Section`](../section/). 只能有一个`HeaderFooter`每个[`HeaderFooterType`](./headerfootertype/)在一个[`Section`](../section/)。

如果[`Section`](../section/)没有`HeaderFooter`特定类型或 `HeaderFooter`没有子节点，则此页眉/页脚被视为链接到 Microsoft Word 中上一节相同类型的页眉/页脚。

什么时候`HeaderFooter`至少包含一个[`Paragraph`](../paragraph/)，它不再被视为与 Microsoft Word 中的上一个相链接。

## 例子

展示如何替换文档页脚中的文本。

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

展示如何从文档中删除所有页脚。

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// 遍历每个部分并删除每种页脚。
foreach (Section section in doc.OfType<Section>())
{
    // 页脚和页眉类型有三种。
    // 1 - “第一”页眉/页脚，仅出现在部分的第一页上。
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 – “主要”页眉/页脚，出现在奇数页上。
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - “偶数”页眉/页脚，出现在偶数页上。
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

展示如何创建页眉和页脚。

```csharp
Document doc = new Document();

// 创建标题并在其后附加一个段落。该段落中的文本
// 将出现在本节每一页的顶部，正文上方。
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// 创建页脚并在其后附加一个段落。该段落中的文本
// 将出现在本节每一页的底部，正文下方。
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
