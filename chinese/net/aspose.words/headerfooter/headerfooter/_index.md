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
| headerFooterType | HeaderFooterType | 一个[`HeaderFooterType`](../headerfootertype/)value 指定页眉或页脚的类型。 |

## 评论

什么时候**页眉页脚**被创建，它属于指定的文档，但不是 还不是文档的一部分，并且**父节点**一片空白。

追加**页眉页脚**到一个**部分**使用 Section.InsertAfter、Section.InsertBefore、 HeadersFooters.Add 或 HeadersFooters.Insert。

## 例子

显示如何创建页眉和页脚。

```csharp
Document doc = new Document();

// 创建一个标题并在其上附加一个段落。该段中的文字
// 将出现在本节每一页的顶部，主体文本上方。
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// 创建一个页脚并向其附加一个段落。该段中的文字
// 将出现在本节每一页的底部，主体文本下方。
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
