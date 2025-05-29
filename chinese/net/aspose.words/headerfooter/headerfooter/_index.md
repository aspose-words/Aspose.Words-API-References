---
title: HeaderFooter
linktitle: HeaderFooter
articleTitle: HeaderFooter
second_title: Aspose.Words for .NET
description: 使用我们直观的构造器，轻松设计出精美的页眉和页脚。定制您的网站外观，打造独特、专业的风格！
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
| headerFooterType | HeaderFooterType | 一个[`HeaderFooterType`](../headerfootertype/)value 指定页眉或页脚的类型。 |

## 评论

什么时候[`HeaderFooter`](../)已创建，它属于指定文档，但尚未成为文档的一部分，并且[`ParentNode`](../../node/parentnode/)是`无效的`。

附加[`HeaderFooter`](../)到[`Section`](../../section/)使用[`InsertAfter`](../../compositenode/insertafter/)，[`InsertBefore`](../../compositenode/insertbefore/), 或[`HeadersFooters`](../../section/headersfooters/)属性和方法[`Add`](../../nodecollection/add/)，[`Insert`](../../nodecollection/insert/)。

## 例子

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

* class [DocumentBase](../../documentbase/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooter](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
