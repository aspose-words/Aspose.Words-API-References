---
title: HeaderFooter
linktitle: HeaderFooter
articleTitle: HeaderFooter
second_title: 用于 .NET 的 Aspose.Words
description: HeaderFooter 构造函数. 创建指定类型的新页眉或页脚 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter constructor

创建指定类型的新页眉或页脚。

```csharp
public HeaderFooter(DocumentBase doc, HeaderFooterType headerFooterType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | DocumentBase | 所有者文件。 |
| headerFooterType | HeaderFooterType | A[`HeaderFooterType`](../headerfootertype/)value 指定页眉或页脚的类型。 |

## 评论

什么时候[`HeaderFooter`](../)创建后，它属于指定文档，但还不是 文档的一部分并且[`ParentNode`](../../node/parentnode/)是`无效的`。

追加[`HeaderFooter`](../)到一个[`Section`](../../section/)使用[`InsertAfter`](../../compositenode/insertafter/),[`InsertBefore`](../../compositenode/insertbefore/), 或[`HeadersFooters`](../../section/headersfooters/)属性和方法[`Add`](../../nodecollection/add/),[`Insert`](../../nodecollection/insert/)。

## 例子

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

* class [DocumentBase](../../documentbase/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooter](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
