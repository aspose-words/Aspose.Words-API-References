---
title: Document.EndnoteOptions
linktitle: EndnoteOptions
articleTitle: EndnoteOptions
second_title: Aspose.Words for .NET
description: 探索 EndnoteOptions 属性以自定义尾注编号和定位，增强文档的清晰度和专业性。
type: docs
weight: 120
url: /zh/net/aspose.words/document/endnoteoptions/
---
## Document.EndnoteOptions property

提供控制本文档中尾注编号和定位的选项。

```csharp
public EndnoteOptions EndnoteOptions { get; }
```

## 例子

显示如何选择文档收集和显示其尾注的不同位置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 尾注是一种将参考或旁注附加到文本的方式
// 不会干扰正文的流程。
// 插入尾注会添加一个小上标引用符号
// 在主体文本中插入尾注。
// 每个尾注还会在文档末尾创建一个条目，由一个符号组成
// 与正文中的参考符号相匹配。
// 我们传递给文档构建器的“InsertEndnote”方法的参考文本。
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// 我们可以使用“Position”属性来确定文档将所有尾注放置在何处。
// 如果我们将“Position”属性的值设置为“EndnotePosition.EndOfDocument”，
// 每个脚注都会显示在文档末尾的集合中。这是默认值。
// 如果我们将“Position”属性的值设置为“EndnotePosition.EndOfSection”，
// 每个脚注都会出现在文本包含尾注引用标记的部分末尾的集合中。
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

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

展示如何更改脚注/尾注引用标记的数字样式。

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
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.", "Custom footnote reference mark");

builder.InsertParagraph();

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.", "Custom endnote reference mark");

// 默认情况下，每个脚注和尾注的参考符号是其索引
// 在所有文档的脚注/尾注中。每个文档都维护单独的计数
// 用于脚注和尾注。默认情况下，脚注使用阿拉伯数字显示其编号，
// 并且尾注以小写罗马数字显示其编号。
Assert.AreEqual(NumberStyle.Arabic, doc.FootnoteOptions.NumberStyle);
Assert.AreEqual(NumberStyle.LowercaseRoman, doc.EndnoteOptions.NumberStyle);

// 我们可以使用“NumberStyle”属性将自定义编号样式应用于脚注和尾注。
// 这不会影响带有自定义引用标记的脚注/尾注。
doc.FootnoteOptions.NumberStyle = NumberStyle.UppercaseRoman;
doc.EndnoteOptions.NumberStyle = NumberStyle.UppercaseLetter;

doc.Save(ArtifactsDir + "InlineStory.RefMarkNumberStyle.docx");
```

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

* class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
