---
title: Story.AppendParagraph
linktitle: AppendParagraph
articleTitle: AppendParagraph
second_title: 用于 .NET 的 Aspose.Words
description: Story AppendParagraph 方法. 创建一个快捷方法Paragraph具有可选文本的对象并将其附加到该对象的末尾 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words/story/appendparagraph/
---
## Story.AppendParagraph method

创建一个快捷方法[`Paragraph`](../../paragraph/)具有可选文本的对象并将其附加到该对象的末尾。

```csharp
public Paragraph AppendParagraph(string text)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| text | String | 该段落的文本。可`无效的`或空字符串。 |

### 返回值

新创建和附加的段落。

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

* class [Paragraph](../../paragraph/)
* class [Story](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
