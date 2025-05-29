---
title: EndnoteOptions.StartNumber
linktitle: StartNumber
articleTitle: StartNumber
second_title: Aspose.Words for .NET
description: 了解 EndnoteOptions StartNumber 属性如何通过自定义第一个编号的尾注以提高清晰度和组织性来增强文档。
type: docs
weight: 40
url: /zh/net/aspose.words.notes/endnoteoptions/startnumber/
---
## EndnoteOptions.StartNumber property

指定第一个自动编号尾注的起始数字或字符。

```csharp
public int StartNumber { get; set; }
```

## 评论

此属性仅在以下情况下有效[`RestartRule`](../restartrule/)设置为 Continuous。

## 例子

显示如何设置文档开始脚注/尾注计数的数字。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 脚注和尾注是将参考或旁注附加到文本的一种方式
// 不会干扰正文的流程。
// 插入脚注/尾注会添加一个小上标引用符号
// 在主体文本中插入脚注/尾注。
// 每个脚注/尾注也会创建一个条目，该条目由一个符号组成
// 与正文中的参考符号相匹配。
// 我们传递给文档构建器的“InsertEndnote”方法的参考文本。
// 默认情况下，脚注条目显示在包含以下内容的每个页面的底部
// 它们的参考符号和尾注出现在文档的末尾。
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");

// 默认情况下，每个脚注和尾注的参考符号是其索引
// 在所有文档的脚注/尾注中。每个文档都维护单独的计数
// 脚注和尾注均从 1 开始。
Assert.AreEqual(1, doc.FootnoteOptions.StartNumber);
Assert.AreEqual(1, doc.EndnoteOptions.StartNumber);

// 我们可以使用“StartNumber”属性来获取文档
// 从不同的数字开始脚注或尾注计数。
doc.EndnoteOptions.NumberStyle = NumberStyle.Arabic;
doc.EndnoteOptions.StartNumber = 50;

doc.Save(ArtifactsDir + "InlineStory.StartNumber.docx");
```

### 也可以看看

* class [EndnoteOptions](../)
* 命名空间 [Aspose.Words.Notes](../../../aspose.words.notes/)
* 部件 [Aspose.Words](../../../)
