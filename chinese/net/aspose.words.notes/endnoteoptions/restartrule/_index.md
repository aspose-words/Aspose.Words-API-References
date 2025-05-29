---
title: EndnoteOptions.RestartRule
linktitle: RestartRule
articleTitle: RestartRule
second_title: Aspose.Words for .NET
description: 了解 EndnoteOptions RestartRule 属性如何通过控制自动编号来增强文档的质量，使其呈现精致、专业的外观。
type: docs
weight: 30
url: /zh/net/aspose.words.notes/endnoteoptions/restartrule/
---
## EndnoteOptions.RestartRule property

确定自动编号何时重新开始。

```csharp
public FootnoteNumberingRule RestartRule { get; set; }
```

## 评论

并非所有值都适用于尾注。 要确定哪些值适用，请参阅[`FootnoteNumberingRule`](../../footnotenumberingrule/)。

## 例子

显示如何在文档的某些位置重新开始脚注/尾注编号。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 脚注和尾注是将参考或旁注附加到文本的一种方式
// 不会干扰正文的流程。
// 插入脚注/尾注会添加一个小上标引用符号
// 在主体文本中插入脚注/尾注。
// 每个脚注/尾注也会创建一个条目，该条目由与参考匹配的符号组成
// 正文中的符号。我们传递给文档构建器的“InsertEndnote”方法的参考文本。
// 默认情况下，脚注条目显示在包含以下内容的每个页面的底部
// 它们的参考符号和尾注出现在文档的末尾。
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 4.");

builder.InsertBreak(BreakType.PageBreak);

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 4.");

// 默认情况下，每个脚注和尾注的参考符号是其索引
// 在所有文档的脚注/尾注中。每个文档都维护单独的计数
// 用于脚注和尾注，并且不会在任何时候重新开始这些计数。
Assert.AreEqual(doc.FootnoteOptions.RestartRule, FootnoteNumberingRule.Default);
Assert.AreEqual(FootnoteNumberingRule.Default, FootnoteNumberingRule.Continuous);

// 我们可以使用“RestartRule”属性来让文档重新启动
// 脚注/尾注计入新页面或新章节。
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### 也可以看看

* enum [FootnoteNumberingRule](../../footnotenumberingrule/)
* class [EndnoteOptions](../)
* 命名空间 [Aspose.Words.Notes](../../../aspose.words.notes/)
* 部件 [Aspose.Words](../../../)
