---
title: Story.AppendParagraph
linktitle: AppendParagraph
articleTitle: AppendParagraph
second_title: Aspose.Words for .NET
description: 探索 Story AppendParagraph 方法，轻松创建并附加带有可自定义文本的 Paragraph 对象，以实现无缝文档增强。
type: docs
weight: 60
url: /zh/net/aspose.words/story/appendparagraph/
---
## Story.AppendParagraph method

创建[`Paragraph`](../../paragraph/)带有可选文本的对象并将其附加到此对象的末尾。

```csharp
public Paragraph AppendParagraph(string text)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| text | String | 段落的文本。可以是`无效的`或空字符串。 |

### 返回值

新创建并附加的段落。

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

* class [Paragraph](../../paragraph/)
* class [Story](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
